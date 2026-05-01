---
name: prospect-social-audit
description: Given a company name and website, discover their social media presence across platforms, evaluate activity levels, and score engagement potential — bridges CRM prospecting with social engagement workflows.
version: 1.0.0
author: Hermes (hermes-agent.nousresearch.com)
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, research, prospecting, crm, discovery, audit, lead-generation]
related_skills: [social-profile-discover, profile-audit, comment-reply, influencer-outreach]
inputs_required: [company-name, company-website, founder-name-if-known]
deliverables: [social-presence-report-with-activity-scores]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: [web_search, web_extract, browser_navigate]
required_env_vars: [FIRECRAWL_API_KEY]
glossary_terms: [engagement-rate, hook, brand-voice-flex]
---

# Prospect Social Audit

Discover and evaluate a prospect company's social media presence across platforms. This skill bridges the gap between "I found a company in the CRM" and "I know their social activity level and how to engage." Use it before drafting outreach or social engagement.

## Purpose

When prospecting at scale, you end up with a list of companies. Most have some social presence. But which ones are active? Which platform should you engage on? Which profile belongs to the decision-maker vs. the company? This skill answers those questions systematically.

## When to Use

- After pushing a new prospect to CRM, enrich with social data
- Before planning social engagement outreach
- Evaluating whether a prospect is "socially contactable"
- Comparing multiple prospects by social activity level
- Identifying warm leads (active posters are often more receptive to engagement)

## Inputs Required

- **Company name** (required)
- **Company website** (required — used to find social links)
- **Founder/contact name** (optional — enables personal profile discovery)
- **Target platforms** (default: LinkedIn + Instagram + X + Facebook)

## Quick Reference

| Platform | What to Find | Activity Signal |
|----------|-------------|----------------|
| LinkedIn | Company page + founder profile | Posting frequency, employee count, engagement per post |
| Instagram | Business account | Post frequency, follower count, comment engagement |
| X (Twitter) | Company handle + personal handle | Tweet frequency, follower ratio, replies |
| Facebook | Business page | Post frequency, reviews, community size |
| TikTok | Business/creator account | Video frequency, view counts, trend adoption |
| YouTube | Channel | Upload frequency, subscriber count, view averages |

## Procedure

### Phase 1: Discovery

1. **Search for social profiles using the company name and website.**
   Delegate to `social-profile-discover` for systematic discovery, or search directly:

   ```bash
   # LinkedIn company page
   firecrawl search "site:linkedin.com/company \"{company name}\""
   
   # Instagram
   firecrawl search "site:instagram.com \"{company name}\" {city}"
   
   # Facebook business page
   firecrawl search "site:facebook.com \"{company name}\" {city}"
   
   # X / Twitter
   firecrawl search "site:x.com OR site:twitter.com \"{company name}\""
   ```

2. **Check company website footer and Contact/About pages for social icon links.**
   ```bash
   firecrawl scrape "{company_website}" --format markdown
   # Look for: href="https://linkedin.com/company/..."
   #           href="https://instagram.com/..."
   #           href="https://facebook.com/..."
   #           href="https://x.com/..." or "https://twitter.com/..."
   ```

3. **If founder/contact name is known, find their personal profiles.**
   ```bash
   firecrawl search "site:linkedin.com/in \"{contact_name}\" {company_name}"
   firecrawl search "site:x.com \"{contact_name}\" {company_abbreviation}"
   ```

### Phase 2: Evaluation

4. **For each discovered profile, evaluate activity level:**

   **LinkedIn Company Page:**
   - Posting frequency: posts per week (estimate from last 30 days)
   - Engagement: average likes/comments per post
   - Follower count: size of audience
   - Employee count: company size signal

   **Instagram:**
   - Post frequency: posts per week
   - Follower count
   - Average likes/comments per post
   - Story activity: active Stories? (check via browser if possible)

   **X (Twitter):**
   - Tweet frequency: tweets per week
   - Follower/following ratio
   - Reply activity: do they engage with replies?
   - Content type: original vs. retweets

   **Facebook:**
   - Post frequency
   - Page likes/follows
   - Review count and rating
   - Community engagement on posts

5. **Score each profile (0–10):**

   | Criterion | Weight | Scoring |
   |-----------|--------|---------|
   | Posting consistency (last 30 days) | 30% | 0 = no posts, 5 = weekly, 10 = daily+ |
   | Engagement level (avg per post) | 25% | 0 = none, 5 = moderate, 10 = high |
   | Audience size | 20% | 0 = <100, 5 = 1K–10K, 10 = >50K |
   | Content quality/relevance | 15% | Subjective: useful, original content |
   | Responsiveness (replies to comments) | 10% | 0 = never, 5 = sometimes, 10 = always |

