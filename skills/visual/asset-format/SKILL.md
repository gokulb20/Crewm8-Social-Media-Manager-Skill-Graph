---
name: asset-format
description: Enforce platform-specific image and video dimensions — X 16:9, Instagram 4:5 or 1:1, LinkedIn 4:5, TikTok 9:16 — plus safe zones, resolution targets, and file format guidance.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Visual, Formatting, Dimensions, Platform-Specs]
    related_skills: [visual-plan, image-prompt, meme-create]
---

# Asset Format

Enforce correct dimensions, aspect ratios, and safe zones for every visual asset on every platform. Wrong dimensions mean cropped images, blurry posts, and a brand that looks amateur. This skill is the single source of truth for visual specs.

## When to Use

- Before exporting any image or video for social
- `visual-plan`, `meme-create`, or `image-prompt` needs dimension guidance
- Founder sends a raw image: "Can you format this for X?"
- Setting up design templates or Canva presets
- Auditing existing posts for formatting issues

## Quick Reference

### Image Dimensions

| Platform | Aspect Ratio | Resolution (px) | Best For |
|----------|-------------|-----------------|----------|
| X (feed image) | 16:9 | 1200x675 or 1600x900 | General posts, quote cards |
| X (card/link image) | 2:1 or 1.91:1 | 1200x628 | Link previews |
| Instagram feed (portrait) | 4:5 | 1080x1350 | Carousels, primary feed posts |
| Instagram feed (square) | 1:1 | 1080x1080 | General feed posts |
| Instagram Stories/Reels | 9:16 | 1080x1920 | Stories, Reels |
| LinkedIn feed | 4:5 or 1.91:1 | 1200x1500 (4:5) | Carousels, single images |
| LinkedIn banner | ~3.33:1 | 1584x396 | Profile header |
| TikTok | 9:16 | 1080x1920 | All TikTok videos |

### Video Dimensions (same ratios, different export settings)

| Platform | Aspect Ratio | Max Duration | Max File Size |
|----------|-------------|-------------|--------------|
| X video | 16:9 or 1:1 | 2:20 (premium: longer) | 512MB |
| Instagram Reels | 9:16 | 90 sec | 4GB |
| LinkedIn video | 16:9 or 1:1 | 10 min | 5GB |
| TikTok | 9:16 | 10 min (native) | Varies |

## Procedure

1. Start with the platform target and content type:
   - Feed post? Story? Banner? Thumbnail? Video? Carousel slide?

2. Select the correct dimensions from the Quick Reference table above.

3. Check safe zones:
   - X feed: image displays with rounded corners — keep critical content away from edges
   - Instagram feed: profile icon and UI elements overlay on bottom-left — avoid placing text there
   - LinkedIn: "see more" cut on long captions — first 2 lines of caption are visible, rest hidden
   - TikTok: captions, like button, and comment field overlay the right and bottom edges — keep text content in center 80%
   - All platforms: avoid bottom 10-15% for key content (UI elements, caption overlays)

4. Specify export settings:
   - Image: PNG for graphics with text (lossless), JPG for photos (quality 85-95%)
   - Video: MP4, H.264 codec, 30fps (or source FPS)
   - File size: optimize to stay under platform limits while maintaining quality

5. If the source asset is the wrong aspect ratio:
   - Note whether it needs cropping (and what to crop out)
   - Note whether it needs letterboxing/pillarboxing (avoid if possible — looks like an ad)
   - Note whether it needs to be extended with a background or blurred fill

6. Provide the format checklist for the exact asset type.

## Output Format

```markdown
# Asset Format: [Asset Name / Type]

## Platform: [X / LinkedIn / IG / TikTok]
## Content Type: [Feed post / Story / Banner / Carousel / Video]

### Specifications
- **Aspect ratio:** [e.g., 4:5]
- **Resolution:** [e.g., 1080x1350 px]
- **File format:** [PNG / JPG / MP4]
- **File size limit:** [Platform limit]

### Safe Zones
- **Top:** [N]px margin
- **Bottom:** [N]px margin (UI overlay risk)
- **Left:** [N]px margin
- **Right:** [N]px margin
- **Center safe area:** [Effective usable area dimensions]

### Source Asset Adjustment
[If source is different ratio — cropping instructions, extension notes]

### Export Settings
- **Format:** [PNG/JPG/MP4 with specific settings]
- **Color space:** sRGB (always for social)
- **Compression:** [Level or bitrate]
```

## Platform-Specific Dimension Rules

**X:**
- Feed images: 16:9 recommended. 1:1 and 4:5 also supported.
- Images display at 16:9 in timeline preview but expand to full aspect ratio on click.
- GIFs: max 5MB (animated) or 15MB (static).

**Instagram:**
- Feed: 4:5 (max vertical), 1:1 (square), 1.91:1 (max horizontal).
- Stories/Reels: always 9:16. Design for full-screen vertical.
- Carousels: all slides must share the same aspect ratio (first slide sets the ratio).

**LinkedIn:**
- Feed images: 1.91:1 to 4:5 supported. 4:5 recommended for carousels.
- PDF carousels: pages render as images, design at 8.5x11 or matching aspect ratio.
- Banner: exact 1584x396. Center content — edges may be cropped on mobile.

**TikTok:**
- Always 9:16 vertical. No exceptions.
- Text overlays: keep within center 80% of frame.
- Thumbnail: extracted from video frame or uploaded separately.

## Pitfalls

- Designing at the wrong aspect ratio and cropping out critical content
- Forgetting that platform UI overlays cover part of the image (safe zones matter)
- Exporting at too-low resolution (blurry on high-DPI screens)
- Exporting at too-high file size (platform compression will destroy quality — compress yourself for control)
- Carousels where slide 1 is a different ratio than slides 2-5 (Instagram rejects it)

## Verification

Preview the asset at its intended platform's display size (view it at ~30-50% of screen width to simulate feed view). Is text readable? Are key elements visible? Do any elements get cut off by platform UI? Export a test post (draft mode) and review on mobile.
