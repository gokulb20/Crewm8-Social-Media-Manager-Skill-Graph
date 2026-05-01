---
name: competitor-content-audit
description: Analyze a competitor's recent social content — extract what's working, what's not, their posting cadence, content mix, and voice patterns — feeds directly into brand-voice-system, content-pillars, and cadence-timing.
version: 1.0.0
author: Hermes (hermes-agent.nousresearch.com)
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, research, competitor-analysis, content-strategy, intelligence]
related_skills: [social-profile-discover, brand-voice-system, content-pillars, cadence-timing]
inputs_required: [competitor-name, competitor-social-handles, audit-period-days]
deliverables: [competitor-content-report-with-strategic-insights]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: [web_search, web_extract, browser_navigate]
required_env_vars: [FIRECRAWL_API_KEY]
glossary_terms: [engagement-rate, content-pillar, cadence, hook]
---

# Competitor Content Audit

Analyze a competitor's social media content to understand their strategy, identify what's working, and find gaps you can exploit. This is competitive intelligence that feeds directly into your own strategy.

## Purpose

Your competitors are already testing what works. Instead of guessing, learn from their data. This skill systematically reviews their last 30–90 days of content, extracts patterns, and translates them into actionable insights for your own brand.

## When to Use

- Before defining content-pillars for a new brand
- When engagement drops and you need fresh angles
- Entering a new niche where competitors are established
- Quarterly competitive review
- After a competitor launches a product or campaign that gained traction

## Inputs Required

- **Competitor name** (required)
- **Competitor social handles** (at least one platform — required)
- **Audit period** (default: 30 days, range: 7–90 days)
- **Platforms to audit** (default: X + LinkedIn + Instagram)
- **Your brand positioning** (optional — for gap analysis)

## Procedure

### Step 1: Inventory competitor's social presence

Use `social-profile-discover` to find all competitor profiles, or search directly:

```bash
firecrawl search "site:x.com \"{competitor_name}\" OR \"{competitor_handle}\""
firecrawl search "site:linkedin.com/company \"{competitor_name}\""
firecrawl search "site:instagram.com \"{competitor_handle}\""
```

### Step 2: Extract recent content

For each platform, extract the last 30 days of posts:

**X (Twitter):**
```bash
# Search for recent tweets
firecrawl search "site:x.com \"{competitor_handle}\" since:2026-04-01" --limit 20
# Or scrape the profile page
firecrawl scrape "https://x.com/{handle}" --format markdown
```

**LinkedIn:**
```bash
firecrawl search "site:linkedin.com/posts \"{competitor_name}\"" --limit 15
```

**Instagram:**
```bash
firecrawl search "site:instagram.com \"{competitor_handle}\"" --limit 15
```

### Step 3: Categorize content

For each extracted post, classify:

| Category | Description | Examples |
|----------|-------------|----------|
| **Education** | How-to, tips, frameworks | "5 ways to...", "Here's the formula..." |
| **POV / Opinion** | Contrarian takes, hot takes | "Most people get X wrong..." |
| **Proof / Social** | Case studies, testimonials, wins | "Client results:", "We just hit..." |
| **BTS / Process** | Behind-the-scenes, building in public | "Day in the life:", "What we're working on..." |
| **CTA / Promo** | Product mentions, launches, offers | "New feature:", "Link in bio..." |
| **Engagement** | Polls, questions, community | "What do you think?", "Poll:" |
| **Trend / News** | Reacting to industry news | "Just saw the news about..." |

### Step 4: Analyze performance signals

For each post, estimate engagement level (low/medium/high) based on:
- Like/comment/repost counts visible on the post
- Reply depth (long threads vs. none)
- Whether it was reshared by others in the niche

### Step 5: Extract patterns

**Content Mix:**
- What percentage is Education vs. POV vs. Proof vs. BTS vs. CTA?
- Is there a dominant pillar? A missing pillar?

**Format Patterns:**
- Threads vs. single posts on X
- Carousels vs. images vs. video on LinkedIn/IG
- Short-form vs. long-form

