---
name: asset-format
description: Enforce platform-specific image and video dimensions — X 16:9, Instagram 4:5 or 1:1, LinkedIn 4:5, TikTok 9:16 — plus safe zones, resolution targets, and file format guidance.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, visual, formatting, dimensions, platform-specs, technical]
related_skills: [visual-plan, image-prompt, meme-create]
inputs_required: [target-platform, content-type, source-asset-info-if-resizing]
deliverables: [asset-format-spec-with-dimensions-and-safe-zones]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Asset Format

Enforce correct dimensions, aspect ratios, and safe zones for every visual asset on every platform. Wrong dimensions mean cropped images, blurry posts, and a brand that looks amateur. This skill is the single source of truth for visual specs.

## Purpose

Every platform displays images differently. The same image that looks perfect on X gets cropped badly on LinkedIn. This skill eliminates guesswork by providing exact specs per platform, content type, and asset format — so every visual lands correctly.

## When to Use

- Before exporting any image or video for social
- Visual plan, meme, or image prompt needs dimension guidance
- Founder sends a raw image: "Format this for X"
- Auditing existing posts for formatting issues

## Inputs Required

- Target platform
- Content type (feed post, story, banner, carousel, video, link preview)
- Source asset dimensions (if resizing an existing image)

## Quick Reference

### Image Dimensions

| Platform | Aspect Ratio | Resolution | Best For |
|----------|-------------|-----------|----------|
| X (feed) | 16:9 | 1200x675 or 1600x900 | General posts, quote cards |
| X (link preview) | 1.91:1 | 1200x628 | Link preview cards |
| IG Feed (portrait) | 4:5 | 1080x1350 | Carousels, primary posts |
| IG Feed (square) | 1:1 | 1080x1080 | General feed posts |
| IG Stories / Reels | 9:16 | 1080x1920 | Stories, Reels |
| LinkedIn Feed | 4:5 or 1.91:1 | 1200x1500 (4:5) | Carousels, single images |
| LinkedIn Banner | ~3.33:1 | 1584x396 | Profile header |
| TikTok | 9:16 | 1080x1920 | All videos |

### Video Specifications

| Platform | Aspect Ratio | Max Duration | Max Size | Codec |
|----------|-------------|-------------|---------|-------|
| X video | 16:9 or 1:1 | 2:20 (premium longer) | 512MB | H.264 |
| IG Reels | 9:16 | 90 sec | 4GB | H.264 |
| LinkedIn video | 16:9 or 1:1 | 10 min | 5GB | H.264 |
| TikTok | 9:16 | 10 min | Varies | H.264 |

## Procedure

1. **Identify the platform and content type.** Feed post? Story? Banner? Carousel? Video? Thumbnail?

2. **Select dimensions from the Quick Reference table.**

3. **Check safe zones:**
   - X feed: rounded corners — keep critical content away from edges
   - IG feed: profile icon + UI elements overlay bottom-left — avoid text there
   - LinkedIn: "see more" cut — first 2 caption lines matter most
   - TikTok: UI (likes, comments) overlays right and bottom edges — keep content in center 80%
   - All platforms: avoid bottom 10-15% for key content

4. **Specify export settings:**
   - Image: PNG for graphics with text (lossless), JPG for photos (quality 85-95%)
   - Video: MP4, H.264, 30fps, captions embedded

5. **If source asset is wrong aspect ratio:**
   - Recommend cropping (specify what to crop)
   - Or extending with blurred background fill

6. **Provide the format checklist** for the exact asset type.

## Output Format

```markdown
# Asset Format: [Asset Name]

## Platform: [X / LinkedIn / IG / TikTok]
## Content Type: [Feed / Story / Banner / Carousel / Video]

### Specifications
- **Aspect ratio:** [e.g., 4:5]
- **Resolution:** [e.g., 1080x1350 px]
- **File format:** [PNG / JPG / MP4]
- **File size limit:** [Platform max]

### Safe Zones
- **Top:** [N]px margin
- **Bottom:** [N]px margin (UI overlay risk)
- **Left:** [N]px margin
- **Right:** [N]px margin
- **Center safe area:** [Effective usable area]

### Source Asset Adjustment
[Cropping/extension notes if source is different ratio]

### Export Settings
- **Format:** [PNG/JPG/MP4 settings]
- **Color space:** sRGB
- **Compression:** [Level or bitrate]
```

## Done Criteria

The skill is complete when:
1. Dimensions match the target platform and content type
2. Safe zones are documented (including platform UI overlays)
3. File format and export settings are specified
4. Any source asset adjustments are stated (crop, extension, fill)

## Pitfalls

- Designing at the wrong aspect ratio and cropping critical content
- Forgetting platform UI overlays cover part of the image
- Exporting at too-low resolution (blurry on high-DPI screens)
- Exporting at too-high file size (platform compression destroys quality)
- Carousels where slide 1 has a different ratio than slides 2-5 (platform rejects it)

## Verification

Preview at platform display size (30-50% of screen width to simulate feed view). Is text readable? Are key elements in the safe zone? Export a test post in draft mode and review on mobile.

## Example

*Input:* LinkedIn carousel. 6 slides. Source text: "3 signs your pricing is wrong."

*Output:*
- Aspect ratio: 4:5
- Resolution: 1200x1500 px per slide
- Format: PNG (graphics with text)
- Safe zones: top 10% + bottom 15% clear (LinkedIn UI + action buttons overlay the bottom)
- Center safe area: 75% of image height — put all text here
- Export: sRGB, PNG-24
- All 6 slides must share the same 4:5 ratio
