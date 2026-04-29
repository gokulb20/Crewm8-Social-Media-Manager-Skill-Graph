---
name: trending-briefing
description: Compile a daily or weekly "what's trending" briefing for the founder — concise, scannable summary of topics, formats, news, and opportunities the brand should know about.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, trends, briefing, reporting, founder-update, executive-summary]
related_skills: [trend-monitor, news-response, performance-report, content-calendar]
inputs_required: [trend-monitor-outputs, news-response-outputs, competitor-activity, audience-conversations]
deliverables: [founder-facing-briefing-daily-or-weekly]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Trending Briefing

Compile a concise daily or weekly briefing on what's trending in the brand's space. The founder doesn't have time to live on social media — this skill turns noise into signal: the 5-10 things they actually need to know.

## Purpose

The founder should never have to ask "what's happening on social?" This briefing pre-empts that question. It's designed to be read in 2 minutes, acted on in 5 minutes, and filed away for content planning reference.

## When to Use

- Daily: end-of-day or next-morning founder briefing
- Weekly: Friday or Monday summary
- Pre-content-planning: briefing to inform the calendar
- Founder asks "what am I missing?"

## Inputs Required

- Trend monitor outputs (from `trend-monitor`)
- News response decisions (from `news-response`)
- Competitor activity observations
- Brand engagement data (from `metrics-track`)
- Content calendar (for relevance context)

## Quick Reference

| Cadence | Format | Ideal Length | Delivery |
|---------|--------|-------------|---------|
| Daily | Bullet scan | 5-8 items, 250-400 words | DM, email, or Slack |
| Weekly | Structured report | 10-15 items, 500-800 words | Doc or email |
| Event/Crisis | Rolling update | 3-5 items, 100-200 words | Real-time messaging |

## Procedure

1. **Aggregate inputs** from monitoring period: trends, news, competitor activity, audience conversations, engagement spikes.

2. **Filter ruthlessly.** Not every trend makes the briefing. Filter: "would this change anything the founder does today?" If no, cut it.

3. **For each briefing item:**
   - Trend/topic (1 line)
   - Why it matters (1 line — relevance to brand)
   - What brand did or should do (1 line — action/opportunity)

4. **Structure for scanability:**
   - No walls of text. 2-3 minute read max.
   - Bullet format, bold key terms
   - Most important item first
   - At least 1 "opportunity" item (not just monitoring)

5. **Add founder action items:**
   - "Reply to this yourself"
   - "Review this draft"
   - "Decision needed: ride this trend or skip?"

## Output Format

```markdown
# [Daily/Weekly] Trending Briefing: [Date]

## Top of Mind (Must See)
- **[Topic]:** [Summary. Why it matters. What we should do.]

## Things Happening
- **[Trend]:** [Summary. Relevance. Action or note.]
...

## Competitor Watch
- **[Competitor]** — [What they did. Lessons for us?]

## Opportunities
- [Trend with specific brand angle suggestion]
- [Comment opportunity — specific account + post]

## Founder Action Items
- [ ] [Action: reply / review / decide]
```

## Done Criteria

The skill is complete when:
1. 5-8 items for daily, 10-15 for weekly
2. Each item has a "why it matters" and "action" component
3. Briefing is readable in under 3 minutes
4. At least 1 action item for the founder
5. Items filtered by relevance (not everything makes the cut)

## Pitfalls

- Including too much detail (founder skims, doesn't study)
- Items without action implications ("X is trending" — so what?)
- Same format every session (founder stops reading)
- Adding filler items (better 3 high-signal items than 10 bullets)
- Not tracking what the founder finds useful

## Verification

Read your briefing in under 2 minutes. Did you get the most important information? Is there at least one item the founder can act on? Would you forward this if you were paying yourself $500/hour for their time?
