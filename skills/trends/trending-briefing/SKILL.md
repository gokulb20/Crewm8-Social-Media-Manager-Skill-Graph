---
name: trending-briefing
description: Compile a daily and weekly "what's trending" briefing for the founder — concise, scannable summary of topics, formats, news, and opportunities the brand should know about.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Trends, Briefing, Reporting, Founder-Update]
    related_skills: [trend-monitor, news-response, performance-report]
---

# Trending Briefing

Compile a concise daily or weekly briefing on what's trending in the brand's space. The founder doesn't have time to live on social media — this skill turns noise into signal: the 5-10 things they actually need to know.

## When to Use

- Daily: end-of-day or next-morning founder briefing
- Weekly: Friday or Monday summary of what mattered this week
- Pre-content-planning: briefing to inform the upcoming content calendar
- Founder says "what am I missing on social this week?"
- Event or conference week (elevated trend activity — founder wants the highlights)

## Quick Reference

| Briefing Cadence | Format | Ideal Length | Delivery |
|-----------------|--------|-------------|---------|
| Daily | Quick bullet scan | 5-8 items, 250-400 words | DM, email, or Slack message — something fast |
| Weekly | Structured report | 10-15 items, 500-800 words | Email, doc, or Notion page — more detailed |
| Event/Crisis | Rolling update | 3-5 items per update, 100-200 words | Real-time messaging |

## Procedure

1. Aggregate inputs from the monitoring period:
   - `trend-monitor` outputs (trends identified, scored, categorized)
   - `news-response` outputs (news items the brand responded to or passed on)
   - Competitor activity (from `competitor-audit` or manual observation)
   - Audience conversations (what is the niche talking about?)
   - Engagement spikes on brand posts (what unexpectedly performed well? Is it tied to a trend?)

2. Filter ruthlessly:
   - Not every trend the AI identified makes the founder briefing
   - Filter: "would this change anything the founder does today?" If no, cut it.
   - Target: 5-8 items for daily, 10-15 for weekly

3. For each briefing item, include:
   - The trend/topic (1 line description)
   - Why it matters (1 line — relevance to the brand)
   - What the brand did or should do (1 line — action/opportunity)
   - Supporting stat or example (if available)

4. Structure the briefing for scanability:
   - No walls of text. The founder reads this in 2-3 minutes.
   - Bullet format, bold key terms, clear categories
   - Lead with the most important item (don't bury the lead)
   - Include at least 1 "opportunity" item (not just monitoring — action)

5. Add founder action items:
   - "Reply to this yourself" (personal touches only the founder can do)
   - "Review this draft" (content needs founder perspective)
   - "Decision needed" (strategy call — ride this trend or skip?)

6. Track what the founder engages with:
   - Which items do they consistently ask about? (those matter most — prioritize them)
   - Which items do they ignore? (stop including that type)
   - Over time, the briefing gets sharper because you learn what the founder values

## Output Format

```markdown
# [Daily / Weekly] Trending Briefing: [Date]

## Top of Mind (1-2 items — must see)
- **[Topic]:** [1-line summary. Why it matters to us. What we should do.]

## Things Happening
- **[Trend/Topic]:** [Summary. Relevance. Action or note.]
- ...

## What Our Audience Is Talking About
- [Observation 1]
- [Observation 2]

## Competitor Watch
- **[Competitor]** — [What they did / posted / launched. Any lessons for us?]
- ...

## Opportunities
- [Trend the brand could ride — with specific angle suggestion]
- [Comment opportunity — specific account + post where engagement would be high-value]

## Founder Action Items
- [ ] [Specific action — reply, review, decision]
- [ ] ...

## Quick Stats
- Top trending topics this period: [List 3-5]
- Brand engagement trend: [Up / Flat / Down] vs. previous period
- Something we missed: [Trend that might have been worth engaging — learn for next time]
```

## Pitfalls

- Including too much detail (founder skims, doesn't study)
- Including items without action implications ("X is trending" — so what?)
- Briefing at the wrong frequency (daily when nothing happens = noise; weekly when things are moving fast = too slow)
- Same format every time — the founder stops reading it
- Not tracking what the founder actually finds useful (briefing quality should improve over time)
- Adding items just to fill the briefing (better 3 high-signal items than 10 filler bullets)

## Verification

Read your briefing in under 2 minutes. Did you get the most important information? Is there at least one item the founder can act on? Would you forward this to the founder if you were paying yourself $500/hour for their time?
