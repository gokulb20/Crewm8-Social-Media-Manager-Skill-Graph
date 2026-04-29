---
name: trend-monitor
description: Monitor trending topics, viral post formats, and emerging hashtags in the startup/tech/AI space daily — identify which trends the brand can authentically engage with.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Trends, Monitoring, Viral, Hashtags]
    related_skills: [trending-briefing, news-response, post-create, meme-create]
---

# Trend Monitor

Scan the social landscape daily to identify what's trending, what's going viral, and what the brand should pay attention to. Speed matters — trends have a 24-72 hour shelf life. The goal is to surface opportunities before they peak, not report on what everyone already knows.

## When to Use

- Daily morning sweep (before content creation/engagement sessions)
- Content planning sessions (what trends should influence this week's calendar?)
- Low-engagement alert (is there a trending conversation the brand should join?)
- Competitor activity spike detected (what did they ride that you missed?)
- Weekly trend briefing for the founder (see `trending-briefing` skill)

## Quick Reference

| Trend Source | What to Monitor | Tool / Method |
|-------------|----------------|--------------|
| X trending topics | Platform-native trending sidebar + "For You" algorithmic feed | X native, Trends24.in |
| X viral post analysis | What formats are getting disproportionate engagement in the niche? | Manual feed audit, Typefully trends |
| LinkedIn trending | What topics are dominating LinkedIn's feed algorithm this week? | Manual feed audit, LinkedIn news |
| IG/TikTok trending audio/formats | What audio, effects, and formats are trending on Reels/TikTok? | Platform-native discovery, TrendTok |
| Industry news | Major announcements, funding rounds, product launches in the niche | Google News, TechCrunch, niche newsletters, X lists |
| Hashtag emergence | New hashtags gaining traction in the niche | Hashtag tracking tools, manual search |
| Meme format emergence | What new meme formats are cross-pollinating into the niche? | Know Your Meme, manual feed audit |

## Procedure

1. Conduct a morning sweep (ideally before 9 AM local time):

   **Platform-specific checks:**
   - X: Trending tab (set to relevant location/category). Scan top 20 trending topics.
   - X: "For You" algorithmic feed — what's getting disproportionate engagement?
   - LinkedIn: Top-of-feed algorithmic posts — what topics dominate today?
   - Instagram: Reels Explore tab — what audio/format is trending?
   - TikTok: FYP scan — what formats, sounds, and topics are surging?

   **Niche-specific checks:**
   - Scan your curated X lists of industry voices — what are they all talking about?
   - Check niche-specific hashtags — any volume spikes?
   - Review the last 24 hours of posts from top competitor accounts

2. For each identified trend, evaluate:

   **Trend Fit Matrix:**
   - Audience relevance: does our target audience care about this? (1-10)
   - Brand authenticity: can we talk about this without forcing it? (1-10)
   - Actionability: can we create content about this in the next 2-6 hours? (1-10)
   - Shelf life: how many hours/days before this is stale? (estimate)
   - Competitive urgency: are competitors already on this? (yes/no/how many)

3. Score each trend and categorize:
   - **Act now** (score > 24): create content within 2-6 hours
   - **Plan today** (score 18-24): slot into today or tomorrow's content
   - **Watch** (score 12-17): monitor for development; revisit in 24 hours
   - **Pass** (score < 12): not worth brand engagement

4. For "act now" trends, immediately draft a content angle:
   - What's the brand's unique take on this trend?
   - What format works best? (quick post, thread, quote tweet, video response)
   - Who should write it? (AI first draft vs. founder directly)

5. Track trends over time:
   - Which trends keep re-emerging? (these become content pillars or ongoing topics)
   - Which trends did the brand successfully ride? (what was the engagement lift?)
   - Which trends did the brand miss? (why — was the monitoring too slow?)

## Output Format

```markdown
# Trend Monitor: [Date, Time]

## Trend Sweep Summary
**Platforms checked:** X, LinkedIn, IG, TikTok
**Total trends identified:** [N]
**Act now:** [N] | **Plan today:** [N] | **Watch:** [N] | **Pass:** [N]

---

## ACT NOW

### Trend: [Name / Topic]
**Source:** [Platform + where it's surfacing]
**Peak window:** [Estimated hours remaining]
**Relevance:** [N]/10 | **Authenticity:** [N]/10 | **Actionability:** [N]/10
**Score:** [N]/30
**Content angle:** [What the brand should say about this]
**Recommended format:** [Post / Thread / Quote tweet / Video / Meme]
**Draft in:** [Link to drafted content or "delegate to post-create"]
**Competitor status:** [Already on it? Who?]

---

## PLAN TODAY

### Trend: [Name]
... [same structure, less urgency]

---

## WATCH

### Trend: [Name]
... [same structure, with revisit note]

---

## PASS

### Trend: [Name]
**Why pass:** [Not our audience / Inauthentic / Already stale]

---

## Trend Patterns (Weekly)
- **Re-emerging topics:** [List — these might be content pillars in disguise]
- **New hashtags gaining traction:** [List]
- **Viral formats to adapt:** [Describe format + brand angle]
```

## Pitfalls

- Chasing every trend (brand looks reactive, not strategic)
- Forcing the brand into a trend that doesn't fit (audience sees through it instantly)
- Monitoring too slowly (trend report at 5 PM about something that peaked at 10 AM = useless)
- Only looking at platform-native trending (misses niche-specific trends that matter more)
- Trend fatigue: jumping on 3+ trends per day (brand has no coherent message anymore)
- Trend-hopping without a unique angle (retweeting the same take as everyone else)

## Verification

For each "act now" trend: can you articulate the brand's unique take in one sentence that nobody else is saying? If the answer is "we agree with the consensus," it's not worth posting. For each trend categorized: did you score it honestly or did excitement inflate the authenticity score?
