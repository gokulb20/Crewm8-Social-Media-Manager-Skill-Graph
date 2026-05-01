---
name: meme-create
description: Create platform-relevant meme concepts adapted to the brand voice — with text overlay, format reference, and posting context — for X, Instagram, and TikTok.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, visual, memes, humor, engagement, creativity]
related_skills: [brand-voice-system, visual-plan, image-prompt, asset-format, trend-monitor]
inputs_required: [meme-opportunity-context, brand-humor-boundaries, target-platform]
deliverables: [meme-concept-with-text-overlay-and-risk-assessment]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: ["FIRECRAWL_API_KEY"]
required_env_vars: ["FIRECRAWL_API_KEY"]
---

# Meme Create

Design branded meme concepts that feel native to the platform and authentic to the brand. Memes are high-risk, high-reward — done right they're the most shared content type; done wrong they signal that a brand is trying too hard.

## Purpose

Memes juice the algorithm in ways polished content can't. They're fast, shareable, and community-building. But forced memes are the fastest way to look out of touch. This skill produces memes that feel natural, not corporate.

## When to Use

- Trending meme format relevant to the niche
- Low-engagement period (memes can reset algorithmic momentum)
- Community inside joke has emerged
- Competitor just posted something too serious (counter with humor)
- Industry pain point that's universally relatable

## Inputs Required

- Meme opportunity (trending format, inside joke, pain point, competitor moment)
- Brand humor style (from voice guide: dry, absurd, self-deprecating, playful, none)
- Risk tolerance (how edgy is the brand willing to be?)
- Target platform

## Quick Reference

| Meme Type | Risk Level | Best Platform | Example |
|-----------|-----------|--------------|---------|
| Trending format adaptation | Low | X, IG, TikTok | Popular template + niche context |
| Industry insider joke | Medium | X, LinkedIn | Only your audience gets it — that's the point |
| Self-deprecating / BTS | Low | IG Stories, X | "How it started vs how it's going" |
| Relatable pain point | Low | All | "Every founder during fundraising" |
| Competitor jab | High | X | Funny but not mean; don't punch down |

## Procedure

1. **Identify the opportunity.** Is there a trending format (from `trend-monitor`)? An inside joke? A relatable pain point?

2. **Choose the format:**
   - Image macro: existing template + branded text overlay
   - Video/reaction: short clip with caption
   - Text-only: "Nobody: / Me:" style (X only, no visual needed)
   - Custom graphic: original visual designed around the joke

3. **Write the text overlay / caption:**
   - Setup line (top): sets up the scenario
   - Punchline (bottom): the relatable/surprising twist
   - 5-10 words per line maximum
   - Match brand humor style (dry, absurd, self-deprecating, playful)

4. **Adapt to each platform:**
   - X: text-first memes work; image macros with overlay
   - IG: visual-first, story-friendly
   - TikTok: video-based, green-screen or reaction format
   - LinkedIn: rare; only if brand personality is established there

5. **Run the cringe test:**
   - Would the founder feel good about this being their top post?
   - Is it funny TO the audience, or AT them?
   - If it flops, is it "oh well" or "delete account"?

6. **Specify visual execution:**
   - Template name (if existing) or visual description (if custom)
   - Dimensions per platform (delegate to `asset-format`)
   - Font and text placement

## Output Format

```markdown
# Meme Concept: [Title / Joke Premise]

## Context
**Meme type:** [Trending format / Industry joke / Self-deprecating / Pain point]
**Why now:** [Trend reference or timing reason]
**Platform:** [X / IG / TikTok / multi-platform]

## Concept
**Setup:** [What the audience sees first]
**Punchline:** [The relatable or surprising reveal]
**Brand connection:** [Why this fits the brand and niche]

## Text Overlay
- **Top text:** [Setup line]
- **Bottom text:** [Punchline]

## Caption
[Post text — context, additional joke layer, CTA]

## Format / Template
**Template name:** [e.g., "Distracted Boyfriend," custom]
**Dimensions:** [Per platform]

## Risk Assessment
**Cringe risk:** [Low / Medium / High]
**Founder comfort check:** [Would they post this?]
```

## Done Criteria

The skill is complete when:
1. Meme concept has a clear setup + punchline
2. Brand connection is authentic (not forced)
3. Risk assessment is documented
4. Text overlay and caption are written
5. Format and dimensions are specified per platform

## Pitfalls

- Forcing humor when the brand voice isn't naturally funny
- Using a template that peaked 2+ weeks ago (late is worse than absent)
- Memes requiring too much niche knowledge to be funny
- Not checking with the founder before posting edgy content

## Verification

The cringe test (step 5). Also: show the concept to one person outside the company who fits the target audience. Do they laugh or say "I don't get it"?

## Example

*Input:* SaaS analytics brand. Trending format: "Wait, it's all [X]?" + "Always has been." Pain point: founders obsessed with vanity metrics.

*Output:*
- Top text: "Wait, it's all DAU?"
- Bottom text: "Always has been." (subtitle: "meanwhile, your retention is 12%")
- Caption: "The hardest truth in analytics: the metric you're optimizing probably isn't the one that matters. Save this for your next board meeting when someone asks about DAU."
- Cringe risk: Low (relatable, punches up, doesn't make fun of the audience)
- Platform: X (text meme, no visual needed)
