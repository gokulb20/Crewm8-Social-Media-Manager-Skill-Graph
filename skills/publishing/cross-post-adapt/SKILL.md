---
name: cross-post-adapt
description: Adapt one piece of content into platform-native variants for X, LinkedIn, Instagram, and TikTok — no copy-paste. Each version feels purpose-built for its platform.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, publishing, cross-posting, platform-adaptation, multi-platform]
related_skills: [post-create, thread-create, caption-draft, schedule-queue, brand-voice-system]
inputs_required: [source-content, source-platform, target-platforms, core-message]
deliverables: [platform-native-adaptations-for-each-target]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Cross-Post Adapt

Transform a single content idea into platform-native posts that do NOT look like the same post copied four times. Each version earns its place on its platform.

## Purpose

Audiences follow brands across platforms. If they see the same post with different line breaks on X and LinkedIn, they feel like the brand doesn't respect the platform. This skill adapts the core message structurally and tonally for each platform so it feels native everywhere.

## When to Use

- Founder wrote one post and says "put this everywhere"
- Content calendar calls for the same topic across platforms
- Building a multi-platform campaign around one message

## Inputs Required

- Source content (text and format)
- Source platform
- Target platforms
- Core message (one sentence — the invariant)

## Quick Reference

| Source Format | X Adaptation | LinkedIn Adaptation | IG Adaptation | TikTok Adaptation |
|--------------|-------------|--------------------|--------------|-----------------|
| X thread (6-10) | (source) | Condense to 900-1200 char story post or carousel | Extract 1-2 insights as quote cards + caption | Extract 1 insight as video script (30-60s) |
| LinkedIn post | Condense to thread (4-6 tweets) | (source) | Pull key insight + visual | Pull 1 insight for ~30s video |
| IG caption | Extract strongest line as short post or mini-thread | Expand into 900-char story post | (source) | Turn into video script |
| TikTok script | Condense to short post or mini-thread | Expand to professional-framed post | Adapt to Reels format | (source) |

## Procedure

1. **Extract the core message** (one sentence — preserve this across all platforms).

2. **For each target platform, determine:**
   - Best format (thread, short post, carousel, video)
   - What needs to change structurally
   - What needs to change tonally

3. **Write each adaptation from scratch:**
   - Do NOT copy-paste and tweak
   - Preserve the core message but express it in the platform's native language
   - New hooks per platform
   - Platform-specific CTAs

4. **Check for copy-paste signals:**
   - Same hook across platforms
   - Same emoji patterns
   - Same paragraph structure
   - Same hashtag density

5. **Sequence cross-platform posting:**
   - Post to primary platform first
   - Wait 2-4 hours before adapted version on secondary platform
   - Adjust if primary version is performing exceptionally well

## Output Format

```markdown
# Cross-Post: [Core Message]

## Source
**Platform:** [Original]
**Format:** [Thread / Post / Caption / Script]
**Core message:** [One sentence]

---

## X Adaptation
**Format:** [Thread / Short post]
[Full content]
**Changes:** [What was restructured and why]

## LinkedIn Adaptation
**Format:** [Post / Carousel]
[Full content]
**Changes:** [What was restructured and why]

## Instagram Adaptation
**Format:** [Feed / Carousel / Reel / Story]
**Visual concept:** [What leads]
[Caption]
**Changes:** [What was restructured and why]

## TikTok Adaptation
**Format:** [Video script / N sec]
**Hook (first 1.5s):** [Text overlay + visual]
[Full script]
**Changes:** [What was restructured and why]

## Posting Sequence
1. [Platform] at [time] — primary
2. [Platform] at [time] — secondary (+ delay)
...
```

## Done Criteria

The skill is complete when:
1. Core message is preserved across all adaptations
2. Each adaptation has a unique hook
3. Each adaptation has a platform-appropriate CTA
4. No "copy-paste" signals exist between adaptations
5. Posting sequence with time spacing is specified

## Pitfalls

- "Changing line breaks and calling it adapted" — audiences on multiple platforms will see both
- Same CTA everywhere (LinkedIn wants "agree?" — TikTok wants "follow for part 2")
- Adapting a format that doesn't work on the target platform
- Posting all versions simultaneously (clone content feeds)

## Verification

Put the adaptations side by side. If you blocked out the platform label, could you tell which platform each was written for? If not, they're too similar.

## Example

*Input:* X thread (7 tweets): "Top 5 SaaS pricing mistakes founders make."

*LinkedIn adaptation:* Condense to 900-char LinkedIn post. Structure: hook → 5 mistakes in flowing narrative (not bullet list) → lesson → CTA. Tone: slightly more professional. Hashtags: 3 at end.

*IG adaptation:* Carousel format. Slide 1: Cover "5 pricing mistakes that kill growth." Slides 2-6: One mistake per slide + visual metaphor (graph, icon). Final slide: CTA + brand. Caption: "Which mistake have you made? Drop it in the comments."

*TikTok adaptation:* 60-second video. Hook: "I made this pricing mistake. Cost me $10K." Body: rapid-fire walkthrough of 5 mistakes with visual overlays. CTA: "Follow for part 2 — how to fix them."