6. **Calculate overall Social Presence Score:**
   - Weighted average across all platforms
   - 0–3: Low — limited social presence, hard to engage
   - 4–6: Medium — present, some activity, possible to engage
   - 7–10: High — active, engaged, excellent engagement target

### Phase 3: Engagement Strategy

7. **Identify the best platform for first engagement:**
   - Highest activity level
   - Platform where your brand already has presence
   - Platform where the prospect's content is most "commentable" (opinion posts, questions, discussions)

8. **Find 1–3 recent posts worth engaging with:**
   - Recent (< 7 days old)
   - High engagement (discussion-worthy)
   - Topic overlap with your product/industry
   - Not promotional or sensitive

9. **Draft a value-add comment idea for the best post.**
   (Defer full drafting to `comment-reply`.)

## Output Format

```markdown
# Prospect Social Audit: {Company Name}

## Summary
**Audit date:** {date}
**Social Presence Score:** {score}/10 — {Low/Medium/High}
**Best platform for engagement:** {platform}
**Activity level:** {description}

## Discovered Profiles

### LinkedIn
- **Company page:** {url} (or "Not found")
- **Followers:** {count} | **Employees:** {count}
- **Posting frequency:** {posts/week} | **Avg engagement:** {likes/comments}
- **Last post:** {date}
- **Activity score:** {score}/10
- **Notable:** {observation}

- **Contact profile** (if found):
  - **URL:** {url}
  - **Activity:** {description}
  - **Recent post topics:** {topics}

### Instagram
- **Handle:** @{handle} (or "Not found")
- **Followers:** {count} | **Posts:** {count}
- **Posting frequency:** {posts/week}
- **Avg engagement:** {likes/comments per post}
- **Activity score:** {score}/10

### X (Twitter)
- **Handle:** @{handle} (or "Not found")
- **Followers:** {count} | **Following:** {count}
- **Tweet frequency:** {tweets/week}
- **Activity score:** {score}/10

### Facebook
- **Page:** {url} (or "Not found")
- **Likes:** {count} | **Reviews:** {count} ({rating}★)
- **Activity score:** {score}/10

### Other (TikTok, YouTube)
- **{Platform}:** {handle/url} (or "Not found")
- **Activity score:** {score}/10

## Engagement Opportunities

### Best Post to Engage With
- **Platform:** {platform}
- **Post URL:** {url}
- **Post topic:** {summary}
- **Why this post:** {reason — recent, discussion-worthy, topic overlap}
- **Suggested comment angle:** {one-sentence idea}

### 1–2 Other Posts Worth Watching
- {url} — {why}
- {url} — {why}

## Social Profile Links (Ready for CRM)
```json
{
  "companySocials": {
    "linkedin": "...",
    "facebook": "...",
    "instagram": "...",
    "twitter": "...",
    "youtube": "...",
    "tiktok": "..."
  },
  "contactSocials": {
    "linkedin": "...",
    "twitter": "..."
  }
}
```
```

## Done Criteria

The skill is complete when:
1. At least one social profile is discovered (company or contact)
2. Each discovered profile has an activity score
3. Social Presence Score is calculated
4. Best platform for engagement is identified
5. At least one recent post is identified for engagement
6. Social profile links are formatted for CRM enrichment
7. If no profiles found, gaps are documented with alternative engagement approaches

## CRM Integration

After completing this audit, enrich the CRM prospect:

```bash
curl -s -X PATCH http://127.0.0.1:3210/api/companies/{slug} \
  -H "Content-Type: application/json" \
  -d '{
    "companySocials": {...},
    "contactSocials": {...}
  }'
```

Or push as enrichment via `POST /api/push` (idempotent — fills empty fields only).

## Pitfalls

- Confusing a personal Instagram with a business one — check bio and content
- Scoring a dormant account as "active" because it has many followers
- Assuming LinkedIn presence equals social activity (many companies have pages but never post)
- Missing profiles because the company uses a different name on social media (check website footer FIRST)
- Using `localhost:3210` instead of `127.0.0.1:3210` for CRM calls (Electron intercepts localhost)

## Verification

Can you answer:
- "Which platform should I engage this prospect on?"
- "What's one specific post I could comment on today?"
- "Is this prospect worth social engagement outreach or should I use email?"

If the answer to any is "I don't know," the audit is incomplete.

## See Also

- **references/platform-specs.md** — character limits, hashtag rules, ER benchmarks
- **references/tool-requirements.md** — API auth, tool options per platform
- **skills/research/social-profile-discover/SKILL.md** — systematic profile discovery
- **skills/engagement/comment-reply/SKILL.md** — drafting engagement comments
- **GLOSSARY.md** — ER%, hook, brand-voice-flex definitions
