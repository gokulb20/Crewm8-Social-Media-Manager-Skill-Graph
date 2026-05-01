---
name: content-pillars
description: Define 3-5 content pillars and a topic taxonomy that translates brand positioning into repeatable content categories the agent can generate against every week without running out of ideas.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, strategy, content-pillars, taxonomy, planning, repetition]
related_skills: [positioning-statement, brand-voice-system, content-calendar, hook-write]
inputs_required: [positioning-statement, audience-research-or-customer-insights]
deliverables: [content-pillar-document-with-topic-bank]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: ["FIRECRAWL_API_KEY"]
required_env_vars: ["FIRECRAWL_API_KEY"]
---

# Content Pillars

Transform brand positioning into 3-5 repeatable content categories (pillars). Each pillar is a lens through which the brand talks about the world. The topic taxonomy underneath ensures the agent never runs out of specific, on-brand ideas.

## Purpose

Without pillars, content is random. With pillars, every post has a job: educate, persuade, prove, humanize, or convert. Pillars make the content calendar fillable without creativity blocks, and they make the brand's feed feel cohesive instead of scattershot.

## When to Use

- After positioning is locked, before the first calendar
- Content feels repetitive or scattered
- Quarterly strategy refresh
- Expanding to a new platform
- Founder says "I don't know what to post about"

## Inputs Required

- Positioning statement (from `positioning-statement` skill)
- Brand voice guide (from `brand-voice-system` skill)
- Customer interview insights or audience pain points
- Competitor content audit (what's working for them)
- Platform strategy (which platforms are active)

## Quick Reference

| Pillar Type | Purpose | Example Topics | Best Formats |
|-------------|---------|---------------|-------------|
| Education / How-to | Teach something valuable | Frameworks, step-by-step guides, mistakes to avoid | Threads, carousels, how-to videos |
| Point of View / Contrarian | Share a differentiated opinion | Hot takes, industry myths, "unpopular opinion" | Short posts, quote tweets, opinion threads |
| Proof / Social Proof | Show the thing works | Case studies, results, revenue updates, customer stories | Metric-led posts, testimonial graphics |
| Behind the Scenes / Build-in-Public | Humanize the brand | Team culture, process, failures, lessons learned, "how it's going" | Photo + caption, process videos, raw updates |
| CTA / Conversion | Drive action | Product launches, demo requests, waitlists, newsletter signups | Launch posts, demo clips, link posts |

## Procedure

1. **Start with the positioning statement.** For each potential pillar, ask: "Does content in this pillar reinforce the brand's core message?" If the answer is "not really," that pillar doesn't belong.

2. **Define 3-5 pillars.** Each pillar gets:
   - A name (1-3 words)
   - A one-sentence description of what content in this pillar does
   - A target split (% of weekly output)
   - 10-15 specific topic ideas (not templates — actual topics that could be posts)
   - The target emotional response: do we want the reader to think, feel, or act?

3. **Map each pillar to the right formats:**
   - Education: threads, carousels, how-to videos, LinkedIn carousels
   - POV: short takes, quote tweets, contrarian threads, LinkedIn opinion posts
   - Proof: case study posts, metric screenshots, testimonial graphics, revenue update threads
   - BTS: photo + caption, process videos, unfiltered updates, TikTok POV content
   - CTA: launch announcements, link posts, demo clips, waitlist pages

4. **Map each pillar to the right platforms:**
   - Education dominates LinkedIn and X
   - POV lives primarily on X (and occasionally LinkedIn)
   - BTS thrives on IG Stories and TikTok
   - Proof works everywhere but lands differently (metrics on X, stories on LinkedIn)
   - CTA works where the audience already trusts you — earn it with other pillars first

5. **Define the pillar mix (recommended starting point, adjust per data):**
   - Education: 35% of weekly output
   - POV: 25%
   - Proof: 20%
   - BTS: 15%
   - CTA: 5% (you earn the right to ask)

6. **Build a 15-topic bank per pillar.** Topics should be specific, not generic. Bad: "SaaS tips." Good: "Why charging monthly killed our growth (and what we switched to)."

7. **Set pillar health check rules:**
   - Any pillar exceeding 50% of weekly output? Rebalance.
   - Any pillar with zero posts this week? Fill it.
   - Any pillar consistently underperforming (below average ER for 3+ weeks)? Diagnose or retire.

## Output Format

```markdown
# [Brand] Content Pillars — [Date]

## Pillar 1: [Name]
**Goal:** [What this content achieves for the audience and the brand]
**Target split:** [X]% of weekly output
**Best formats:** [List 2-3]
**Platform priority:** [Platform A > Platform B > ...]
**Emotional target:** [Think / Feel / Act]

### Topic Bank (15 ideas)
1. [Specific, actionable topic]
2. [Specific, actionable topic]
...15

## Pillar 2: [Name]
...

## Pillar Mix Target
| Pillar | % of Weekly | X | LinkedIn | IG | TikTok |
|--------|------------|---|---|-----|--------|
| Education | 35% | Threads | Carousels | Carousels | How-tos |
| POV | 25% | Short posts | Opinion posts | — | Reaction videos |
| Proof | 20% | Metric posts | Case studies | Testimonials | — |
| BTS | 15% | Photo posts | — | Stories | POV clips |
| CTA | 5% | Launch posts | Demos | — | — |

## Pillar Health Check (Review Monthly)
- Which pillar drives the most engagement?
- Which pillar drives the most conversions?
- Which pillar is underrepresented or overperforming?
- Is any pillar below average ER for 3+ weeks? Diagnose.
```

## Done Criteria

The skill is complete when:
1. 3-5 pillars are defined with names, goals, and target splits
2. Each pillar has 10-15 specific topic ideas (not generic categories)
3. Each pillar is mapped to formats and platforms
4. The pillar mix totals 100% and is actionable
5. The health check rules are documented

## Pitfalls

- More than 5 pillars dilutes everything — the audience can't tell what you stand for
- Pillars that are too broad ("Business Advice") are useless as a filter
- Same pillar mix on every platform (X is not LinkedIn is not TikTok)
- CTA content without scaffolding from other pillars (you can't ask before you give)
- Topic banks that run dry in 2 weeks (aim for 15 topics per pillar — that's 3 months of material before repeating)

## Verification

Map the last 2 weeks of posts to pillars. If more than 20% don't fit any pillar, the taxonomy is wrong. If one pillar exceeds 50% of output, rebalance. Can you look at the topic bank and immediately write a post from any topic? If a topic makes you think "I have nothing to say about this," it's not specific enough.

## Example

*Input:* SaaS analytics tool positioning = "Product analytics for B2B founders who hate dashboards."

*Output:*
- **Pillar 1 (Education):** "Product analytics that actually matter" — topics: 3 metrics that predict churn, why DAU is a vanity metric, how to set up your first retention cohort
- **Pillar 2 (POV):** "Unpopular analytics takes" — topics: why dashboard tools make worse decisions, the metric VCs care about that you're ignoring
- **Pillar 3 (Proof):** "Customer results" — topics: how [customer] reduced churn 40%, revenue impact of fixing onboarding drop-off
- **Pillar 4 (BTS):** "Building an analytics company" — topics: why we rebuilt our data pipeline, the feature customers begged for that we said no to
- **Pillar 5 (CTA):** "Try it" — topics: free trial launch, comparison vs. competitors, feature deep-dives
