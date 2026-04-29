---
name: schedule-queue
description: Queue posts to scheduling tools (Buffer, Hypefury, native schedulers) with platform-specific formatting, optimized posting times, media attachments, and cross-platform coordination.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Publishing, Scheduling, Queue, Automation]
    related_skills: [content-calendar, cadence-timing, cross-post-adapt, draft-review, thread-structure]
---

# Schedule Queue

Take approved content and queue it to the right scheduling tool for the right platform at the right time. This skill bridges the gap between "content is written" and "content is live." It handles formatting, media attachment, timing optimization, and queue management.

## When to Use

- Weekly batch scheduling session (queue the whole week at once)
- Posts have been drafted and approved (passed `draft-review`)
- Content calendar is locked for the week
- Founder approved the queue and says "schedule it"
- Rebalancing a queue mid-week (move posts due to trending content)

## Quick Reference

| Scheduling Tool | Best For | Platform Support |
|----------------|---------|-----------------|
| Buffer | Multi-platform queue, team collaboration | X, LinkedIn, IG (limited), TikTok (limited) |
| Hypefury | X-focused with auto-plug, threads | X, LinkedIn, IG |
| Typefully | X threads, analytics, auto-plug | X, LinkedIn |
| Native schedulers | Platform-specific features | X (Media Studio), LinkedIn (native), IG (Meta Business Suite), TikTok (native) |
| Later | IG-first with visual planning | IG, TikTok, LinkedIn, X |

## Procedure

1. Gather all approved posts for the scheduling window:
   - Post text per platform (from `post-create`, `thread-create`, `caption-draft`)
   - Target platforms per post
   - Recommended posting times from `cadence-timing` skill
   - Media assets (images, videos, GIFs) — confirm they're formatted per `asset-format`
   - Any special rules (thread structure from `thread-structure`, auto-plug settings, link placement)

2. Assign each post to a specific time slot:
   - Match to best-practice times from `cadence-timing`
   - Check for collisions (two posts from same brand within 30 minutes on same platform — too close)
   - Ensure thread tweets are scheduled with correct spacing (1-2 minutes between tweets)
   - Leave buffer slots for reactive/trending content

3. Format content per platform before queuing:
   - X: character count (280), line breaks, no links in first tweet
   - LinkedIn: character-friendly formatting, 3-5 hashtags at end
   - IG: caption with first 2 lines optimized, hashtags in first comment or end
   - TikTok: caption short, no links, hashtags optimized for discovery

4. Attach media assets:
   - Confirm correct dimensions per platform (see `asset-format`)
   - Write alt-text for images (accessibility + SEO)
   - Set thumbnail for videos if custom needed
   - Verify video captions/subtitles are embedded or attached

5. Set auto-plug rules for applicable posts:
   - Threads: add link to first tweet after [X likes or Y minutes] threshold
   - Link-in-bio posts: ensure bio link is updated BEFORE the post goes live
   - Follow-up posts: schedule secondary posts that reference the main post (2 hours after)

6. Apply queue management rules:
   - Set queue to "stop at X posts" if the week is unusually heavy (avoid audience fatigue)
   - Enable "best time" slots where the scheduler picks the optimal time within a window
   - Set fallback times if a slot is empty (don't post nothing)

7. Provide the queue summary for a final review before hitting "schedule all."

## Output Format

```markdown
# Publishing Queue: [Week of Date]

## Queue Summary
- **Total posts:** [N] across all platforms
- **Scheduling tool:** [Buffer / Hypefury / etc.]
- **Scheduling window:** [Date range]
- **Flex slots reserved:** [N] for reactive content

## Queue by Platform

### X
| Time | Content | Type | Media | Auto-plug | Status |
|------|---------|------|-------|-----------|--------|
| Mon 9:00 AM | [Hook text truncated] | Thread (8 tweets) | Image tweet 3 | Link after 20 likes | Queued |
| Mon 1:00 PM | [Hook text truncated] | Short post | None | None | Queued |
...

### LinkedIn
| Time | Content | Type | Media | Notes | Status |
|------|---------|------|-------|-------|--------|
...

### Instagram
...

### TikTok
...

## Collision Check
[Any posts within 30 min of each other on same platform? Any thread spacing violations?]

## Bio Link Coordination
[Posts that require bio link to match — which link, when to update]

## Post-Schedule Actions
- [ ] Update bio link for [platform] at [time]
- [ ] Monitor auto-plug for [thread] — manually trigger if threshold not met in 2 hours
- [ ] Reply to first comment on each post within 30 minutes (algorithm boost)
```

## Pitfalls

- Scheduling threads with zero spacing (all tweets hit at once — looks broken)
- Forgetting to check media dimensions before scheduling (rejected by platform, queue stalls)
- Scheduling a post that links to a URL that isn't live yet
- Queue collision: two brands or handles posting on the same platform at nearly the same time
- Not updating bio link before a "link in bio" post goes live (dead link = lost traffic)
- Over-scheduling: 4 X posts in 3 hours (algorithm punishes, audience annoyed)

## Verification

Preview the queue in the scheduling tool (most have a calendar view). Does the week look balanced? Are there obvious gaps? Does every post have media attached if needed? Export the queue as a shareable calendar view for founder sign-off.
