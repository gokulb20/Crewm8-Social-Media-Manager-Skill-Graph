---
name: visual-plan
description: Plan visual assets for social content — carousel slide-by-slide copy, banners, quote cards, mock demos — including layout specs, color/font guidance, and AI image prompt generation.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Visual, Carousels, Banners, Design-Planning]
    related_skills: [image-prompt, asset-format, meme-create, caption-draft]
---

# Visual Plan

Produce detailed visual asset specifications that a designer or AI image generator can execute. Every post that needs a visual gets a clear brief — slide-by-slide copy for carousels, layout descriptions, dimension specs, and color/font guidance.

## When to Use

- Content calendar calls for carousels, banners, quote cards, or graphics
- Repurposing blog content into LinkedIn/IG carousels
- Campaign requires consistent visual branding across posts
- Founder says "can you mock up what this would look like?"
- Preparing assets for a launch week

## Quick Reference

| Asset Type | Typical Slides/Layout | Best Platform | Dimension Target |
|-----------|----------------------|--------------|-----------------|
| Carousel | 5-10 slides | LinkedIn, IG | 4:5 (1080x1350) |
| Quote card | 1 image | X, LinkedIn, IG | 16:9 for X, 4:5 for IG/LinkedIn |
| Banner/Header | 1 image | LinkedIn, X | 1500x500 (LinkedIn), 1500x500 (X) |
| Infographic | 1 long image or 3-5 slides | LinkedIn, IG | 4:5 |
| Data/chart card | 1 image | X, LinkedIn | 16:9 or 1:1 |

## Procedure

1. Start with the content the visual will support:
   - What's the key message? (One sentence)
   - What's the emotional tone? (Serious, playful, urgent, calm, inspiring)
   - What action should the visual drive? (Stop scroll, save, share, click)

2. Choose the visual format:
   - Carousel: when content is sequential (step-by-step, list of insights, framework)
   - Single image: when content is one powerful statement/quote/stat
   - Banner: profile or event-related
   - Video thumbnail: for podcast clips, YouTube promotions

3. For carousels, draft slide-by-slide:
   - Slide 1 (cover): The hook. Title + visual that stops the scroll. No more than 10 words.
   - Slides 2 through N-1: One idea per slide. Mix text and supporting visuals.
   - Final slide: Summary + CTA + brand logo/handle.
   - Each slide: 15-25 words max (people swipe, they don't read essays)

4. For each slide/asset, specify:
   - The exact copy/text on that slide
   - Visual direction (what image, icon, or graphic should accompany the text)
   - Layout preference (text-heavy, image-heavy, split screen, centered)

5. Apply brand visual guidelines:
   - Color palette (background, text, accent colors)
   - Typography (headline font, body font, any styling)
   - Logo placement (consistent across slides)
   - Any pattern, gradient, or texture elements

6. Generate AI image prompts for any visual that needs AI generation (delegate to `image-prompt` skill for the actual syntax).

7. Specify exact dimensions using `asset-format` skill rules.

## Output Format

```markdown
# Visual Plan: [Asset Name / Campaign]

## Content Context
**Key message:** [One sentence]
**Tone:** [Emotional register]
**Goal:** [Stop scroll / Save / Share / Click / Follow]

## Format: [Carousel / Single image / Banner / Thumbnail]

### Slide-by-Slide (for carousels)

#### Slide 1 (Cover)
**Copy:** [Exact text — max 10 words]
**Visual:** [Description of image/graphic]
**Layout:** [Text-heavy / Split / Centered]
**Colors:** [Background + text + accent]

#### Slide 2
...

#### Final Slide
**Copy:** [CTA + brand handle/logo]
**Visual:** [Brand mark / Logo placement]

## Specifications
- **Dimensions:** [Exact pixel dimensions per platform]
- **Safe zones:** [Margins for text — avoid platform UI elements]
- **Font:** [Headline + body font names]
- **Color palette:** [Hex codes]

## AI Image Prompts
[For each visual element that needs AI generation — full prompt in image-prompt format]

## Designer Notes
[Any additional guidance, references to existing brand assets, inspiration links]
```

## Pitfalls

- Carousel slides with too much text (20+ words per slide — nobody reads it)
- Slide 1 that doesn't hook standalone (people see it in feed before they swipe)
- Inconsistent visual branding across slides (different fonts, colors, alignment)
- Forgetting the CTA on the final slide (carousel ends and reader just... swipes away)
- Planning a carousel the brand doesn't have visual capacity to execute (better a text thread than a bad carousel)
- Specifying dimensions incorrectly per platform (see `asset-format` skill)

## Verification

Look at slide 1 in isolation. Does it make you want to swipe? Does the sequence flow logically? Is the final slide satisfying? Can you picture exactly what each slide looks like from the description alone?