**Hook Patterns:**
- How do they open posts? (Question, stat, story, contrarian claim?)
- Which hook style gets the most engagement?

**CTA Patterns:**
- What do they ask the audience to do?
- Do they drive to newsletter, product, or community?

**Posting Cadence:**
- How many posts per day/week?
- Consistent schedule or sporadic?
- Best-performing days/times?

**Voice Patterns:**
- Formal or casual?
- First-person (I/we) or brand voice?
- Emoji usage, humor, controversy level?

### Step 6: Identify gaps and opportunities

Compare against your brand:
- **What they do well that you don't:** (e.g., "They post 3 educational carousels/week — we do 0")
- **What they neglect that you can own:** (e.g., "They never show BTS — we can be the transparent brand")
- **Where their engagement is weak:** (e.g., "Their POV posts get 2x engagement but they only do 1/month")
- **Audience questions they leave unanswered:** (scan comments for repeated questions)

### Step 7: Generate actionable recommendations

Turn insights into specific actions for your content strategy.

## Output Format

```markdown
# Competitor Content Audit: {Competitor Name}

## Overview
- **Audit period:** {date range}
- **Platforms analyzed:** {list}
- **Posts reviewed:** {count}
- **Competitor social presence score:** {score}/10

## Content Mix (Last 30 Days)
| Category | Count | % of Total | Avg Engagement |
|----------|-------|-----------|----------------|
| Education | {n} | {n}% | {low/med/high} |
| POV / Opinion | {n} | {n}% | {low/med/high} |
| Proof / Social | {n} | {n}% | {low/med/high} |
| BTS / Process | {n} | {n}% | {low/med/high} |
| CTA / Promo | {n} | {n}% | {low/med/high} |
| Engagement | {n} | {n}% | {low/med/high} |
| Trend / News | {n} | {n}% | {low/med/high} |

## Top 3 Performing Posts
1. **{Platform}** — {topic} — {why it worked}
2. **{Platform}** — {topic} — {why it worked}
3. **{Platform}** — {topic} — {why it worked}

## Bottom 3 Performing Posts
1. **{Platform}** — {topic} — {why it underperformed}
2. ...

## Cadence & Timing
- **Posting frequency:** {n} posts/week on {platform}
- **Most active days:** {days}
- **Consistent schedule?** {Yes/No}

## Voice & Format Patterns
- **Voice:** {formal/casual/first-person/brand}
- **Dominant format:** {threads/carousels/images/video}
- **Hook style:** {pattern}
- **CTA style:** {pattern}

## Strategic Gaps & Opportunities
1. **Gap:** {what they miss} → **Opportunity:** {what you can own}
2. **Gap:** {weak area} → **Opportunity:** {where to differentiate}
3. **Gap:** {audience need} → **Opportunity:** {content to create}

## Recommendations for Your Brand
1. **Immediate (this week):** {action}
2. **Short-term (this month):** {action}
3. **Long-term (ongoing):** {action}
```

## Done Criteria

The skill is complete when:
1. At least 20 posts reviewed across platforms
2. Content mix percentages calculated
3. Top 3 and bottom 3 posts identified with reasoning
4. Cadence, voice, and format patterns documented
5. At least 3 strategic gaps identified
6. Specific recommendations generated

## Pitfalls

- Assuming engagement = quality (viral ≠ good for business)
- Copying competitor voice instead of differentiating
- Only auditing one platform (competitors often have different strategies per platform)
- Ignoring comments (audience questions in comments reveal unmet needs)
- Over-analyzing old content (focus on last 30 days for current strategy)

## Verification

Can you answer: "What's one specific thing this competitor does that we should do differently?" If you can't, the audit is too surface-level.

## See Also

- **references/platform-specs.md** — platform dimensions and benchmarks
- **skills/research/social-profile-discover/SKILL.md** — finding competitor profiles
- **skills/strategy/content-pillars/SKILL.md** — defining your own pillars
- **skills/strategy/brand-voice-system/SKILL.md** — developing differentiated voice
