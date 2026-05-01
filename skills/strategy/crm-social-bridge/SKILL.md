---
name: crm-social-bridge
description: Map a CRM prospect list into a social engagement priority queue — scores each prospect for social fit, identifies which platforms to target, and generates a ranked outreach-ready worklist with draft engagement angles.
version: 1.0.0
author: Hermes (hermes-agent.nousresearch.com)
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, strategy, crm, lead-generation, outreach, engagement, bridge]
related_skills: [prospect-social-audit, social-profile-discover, brand-voice-system, comment-reply, dm-warmup]
inputs_required: [crm-prospect-list, target-platforms, engagement-goal]
deliverables: [social-engagement-priority-queue-with-draft-angles]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: [web_search, web_extract, curl]
required_env_vars: [FIRECRAWL_API_KEY]
glossary_terms: [audience-fit, platform-native]
---

# CRM → Social Engagement Bridge

Transform a CRM prospect list into a ranked, platform-specific engagement queue with draft angles for each prospect. This skill connects the lead discovery pipeline to the social media execution layer.

## Purpose

You have 50+ prospects in the CRM. You can't engage with all of them equally. This skill scores each prospect for social fit, identifies where they are active, and generates the first draft of how you would engage — so your daily social work starts from a prioritized queue, not a blank page.

## When to Use

- After a CRM batch is loaded and you want to begin social outreach
- Weekly: refreshing the engagement queue from new CRM entries
- Before running niche-account-discovery (to avoid duplicating known prospects)
- When pivoting from passive content to active engagement
- After a competitor audit reveals new target accounts to add to the CRM

## Inputs Required

- **CRM prospect list** (required — fetched from the CRM API)
- **Target platforms** (default: LinkedIn + X)
- **Engagement goal** (default: "warm relationship building")
  - Options: warm relationship building → nurture, direct outreach → meeting, content amplification → brand awareness
- **Your brand voice** (required — from brand-voice-system)
- **Daily engagement capacity** (default: 5 meaningful interactions/day)

## Procedure

### Step 1: Pull the CRM prospect list

```bash
# Get all companies from the CRM
curl -s "http://127.0.0.1:3210/api/companies" | jq -r '.companies[] | {name: .name, slug: .slug, website: .website, industry: .industry, location: .location, relevance: .relevance, about: .about}' > /tmp/crm_prospects.json

# Get all people for social profile enrichment
curl -s "http://127.0.0.1:3210/api/people" | jq -r '.people[] | {name: .name, company: .company, email: .email, phone: .phone}' > /tmp/crm_people.json
```

### Step 2: Score each prospect for social fit

For each company in the CRM, score across these dimensions (1–5 each):

| Dimension | High Score (5) | Low Score (1) |
|-----------|--------------|---------------|
| **Industry relevance** | Directly in your niche / ICP | Adjacent or unclear |
| **Company size fit** | Solo/small team (easy to reach decision-maker) | Enterprise (gatekeepers) |
| **Social presence** | Active on target platforms | No social found |
| **Engagement receptivity** | Responds to comments/DMs | Broadcast-only, no replies |
| **Recency / freshness** | Added to CRM in last 30 days | Stale prospect, may be outdated |
| **Content opportunity** | Posts regularly, you can add value | Rare posts, hard to engage naturally |

**Social Fit Score = sum of 6 dimensions (max 30).**

### Step 3: Identify target platforms per prospect

Use `social-profile-discover` for top-scored prospects, or infer from industry:

- **B2B professional services** → LinkedIn primary, X secondary
- **Creative / visual businesses** → Instagram primary, TikTok secondary
- **Local service businesses** → Facebook + Instagram
- **Tech / SaaS** → X + LinkedIn
- **Event / wedding / nonprofit** → Instagram + Facebook

### Step 4: Generate engagement angles

For each prospect in the priority queue, draft 2–3 natural engagement angles:

**Angle types:**
- **Value-first comment** on their recent post (add insight, ask thoughtful question)
- **Connection request / follow** with personalized note referencing their content
- **Content mention** — create a post that references their work (tag them)
- **DM warmup** — if they replied to a comment, move to DM with specific ask
- **Collaboration angle** — suggest a mutual-benefit content piece

**Example angles for a marketing agency prospect:**
1. "Comment on their recent case study post: 'Love the results on the X campaign — curious if you tested Y variation? We saw Z% lift with that approach.'"
2. "Share their post with your take: 'Great framework from {name}. Here's how we adapted it for {niche}...'"
3. "DM if they reply: 'Would love to swap notes on {topic} — our {client type} saw similar patterns.'"

### Step 5: Rank and queue

Sort by: **Social Fit Score desc → then by platform alignment → then by recency.**

Output a daily worklist sized to engagement capacity.

### Step 6: Push the engagement queue back to CRM

Update the CRM with the social engagement plan for each prospect:

```bash
cat > /tmp/crm_social_update.json << 'JSON'
{
  "company": "Example Corp",
  "tags": "#social-target #linkedin-primary #engagement-queued",
  "socialPlan": {
    "priority": 1,
    "platforms": ["linkedin", "x"],
    "angles": ["comment on case study", "share with adaptation"],
    "firstTouch": "2026-05-01",
    "status": "queued"
  }
}
JSON
curl -s -X PATCH "http://127.0.0.1:3210/api/companies/example-corp" \
  -H "Content-Type: application/json" \
  -d @/tmp/crm_social_update.json
```

## Output Format

```markdown
# CRM → Social Engagement Queue

## Queue Summary
- **Total prospects:** {n}
- **Scored for social fit:** {n}
- **High priority (score 24–30):** {n}
- **Medium priority (score 18–23):** {n}
- **Low priority (score <18):** {n}
- **No social presence found:** {n}

## Daily Engagement Worklist (Top {capacity})

### 1. {Company Name} (Score: {n}/30)
- **Platforms:** {platforms}
- **Industry:** {industry}
- **Location:** {location}
- **Social presence:** {urls}
- **Engagement angles:**
  1. {angle 1}
  2. {angle 2}
  3. {angle 3}
- **CRM link:** http://127.0.0.1:3210/api/companies/{slug}

### 2. ...

## Prospects Without Social Presence (needs `social-profile-discover`)
1. {name} — {industry} — {why no social found}

## Platform Distribution
- LinkedIn: {n} prospects
- X: {n} prospects
- Instagram: {n} prospects
- Facebook: {n} prospects
- TikTok: {n} prospects

## Engagement Goal Alignment
- **Goal:** {goal}
- **Recommended focus:** {platform} for {goal}
```

## Done Criteria

The skill is complete when:
1. Every CRM prospect has a social fit score
2. Top-scored prospects have platform recommendations
3. At least 2 engagement angles drafted per high-priority prospect
4. A daily worklist is generated matching engagement capacity
5. Social plan is pushed back to CRM for tracking

## Pitfalls

- Scoring all prospects equally (a law firm and a marketing agency need different approaches)
- Generating generic angles ("great post!" is not an angle — specific insight is)
- Over-targeting one platform (diversify based on where prospects are active)
- Ignoring prospects with low scores (move to nurture, don't delete)
- Not updating the CRM after engagement (track what you tried and what worked)

## Verification

Can you open the top-ranked prospect's LinkedIn/X profile and immediately see a post where your drafted angle would fit naturally? If not, the angle is too generic — refine it.

## See Also

- **references/platform-specs.md** — platform dimensions and benchmarks
- **references/tool-requirements.md** — API auth options
- **skills/research/prospect-social-audit/SKILL.md** — evaluating a single prospect
- **skills/research/social-profile-discover/SKILL.md** — finding profile URLs
- **skills/engagement/comment-reply/SKILL.md** — executing the engagement
- **skills/engagement/dm-warmup/SKILL.md** — moving to direct messages
