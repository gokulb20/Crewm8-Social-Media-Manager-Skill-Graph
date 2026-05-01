---
name: schedule-queue
description: Queue approved posts to scheduling tools (Buffer, Hypefury, Typefully, native schedulers) with platform-specific formatting, optimized posting times, media attachments, and cross-platform coordination.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, publishing, scheduling, queue, automation, workflow]
related_skills: [content-calendar, cadence-timing, cross-post-adapt, draft-review, thread-structure]
inputs_required: [approved-posts-per-platform, posting-times, media-assets, scheduling-tool]
deliverables: [publishing-queue-ready-to-schedule]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: ["BUFFER_API_KEY"]
required_env_vars: ["BUFFER_API_KEY"]
---

# Schedule Queue

Take approved content and queue it to the right scheduling tool for the right platform at the right time. This skill bridges "content is written" and "content is live."

## Purpose

The gap between content creation and publishing is where most social strategies die. This skill eliminates that gap by handling formatting, media attachment, timing optimization, and queue management — so all that's left is clicking "schedule all."

## When to Use

- Weekly batch scheduling session
- Posts drafted and approved (passed `draft-review`)
- Content calendar is locked
- Founder approved the queue
- Rebalancing a queue mid-week

## Inputs Required

- Approved posts per platform (text, formatted)
- Target posting times per platform (from `cadence-timing`)
- Media assets per post (images, videos, GIFs)
- Scheduling tool (Buffer, Hypefury, Typefully, native — or any equivalent)
- Auto-plug rules for threads
- Bio link update schedule

## Quick Reference

| Scheduling Tool | Best For | Platform Support |
|----------------|---------|-----------------|
| Buffer | Multi-platform queue, team collaboration | X, LinkedIn, IG (limited), TikTok (limited) |
| Hypefury | X-focused with auto-plug, threads | X, LinkedIn, IG |
| Typefully | X threads, analytics, auto-plug | X, LinkedIn |
| Native schedulers | Platform-specific features | X (Media Studio), LinkedIn (native), IG (Meta Business Suite), TikTok (native) |
| Later | IG-first with visual planning | IG, TikTok, LinkedIn, X |

## Procedure

1. **Gather all approved posts** for the scheduling window:
   - Post text per platform
   - Target platforms
   - Recommended posting times
   - Media assets (formatted per `asset-format`)
   - Special rules (thread structure, auto-plug settings)

2. **Assign each post to a time slot:**
   - Match `cadence-timing` best times
   - Check for collisions (two posts same platform within 30 min — too close)
   - Space thread tweets 1-2 minutes apart

3. **Format content per platform before queuing:**
   - X: character count verified, links only in final tweet or reply
   - LinkedIn: 3-5 hashtags at end
   - IG: first 2 lines optimized, hashtags in first comment or end of caption
   - TikTok: caption short, no links

4. **Attach media assets:**
   - Confirm correct dimensions
   - Write alt-text for accessibility
   - Set thumbnail for video if custom needed
   - Verify captions/subtitles embedded

5. **Set auto-plug rules:**
   - Threads: add link to tweet 1 after [X likes or Y minutes]
   - Link-in-bio posts: ensure bio link is updated BEFORE post goes live

6. **Set queue management:**
   - Maximum posts per day per platform to avoid fatigue
   - Fallback times if a slot is empty

## Output Format

```markdown
# Publishing Queue: [Week of Date]

## Queue Summary
- **Total posts:** [N] across platforms
- **Scheduling tool:** [Tool name]
- **Window:** [Date range]
- **Flex slots reserved:** [N]

## Queue by Platform

### X
| Time | Content | Type | Media | Auto-plug | Status |
|------|---------|------|-------|-----------|--------|
| Mon 9:00 AM | [Hook truncated] | Thread (8 tweets) | Image tweet 3 | Link after 20 likes | Queued |
...

### LinkedIn / Instagram / TikTok
[Same structure per platform]

## Collision Check
[Any posts within 30 min of each other?]

## Bio Link Coordination
[Posts that require bio link updates — when to update]
```

## Done Criteria

The skill is complete when:
1. Every approved post has a time slot
2. No platform collisions exist
3. All media is attached and correctly formatted
4. Auto-plug rules are configured
5. Bio link coordination is documented
6. Queue is ready for the "schedule all" action

## Pitfalls

- Scheduling threads with zero spacing (unfolds as one block)
- Forgetting to check media dimensions (queue stalls when platform rejects it)
- Scheduling a post linking to a URL that isn't live yet
- Not updating bio link before "link in bio" post goes live

## Verification

Preview the queue in the scheduling tool's calendar view. Does the week look balanced? Does every post have media if needed? Does every thread have correct tweet spacing?
