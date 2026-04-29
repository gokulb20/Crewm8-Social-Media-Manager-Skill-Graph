---
name: image-prompt
description: Write precise AI image generation prompts for Midjourney, DALL-E, and Stable Diffusion/SDXL — with style references, composition guidance, and platform-appropriate aspect ratios.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, visual, image-generation, ai-art, prompts, creative]
related_skills: [visual-plan, asset-format, meme-create]
inputs_required: [visual-concept-description, style-direction, target-platform, ai-tool-preference]
deliverables: [generation-prompts-for-1-3-tools]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Image Prompt

Write precise, effective AI image generation prompts for any tool (Midjourney, DALL-E, SDXL). Describe visual concepts clearly so the generated image matches the brand's vision and platform requirements.

## Purpose

Most AI images look generic because the prompts are generic. "A cool tech image" produces random results. This skill structures prompts with subject, style, composition, lighting, and mood — producing images that look intentional, not accidental.

## When to Use

- Visual plan identified a need for an AI-generated image
- Creating hero images for blog posts or newsletters
- Generating backgrounds, textures, or abstract visuals for quote cards
- Iterating on a visual style until it matches brand aesthetic

## Inputs Required

- Subject (what the image depicts)
- Style direction (photorealistic, illustration, 3D render, abstract, minimalist)
- Mood / lighting (bright, moody, warm, cold, dramatic)
- Color palette (dominant colors or vibe)
- Target aspect ratio

## Quick Reference

| Tool | Prompt Structure | Key Parameters |
|------|-----------------|---------------|
| Midjourney | `[subject] + [style] + [composition] + [lighting] + [mood] --ar [ratio]` | `--ar 16:9`, `--style raw`, `--v 6` |
| DALL-E | Natural language, 1-4 sentences | No special syntax; avoid text |
| SDXL | `[subject], [style], [quality tags], [negatives]` | Negative prompt separate |

## Procedure

1. **Define the visual:**
   - Subject: main focus
   - Action/context: what's happening
   - Style: photorealistic, illustration, 3D render, abstract, minimalist
   - Mood/lighting: bright, moody, warm, cold, dramatic
   - Color palette: dominant colors or vibe

2. **Choose the generation tool:**
   - Midjourney: best for artistic, stylized, conceptual visuals
   - DALL-E: best for literal depictions, text in images (but avoid text), precise compositions
   - SDXL: best for photorealism and negative prompting

3. **Write the main prompt:**
   - Lead with the subject
   - Add style descriptors ("minimalist tech illustration, flat design, clean lines")
   - Add composition ("centered, plenty of negative space")
   - Add lighting/mood ("warm lighting, morning glow, editorial photography")
   - End with technical parameters (aspect ratio, version, style settings)

4. **Tool-specific notes:**
   - Midjourney: include `--ar [ratio]`, use `--style raw` for literal interpretations, `--no text` to avoid gibberish
   - DALL-E: natural language, be specific about what you DON'T want
   - SDXL: separate negative prompt for "text, watermark, blurry, low quality, distorted"

5. **Generate 2-3 prompt variations** for A/B comparison.

## Output Format

```markdown
# Image Prompt: [Visual Concept Name]

## Visual Description
[Plain-language description]

## Platform & Dimensions
**Platform:** [X / LinkedIn / IG / TikTok / multi-use]
**Aspect ratio:** [16:9 / 4:5 / 1:1 / 9:16]

## Primary Prompt (Midjourney)
```
[Full Midjourney prompt with parameters]
```

## DALL-E Prompt
```
[Natural language DALL-E prompt]
```

## SDXL Prompt
**Positive:** [SDXL positive prompt + quality tags]
**Negative:** [SDXL negative prompt]

## Style References
- Mood board keywords: [style references]
```

## Done Criteria

The skill is complete when:
1. Prompt includes subject, style, composition, lighting, and mood
2. Aspect ratio matches the target platform
3. Tool-specific syntax is correct (no Midjourney parameters in DALL-E prompts)
4. 1-2 alternate prompts are provided for comparison
5. Negative prompt is provided (for SDXL) or "no text" instruction (for Midjourney/DALL-E)

## Pitfalls

- Vague prompts ("a cool tech image") — results will be random
- Contradictory prompts ("minimalist but also highly detailed and complex")
- Forgetting aspect ratio (image may come back at wrong dimensions)
- AI-generated text in images (use `--no text` or negative prompt)
- Using copyrighted artist names — stick to style movements and descriptors

## Verification

Does the prompt describe exactly what you want? If you handed it to a human illustrator, would they produce what you're imagining? Does the aspect ratio match the platform requirement?

## Example

*Input:* Quote card background for X (16:9). Topic: cold outreach. Mood: professional, warm, editorial. Brand colors: dark gray + orange.

*Output (Midjourney):*
```
A minimalist workspace flat lay from above — laptop, coffee cup, notebook with handwritten notes, soft natural window lighting, warm earth tones with orange accents, deep gray background, editorial photography style, negative space around top and bottom for text overlay --ar 16:9 --style raw --v 6 --no text, watermark, people
```

*DALL-E version:*
"A top-down flat lay photograph of a desk workspace: a laptop, a coffee cup, and a notebook with handwritten notes. Soft natural window lighting, warm earth tones with orange accents against a dark gray background. Minimalist, editorial style. The top and bottom thirds of the image should be empty space suitable for text overlay. No people, no text in the image."
