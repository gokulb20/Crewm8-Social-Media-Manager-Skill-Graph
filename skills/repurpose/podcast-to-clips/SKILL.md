---
name: podcast-to-clips
description: Extract podcast episode transcripts into quote tweets, Instagram Reels copy, LinkedIn highlight posts, and TikTok script hooks — turning 60-minute conversations into 5-8 social assets.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, repurpose, podcast, clips, multi-platform, content-bank]
related_skills: [post-create, caption-draft, visual-plan, newsletter-to-posts]
inputs_required: [podcast-or-interview-transcript, full-episode-url, guest-handle-or-bio]
deliverables: [clip-inventory-with-posting-schedule]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: ["FIRECRAWL_API_KEY"]
required_env_vars: ["FIRECRAWL_API_KEY"]
---

# Podcast to Clips

Distill podcast and video interview transcripts into platform-native social assets. A single 60-minute episode should yield 5-8 posts across platforms, not just one "new episode out" announcement.

## Purpose

Podcasts are a content goldmine that most brands under-leverage. Each episode contains 5-8 moments worth posting. This skill extracts them, formats them per platform, and sequences the clips so one episode feeds a week of content.

## When to Use

- New podcast episode published
- Founder was a guest on someone else's podcast
- Older episode that performed well deserves a second push
- Building a clips library for ongoing content

## Inputs Required

- Full podcast transcript (auto-generated is fine)
- Episode title, host/guest handles, episode URL
- Brand voice guide
- Any specific clips the founder wants to highlight

## Quick Reference

| Podcast Segment | Best Clip Format | Best Platform |
|----------------|-----------------|--------------|
| Hot take / contrarian opinion | Quote tweet or text-over-video | X, TikTok |
| Data point or surprising stat | Quote card + stat-led post | X, LinkedIn |
| Personal story | Video clip (30-60s) + caption | IG, TikTok |
| Framework or system | Carousel or thread | LinkedIn, X |
| Practical tip / how-to | Short video (15-30s) or text post | TikTok, IG, X |

## Procedure

1. **Read the full transcript.** Timestamp every moment that:
   - Made you pause or think differently
   - Contained a specific number or data point
   - Told a concrete story
   - Stated something contrarian or controversial
   - Offered a framework or step-by-step process
   - Was genuinely funny or human

2. **For each timestamped moment, determine the best format:**
   - Quote tweet: exact quote + 1-2 lines of context
   - Video clip: exact time range (15-90 seconds), text overlay hook
   - Carousel/post: if it's a framework, draft slide structure
   - Thread: if connected insights, build 3-5 tweet mini-thread

3. **For video clips:**
   - Clip length: 15-30s for TikTok/Reels, 30-90s for X, 60s max for LinkedIn
   - Include captions/subtitles
   - Write text overlay hook for first 1.5 seconds
   - Write platform-native caption

4. **For each clip, draft:** hook, caption/body text, CTA, hashtags.

5. **Organize clips into a posting schedule:**
   - Best clip first (within 24h of episode drop)
   - Spread remaining clips across 5-7 days
   - Do not post all clips the same day

6. **Include attribution.** Tag the host's account (if guesting). Link to full episode in every clip's caption or final tweet.

## Output Format

```markdown
# Podcast Clips: [Episode Title]

## Source
[Episode link + timestamp]

## Clip Inventory

### Clip 1: [Topic]
**Timestamp:** [MM:SS - MM:SS]
**Format:** [Video clip / Quote tweet / Thread / Carousel]
**Platform:** [Primary + secondary]
**Hook / Text overlay:** [Text]
**Caption / Body:** [Full text]
**CTA:** [CTA]
**Hashtags:** [Platform-appropriate set]

### Clip 2...
...

## Posting Schedule
- Day 1: [Clip X on platform Y]
- Day 2: [Clip X on platform Y]
...
```

## Done Criteria

The skill is complete when:
1. At least 5 clips are extracted per 60-minute episode
2. Each clip has a timestamp, format, platform assignment, and caption
3. Video clips specify time ranges and text overlay hooks
4. A posting schedule spaces clips across at least 5 days
5. All clips include attribution links

## Pitfalls

- Clips the host finds interesting but the audience doesn't
- Video clips without captions/subtitles (unwatchable for most consumption)
- Posting all clips at once (floods feed, reduces per-clip engagement)
- Same caption for every clip ("new episode out!") instead of clip-specific hooks
- Clips that require full-episode context to make sense

## Verification

For each clip: if you saw this in your feed without knowing the podcast, would it make sense? If the hook is "new episode" — rewrite to a content-first hook.

## Example

*Input:* 60-minute podcast episode. Founder guests on "The B2B Growth Show." Topic: cold outreach strategies.

*Extracted clips:*
1. (Quote tweet) Timestamp 12:30 — "Most cold outreach is lazy, it's not broken." Format: quote tweet. Platform: X.
2. (Framework) Timestamp 24:00 — "The 3-question qualification framework." Format: carousel. Platform: LinkedIn.
3. (Story) Timestamp 38:00 — "How one cold email led to a $50K deal." Format: video clip (45s). Platform: IG + TikTok.
4. (Data point) Timestamp 51:00 — "Open rates dropped 40% when we made this one change." Format: stat-led post. Platform: X.
5. (Tip) Timestamp 55:00 — "The exact DM template that books meetings." Format: short video (20s). Platform: TikTok.
