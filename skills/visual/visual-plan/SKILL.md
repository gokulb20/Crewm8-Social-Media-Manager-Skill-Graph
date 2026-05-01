---
name: visual-plan
description: Plan visual assets for social content — carousel slide-by-slide copy, banners, quote cards, and mock demos — including layout specs, color/font guidance, and AI image prompt generation.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, visual, carousels, banners, design-planning, creative]
related_skills: [image-prompt, asset-format, meme-create, caption-draft, post-create]
inputs_required: [content-message, brand-visual-guidelines, target-platform, asset-type]
deliverables: [visual-brief-with-slide-by-slide-copy-and-dimensions]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: []
required_env_vars: []
---

# Visual Plan

Produce detailed visual asset specifications that a designer or AI image generator can execute. Every post that needs a visual gets a clear brief — slide-by-slide copy for carousels, layout descriptions, dimension specs, and color/font guidance.

## Purpose

Most social visuals fail because nobody planned them. The text doesn't fit, the layout doesn't work for the platform, or the visual doesn't support the message. This skill produces a plan that removes all ambiguity before a single pixel is created.

## When to Use

- Content calendar calls for carousels, banners, quote cards, or graphics
- Repurposing blog content into LinkedIn/IG carousels
- Campaign requires consistent visual branding
- Founder says "can you mock up what this would look like?"

## Inputs Required

- Key message (one sentence)
- Tone (serious, playful, urgent, calm, inspiring)
- Brand visual guidelines (colors, fonts, logo)
- Target platform
- Content format (carousel, single image, banner, video thumbnail)

## Quick Reference

| Asset Type | Typical Slides | Best Platforms | Dimension Target |
|-----------|---------------|--------------|-----------------|
| Carousel | 5-10 slides | LinkedIn, IG | 4:5 (1080x1350) |
| Quote card | 1 image | X, LinkedIn, IG | 16:9 for X, 4:5 for IG/LinkedIn |
| Banner/Header | 1 image | LinkedIn, X | 1500x500 (LinkedIn), 1500x500 (X) |
| Infographic | 1 long image or 3-5 slides | LinkedIn, IG | 4:5 |
| Data/chart card | 1 image | X, LinkedIn | 16:9 or 1:1 |

## Procedure

1. **Define the content context:**
   - Key message (one sentence)
   - Emotional tone
   - Action the visual should drive (stop scroll, save, share, click)

2. **Choose the format:**
   - Carousel: when content is sequential (step-by-step, list of insights, framework)
   - Single image: one powerful statement/quote/stat
   - Banner: profile or event-related visual

3. **For carousels, draft slide-by-slide:**
   - Slide 1 (cover): Hook + visual that stops scroll. Max 10 words.
   - Slides 2-N-1: One idea per slide. Mix text and supporting visual.
   - Final slide: Summary + CTA + brand logo/handle.
   - Each slide: 15-25 words max

4. **For each slide, specify:**
   - Exact copy
   - Visual direction (image, icon, or graphic)
   - Layout (text-heavy, image-heavy, split screen, centered)

5. **Apply brand guidelines:**
   - Color palette (background, text, accent)
   - Typography (headline font, body font)
   - Logo placement (consistent)

6. **Generate AI image prompts** for any AI-generated visuals (delegate to `image-prompt`).

7. **Specify exact dimensions** using `asset-format` rules.

## Output Format

```markdown
# Visual Plan: [Asset Name]

## Content Context
**Key message:** [One sentence]
**Tone:** [Emotional register]
**Goal:** [Stop scroll / Save / Share / Click]

## Format: [Carousel / Single image / Banner / Thumbnail]

### Slide-by-Slide (for carousels)

#### Slide 1 (Cover)
**Copy:** [Exact text — max 10 words]
**Visual:** [Image/graphic description]
**Layout:** [Text-heavy / Split / Centered]
**Colors:** [Background + text + accent]

#### Slide 2...
...

### Specifications
- **Dimensions:** [Exact pixel dimensions]
- **Safe zones:** [Margins — avoid platform UI]
- **Font:** [Headline + body]
- **Color palette:** [Hex codes]
```

## Done Criteria

The skill is complete when:
1. All slides have exact copy, visual direction, and layout
2. Dimensions match the target platform specification
3. Brand colors and fonts are specified
4. AI image prompts are provided (if AI generation is involved)
5. The visual brief is detailed enough for a designer or AI to execute without clarification

## Pitfalls

- Carousel slides with too much text (20+ words per slide — nobody reads them)
- Slide 1 that doesn't hook standalone (people see it in feed before they swipe)
- Inconsistent visual branding across slides
- Forgetting CTA on the final slide
- Specifying wrong dimensions per platform (see `asset-format`)

## Verification

Look at slide 1 in isolation — does it make you want to swipe? Does the sequence flow logically? Is the final slide satisfying? Can you picture exactly what each slide looks like from the description?

## Example

*Input:* Topic = "3 signs your pricing is wrong." Tone = confident, slightly provocative. Platform = LinkedIn carousel. Brand = dark background (gray/black), white text, orange accent.

*Output:* 6-slide carousel.
- Slide 1: "3 signs your pricing is wrong" (large text, centered, orange accent underline). Visual: subtle question mark icon.
- Slide 2: "Sign 1: You've never raised prices" — copy: "If your prices are the same as 2 years ago, you're leaving money on the table." Visual: declining graph.
- Slide 3-5: Same structure for remaining signs.
- Slide 6: "Which sign hit closest? Drop it in the comments. → Follow for more pricing breakdowns." Visual: brand mark, orange accent.
- Dimensions: 1080x1350 (4:5, LinkedIn). Font: Inter Bold for headers, Inter Regular for body. Colors: background #1a1a1a, text #ffffff, accent #ff6b35.
