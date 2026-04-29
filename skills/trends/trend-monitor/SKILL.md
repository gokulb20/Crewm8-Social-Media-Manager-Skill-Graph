---
name: trend-monitor
description: Monitor trending topics, viral formats, and emerging hashtags in the startup/tech/AI space daily — score each trend and identify which the brand can authentically engage with.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, trends, monitoring, viral, hashtags, intelligence]
related_skills: [trending-briefing, news-response, post-create, meme-create, content-calendar]
inputs_required: [brand-niche, list-of-key-accounts-to-monitor, platform-access]
deliverables: [trend-report-with-act-now-recommendations]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
requires_capabilities: [web-search, web-extract]
---

# Trend Monitor

Scan the social landscape daily to identify what's trending, what's going viral, and what the brand should pay attention to. Trends have a 24-72 hour shelf life. The goal is to surface opportunities before they peak, not report on what everyone already knows.

## Purpose

Without trend monitoring, you're always reacting to what was. With it, you're one of the first voices on what's next. Being early on a trend is disproportionately rewarded by algorithms — this skill makes speed a structural advantage.

## When to Use

- Daily morning sweep (before content creation)
- Content planning sessions
- Low-engagement alert (is there a trend brand should join?)
- Competitor activity spike detected

## Inputs Required

- Brand niche and keywords
- Curated X list of industry voices
- Competitor accounts to watch
- Current content calendar (to slot trend-derived posts)

## Quick Reference

| Trend Source | What to Monitor | Method |
|-------------|----------------|--------|
| X trending topics | Trending sidebar + algorithm feed | X native, Trends24 |
| Viral post analysis | Disproportionate engagement in niche | Manual feed audit |
| LinkedIn trending | What's dominating feed this week | Manual audit, LinkedIn news |
| IG/TikTok trending audio/formats | Trending sounds, effects, formats | Platform discovery, TrendTok |
| Industry news | Major announcements, funding, launches | Google News, newsletters, X lists |
| Hashtag emergence | New hashtags gaining traction | Hashtag tracking, manual search |

## Procedure

1. **Morning sweep** (before 9 AM local):

   **Platform checks:**
   - X: Trending tab + "For You" feed — what's getting disproportionate engagement?
   - LinkedIn: Top-of-feed — what topics dominate today?
   - IG: Reels Explore — what audio/format is trending?
   - TikTok: FYP — what formats, sounds, topics are surging?

   **Niche checks:**
   - Curated X lists — what are industry voices all talking about?
   - Niche hashtag volume spikes
   - Competitor posts from last 24 hours

2. **Evaluate each trend using the Fit Matrix:**
   - Audience relevance: does our audience care? (1-10)
   - Brand authenticity: can we talk about this naturally? (1-10)
   - Actionability: can we create content in next 2-6 hours? (1-10)
   - Shelf life: hours/days before stale?
   - Competitive urgency: competitors already on this?

3. **Score and categorize:**
   - **Act now** (score > 24): create content within 2-6 hours
   - **Plan today** (score 18-24): slot into today or tomorrow
   - **Watch** (score 12-17): revisit in 24 hours
   - **Pass** (score < 12): not worth engaging

4. **For "act now" trends, immediately draft content angle:**
   - Unique brand take on this trend
   - Recommended format
   - Urgency note

## Output Format

```markdown
# Trend Monitor: [Date]

## Summary
**Total trends identified:** [N] | **Act now:** [N] | **Plan:** [N] | **Watch:** [N] | **Pass:** [N]

## ACT NOW

### Trend: [Name]
**Source:** [Platform]
**Peak window:** [Estimated hours remaining]
**Score:** [N]/30 (Relevance [N] Authenticity [N] Actionability [N])
**Brand angle:** [What to say about this]
**Recommended format:** [Post / Thread / Quote tweet / Video / Meme]
**Competitor status:** [Already on it?]

## PLAN TODAY / WATCH / PASS
[Same structure, lower urgency]
```

## Done Criteria

The skill is complete when:
1. Morning sweep is conducted across all 4 platforms
2. Trends are scored on the 3-dimension Fit Matrix
3. "Act now" trends have content angle and format recommended
4. Weekly trend patterns are noted (for the briefing)

## Pitfalls

- Chasing every trend (brand looks reactive, not strategic)
- Forcing the brand into a trend that doesn't fit
- Monitoring too slowly (report at 5 PM about something that peaked at 10 AM)
- Only looking at platform-native trending (missing niche-specific trends)

## Verification

For each "act now" trend: can you articulate the brand's unique take in one sentence that nobody else is saying? If it's "we agree with the consensus," it's not worth posting.
