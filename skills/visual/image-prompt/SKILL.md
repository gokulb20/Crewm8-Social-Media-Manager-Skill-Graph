---
name: image-prompt
description: Write AI image prompts for Midjourney, DALL-E, and Stable Diffusion/SDXL with style references, composition guidance, and platform-appropriate aspect ratios.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Visual, Image-Generation, AI-Art, Prompts]
    related_skills: [visual-plan, asset-format, meme-create]
---

# Image Prompt

Write precise, effective AI image generation prompts for any tool (Midjourney, DALL-E, SDXL). Describe visual concepts clearly so the generated image matches the brand's vision and platform requirements.

## When to Use

- `visual-plan` or `meme-create` identified a need for an AI-generated image
- Founder needs a visual concept described for a designer
- Creating hero images for blog posts or newsletters
- Generating background images, textures, or abstract visuals for quote cards
- Iterating on a visual style until it matches brand aesthetic

## Quick Reference

| Tool | Prompt Structure | Key Parameters |
|------|-----------------|---------------|
| Midjourney | `[subject] + [style descriptors] + [composition] + [lighting] + [mood] --ar [ratio]` | `--ar 16:9`, `--style raw`, `--v 6` |
| DALL-E | Natural language description, 1-4 sentences | No special syntax needed |
| SDXL | `[subject], [style], [quality tags], [negatives]` | Negative prompt separate |

## Procedure

1. Define exactly what the image needs to depict:
   - Subject: what is the main focus?
   - Action/context: what's happening?
   - Style: photorealistic, illustration, 3D render, abstract, minimalist?
   - Mood/lighting: bright, moody, warm, cold, dramatic?
   - Color palette: dominant colors or vibe?

2. Choose the generation tool based on what you need:
   - Midjourney: best for artistic, stylized, or conceptual visuals
   - DALL-E: best for literal depictions, text in images, precise compositions
   - SDXL: best for photorealism and when you need negative prompts

3. Write the main prompt:
   - Lead with the subject
   - Add style descriptors (e.g., "minimalist tech illustration, flat design, clean lines")
   - Add composition notes (e.g., "centered composition, plenty of negative space")
   - Add lighting/mood (e.g., "warm lighting, morning glow, editorial photography")
   - End with technical parameters (aspect ratio, version, style settings)

4. For Midjourney specifically:
   - Include aspect ratio: `--ar 16:9` for X, `--ar 4:5` for IG/LinkedIn, `--ar 9:16` for TikTok
   - Use `--style raw` for more literal interpretations
   - Use `--no text` to avoid AI-generated gibberish text in images
   - Add `--stylize` or `--chaos` for creative variation if desired

5. For DALL-E specifically:
   - Natural language works best, no special syntax
   - Be specific about what you DON'T want (e.g., "no text, no watermarks")
   - Works well with style references: "in the style of [artist/movement]" (as long as it's public domain/generic)

6. For SDXL specifically:
   - Write a separate negative prompt: "text, watermark, blurry, low quality, distorted faces"
   - Include quality booster tags: "8k, highly detailed, sharp focus, professional"

7. Generate 2-3 prompt variations for A/B comparison if possible.

## Output Format

```markdown
# Image Prompt: [Visual Concept Name]

## Visual Description
[Plain-language description of what the image should look like]

## Platform & Dimensions
**Platform:** [X / LinkedIn / IG / TikTok / multi-use]
**Aspect ratio:** [16:9 / 4:5 / 1:1 / 9:16]
**Resolution target:** [e.g., 1920x1080 for 16:9]

## Primary Prompt (Midjourney)
```
[Full Midjourney prompt with parameters]
```

## DALL-E Prompt
```
[Natural language DALL-E prompt]
```

## SDXL Prompt
**Positive:**
```
[SDXL positive prompt + quality tags]
```
**Negative:**
```
[SDXL negative prompt]
```

## Style References
- **Mood board keywords:** [e.g., "editorial tech photography, Stripe-style illustration"]
- **Reference images:** [Links or descriptions of reference images]

## Notes
[Any specific requirements: no humans, must match existing brand visuals, font-safe areas, etc.]
```

## Pitfalls

- Prompts that are too vague ("a cool tech image") — results will be random
- Prompts that are too specific and contradictory ("minimalist but also highly detailed and complex")
- Forgetting to specify aspect ratio (image may come back at wrong dimensions)
- AI-generated text within images (almost always looks bad — use `--no text` or "no text" in negative)
- Using artist names that may be copyright-protected — stick to style movements and generic descriptors
- Not checking that the generated image's subject matches the post content

## Verification

Does the prompt describe exactly what you want, or does it leave room for the AI to interpret? (Some room is good. Ambiguity about the main subject is not.) If you handed this prompt to a human illustrator, would they produce what you're imagining?
