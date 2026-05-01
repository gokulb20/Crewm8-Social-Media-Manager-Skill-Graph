---
name: news-response
description: Scan for industry news, product launches, and competitor announcements — write quick-response posts within 1 hour with the brand's unique perspective or commentary.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, trends, news, quick-response, commentary, thought-leadership]
related_skills: [trend-monitor, post-create, brand-voice-system, trending-briefing]
inputs_required: [news-item-url-or-summary, brand-positioning, perspective-or-take]
deliverables: [news-response-draft-ready-to-post]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: ["FIRECRAWL_API_KEY"]
required_env_vars: ["FIRECRAWL_API_KEY"]
requires_capabilities: [web-search, web-extract]
---

# News Response

Scan for industry news and write fast, thoughtful responses that position the brand as plugged-in and opinionated. Speed wins on news — the first insightful take gets disproportionate engagement. Being the 4th person to comment on a story means you're invisible.

## Purpose

News commentary is the highest-leverage content type for building authority. It proves you're paying attention, have opinions, and can contextualize industry events. But only if you're fast and add genuine insight.

## When to Use

- Major industry announcement (funding, acquisition, product launch, regulation)
- Competitor launched something significant
- Technology breakthrough or trend report
- Founder says "we should weigh in"

## Inputs Required

- News item (URL, headline, or summary)
- Brand positioning (so the take is on-brand)
- Whether founder approval is needed for this specific topic

## Quick Reference

| News Type | Response Target | Format | Tone |
|----------|----------------|--------|------|
| Major industry news | Within 1 hour | Short post + optional follow-up thread | Insightful, fast analysis |
| Competitor announcement | Within 2-3 hours | Respectful commentary | Professional, differentiated |
| Data/trend report | Within 4-6 hours | Thread or LinkedIn post | Analytical, helpful framing |
| Founder/figure controversy | Assess carefully — sometimes silence | If engaging: calm, principled stance | Measured, values-driven |

## Procedure

1. **Monitor news channels:**
   - X lists of industry journalists and analysts
   - Google News alerts for key terms
   - Niche newsletters and SubStacks
   - Competitor social accounts

2. **When news breaks, assess:**
   - Relevant to brand audience?
   - Can brand add unique perspective?
   - Time-sensitive window?
   - Is silence smarter? (controversy, tragedy, legal)

3. **Draft the response:**
   - Acknowledge the news (1 line — assume audience hasn't seen it)
   - Add brand's unique take (what does this MEAN for the audience?)
   - Provide context the headline missed (this is where you add value)
   - Frame implications: why this matters, what to watch

4. **Choose format:**
   - X: fast short post or quote tweet of news source
   - LinkedIn: longer analysis post
   - Not typically breaking news for IG/TikTok (unless visual-first angle)

5. **Quality control:**
   - Fact check: confirmed or rumor?
   - Attribution: link to original source
   - Brand fit: makes brand look smart or opportunistic?

## Output Format

```markdown
# News Response: [Headline]

## Source
**News break:** [Timestamp]
**Source:** [URL or @handle]
**Summary:** [What happened]

## Assessment
**Relevance to audience:** [High / Medium / Low]
**Unique angle:** [Yes / No — what]
**First-mover window:** [Hours remaining]
**Risk level:** [Low / Medium / High]

## Response Draft
**Platform:** [X / LinkedIn]
[Full post text]
**Format:** [Short post / Thread / Quote tweet]
**Tone:** [Insightful / Analytical / Measured / Critical]
**CTA:** [What action to drive]
```

## Done Criteria

The skill is complete when:
1. News is verified (not rumor)
2. Response draft includes a unique take (not just "here's the news")
3. Format is matched to news type and platform
4. Link attribution to source is included
5. Content angle approved for sensitivity (if applicable)

## Pitfalls

- Responding without a genuine take ("This is big" — no insight)
- Taking a stance without founder approval
- Getting facts wrong because speed > accuracy
- Quoting competitor news in a way that promotes them
- Being the 14th person with the same take

## Verification

Before posting: is this take something only this brand could say? Is it more insightful than the top 3 existing responses? If not, refine or don't post.
