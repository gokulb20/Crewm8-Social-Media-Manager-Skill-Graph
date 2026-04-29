---
name: thread-structure
description: Manage X thread structures — hook tweet first, proper sequencing, auto-plug link timing (after X likes or Y minutes), visual placement, and cross-tweet flow.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Publishing, Threads, Structure, Auto-Plug]
    related_skills: [thread-create, schedule-queue, cta-craft]
---

# Thread Structure

Structure X threads for maximum readability, engagement, and algorithmic performance. Handles tweet sequencing, auto-plug timing, link placement rules, visual positioning, and the technical details that make threads work (or break them).

## When to Use

- Converting a drafted thread into a scheduled/publishable sequence
- Setting auto-plug rules for link insertion after engagement threshold
- Thread flow feels off — diagnosing structural issues
- Multi-part threads (part 1, part 2 over multiple days)
- Thread with multiple media assets (where to place each)

## Quick Reference

| Thread Element | Rule | Why |
|---------------|------|-----|
| Hook (tweet 1) | No links, no hashtags, lead with strongest word | Links reduce reach; hashtags aren't needed for thread discovery |
| Visual placement | Tweet 2-4 | Shows in timeline preview when thread is collapsed |
| Spacing between tweets | 1-2 minutes | Platform threads unfold naturally; zero-spacing looks broken |
| Auto-plug link | Add to tweet 1 AFTER [20+ likes or 60+ minutes] | Early link kills reach; late link captures traffic after engagement |
| Link in final tweet | Always allowed | Expected; doesn't hurt reach at thread end |
| Reply-to-self rules | Reply in sequence to your PREVIOUS tweet (not all to tweet 1) | Creates a true thread; replying all to tweet 1 looks like a monologue |
| Thread length cap | 12 tweets max before engagement drops | Beyond 12, people bail; split into multi-part if needed |

## Procedure

1. Start with the full thread draft (from `thread-create`).

2. Verify thread mechanics:
   - Tweet 1: under 280 characters. No link. No hashtag. Hook-driven.
   - Each subsequent tweet: replies to the previous tweet in sequence.
   - Final tweet: includes summary + CTA. Link (if any) lives here.

3. Set tweet spacing:
   - Minimum: 30 seconds between tweets
   - Optimal: 1-2 minutes between tweets (feels natural, lets system register each as a reply)
   - Max: 5 minutes (longer gaps lose thread momentum)

4. Place visual media:
   - 1 visual per thread recommended (more is distracting)
   - Best position: tweet 2, 3, or 4 (visible when thread is collapsed in timeline)
   - Image: pre-formatted per `asset-format`. Include alt-text.
   - Video: keep under 2:20. Captions required.

5. Configure auto-plug rules:
   - Identify the link you want to insert (newsletter signup, product page, full article)
   - Set trigger threshold: "After tweet 1 reaches [20] likes OR [60] minutes, whichever comes first"
   - Action: reply to tweet 1 with: "[Call to action] [Link]"
   - Example: "If you want these frameworks in your inbox every week: [newsletter link]"
   - Tools like Hypefury and Typefully support automated auto-plug

6. For multi-part threads:
   - Label clearly: "Part 1/3", "Part 2/3", etc. (in the first tweet of each part)
   - Space parts across different days, not hours
   - Each part must work as a standalone thread (people find part 2 without seeing part 1)
   - Link to other parts in the final tweet of each

7. Schedule the thread:
   - Use threading features in your scheduling tool (most support "thread mode")
   - Double-check: each tweet replies to the correct parent tweet
   - Schedule for optimal thread time (weekday mornings, per `cadence-timing`)

## Output Format

```markdown
# Thread Structure: [Thread Title]

## Sequence
| Tweet # | Text (truncated) | Parent | Media | Notes |
|---------|-----------------|--------|-------|-------|
| 1 | [Hook text] | (root) | None | No link, no hashtag |
| 2 | [Context text] | Tweet 1 | Image [file] | Establishes credibility |
| 3 | [Insight 1] | Tweet 2 | None | |
...
| Final | [Summary + CTA] | Tweet N-1 | None | Link: [URL] |

## Auto-Plug Configuration
- **Link:** [URL]
- **Trigger:** After tweet 1 reaches [N] likes OR [N] minutes
- **Reply text:** [Auto-plug message + link]

## Thread Settings
- **Total tweets:** [N]
- **Spacing:** [N] seconds/minutes between tweets
- **Scheduled for:** [Day, time window]
- **Scheduling tool:** [Hypefury / Typefully / Buffer / native]

## Fallback
If auto-plug doesn't trigger (engagement too low):
- Manually add link to tweet 1 after 90 minutes regardless
```

## Pitfalls

- Replying all tweets to tweet 1 instead of each previous tweet (breaks thread UI)
- Zero spacing between tweets (posts simultaneously — thread doesn't "unfold")
- Auto-plugging too early (link at 5 likes looks desperate, kills organic momentum)
- Auto-plugging too late (thread is dead by hour 6, nobody will see the link)
- Forgetting to configure auto-plug and realizing the thread has no link after it already went viral
- Threads that reply to the wrong parent after an edit (hard to fix once live)

## Verification

Preview the thread sequence in your scheduling tool. Click "show thread" mode if available. Does the order look right? Does each tweet reply to the correct parent? Is the auto-plug configured? Is tweet 1 clean (no links, no hashtags)?
