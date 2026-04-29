---
name: meme-create
description: Create platform-relevant meme concepts adapted to the brand voice — with text overlay, format reference, and posting context — for X, Instagram, and TikTok.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Visual, Memes, Humor, Engagement]
    related_skills: [brand-voice-system, visual-plan, image-prompt, asset-format]
---

# Meme Create

Design branded meme concepts that feel native to the platform and authentic to the brand. Memes are high-risk, high-reward — done right they're the most shared content type; done wrong they signal that a brand is trying too hard.

## When to Use

- Trending meme format circulating that's relevant to the niche
- Low-engagement period (memes can juice the algorithm)
- Community inside joke has emerged (meme solidifies it)
- Competitor just posted something too serious (counter with humor)
- Product or industry pain point that's universally relatable

## Quick Reference

| Meme Type | Risk Level | Best Platform | Example Context |
|-----------|-----------|--------------|----------------|
| Trending format adaptation | Low | X, IG, TikTok | Take a popular template, apply niche context |
| Industry insider joke | Medium | X, LinkedIn | Only your target audience will get it — that's the point |
| Self-deprecating / BTS | Low | IG Stories, X | "How it started vs how it's going" with real moments |
| Competitor jab | High | X | Funny but not mean; don't punch down |
| Relatable pain point | Low | All | "Every founder during fundraising" type beats |

## Procedure

1. Identify the meme opportunity:
   - Is there a trending format right now? (check `trend-monitor` skill output)
   - Is there a community joke or shared pain point worth meme-ifying?
   - Is the founder willing to be a little less polished for this one?

2. Choose the meme format:
   - Image macro: existing template + branded text overlay
   - Video/reaction: short clip with caption/timing
   - Text-only format: "Nobody: / Me:" style posts work on X without visuals
   - Custom graphic: original visual designed around the joke

3. Write the text overlay / caption:
   - Setup line (top): sets up the scenario
   - Punchline (bottom): the relatable/surprising twist
   - Keep text short — 5-10 words per line maximum
   - Match the brand's humor style (dry, absurdist, self-deprecating, playful)

4. Adapt to each platform:
   - X: text-first memes work (no visual needed); image macros with overlay
   - IG: visual-first, story-friendly format preferred
   - TikTok: video-based, green-screen or reaction format
   - LinkedIn: much rarer; only if the brand has an established "personality" there. Skip if unsure.

5. Run the "cringe test":
   - Would the founder feel good about this being the top post on their profile?
   - Is this funny TO the audience, or AT them?
   - If the meme flops, is it "oh well" or "delete account" level? Avoid the latter.

6. Specify visual execution:
   - If using an existing template: name the template so a designer can find it
   - If creating from scratch: describe the visual + reference any inspiration
   - Dimensions per platform (delegate to `asset-format`)

7. Determine timing:
   - Memes tied to trends: post within 24 hours of trend peak
   - Evergreen memes: post during historically low-engagement windows as an algorithm bump

## Output Format

```markdown
# Meme Concept: [Title / Joke Premise]

## Context
**Meme type:** [Trending format / Industry joke / Self-deprecating / Pain point]
**Why now:** [Trend reference or timing reason]
**Platform:** [X / IG / TikTok / multi-platform]

## Concept
**Setup:** [Text or visual description — what the audience sees first]
**Punchline / Twist:** [The relatable or surprising reveal]
**Brand connection:** [Why this fits the brand's voice and niche]

## Text Overlay (for visual memes)
- **Top text:** [Short setup line]
- **Bottom text:** [Punchline]

## Caption
[The text that accompanies the meme post — context, additional joke layer, or CTA]

## Format / Template Reference
- **Template name:** [e.g., "Distracted Boyfriend," "Drake Hotline Bling," custom]
- **Visual description:** [What the image/video should look like if not using an existing template]
- **Dimensions:** [Per platform]

## Risk Assessment
**Cringe risk:** [Low / Medium / High]
**Founder comfort check:** [Would they post this? If unsure, flag for approval.]
**Backup plan:** [If engagement is bad, what's the next post to recover?]

## Posting Context
**Best window:** [Trending window or low-engagement bump slot]
**Cross-platform:** [Adaptation notes if posting to multiple platforms]
```

## Pitfalls

- Forcing humor when the brand voice isn't naturally funny (serious brands doing memes = cringe)
- Using a template that peaked 2 weeks ago (late to the party is worse than not showing up)
- Memes that require too much niche knowledge (if 90% of followers don't get it, it's a wasted post)
- Inside jokes that feel exclusionary rather than community-building
- Not checking with the founder before posting an edgy meme (surprise cringe is worse than approved cringe)

## Verification

The cringe test (see step 5 above). Also: show the meme concept to one person outside the company who fits the target audience. Do they laugh or do they say "I don't get it"? If the latter, scrap it or simplify.
