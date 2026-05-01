---
name: thread-structure
description: Manage X thread structures — hook tweet first, proper sequencing, auto-plug link timing (after X likes or Y minutes), visual placement, and cross-tweet flow.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, publishing, threads, structure, auto-plug, x]
related_skills: [thread-create, schedule-queue, cta-craft]
inputs_required: [full-thread-draft, link-for-auto-plug, scheduling-tool]
deliverables: [thread-spec-with-tweet-sequence-and-auto-plug-config]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: []
required_env_vars: []
---

# Thread Structure

Structure X threads for maximum readability, engagement, and algorithmic performance. Handles tweet sequencing, auto-plug timing, link placement rules, visual positioning, and all the mechanical details that separate a professional thread from a broken one.

## Purpose

A great thread can fail on mechanics alone: wrong parent replies, zero spacing, auto-plug that never triggers, links in the first tweet killing reach. This skill ensures the technical execution matches the creative quality.

## When to Use

- Converting a drafted thread into a publishable sequence
- Setting auto-plug rules for link insertion
- Thread flow feels off
- Multi-part threads over multiple days
- Thread with multiple media assets

## Inputs Required

- Full thread draft (from `thread-create` or `blog-to-thread`)
- Link URL for auto-plug (if any)
- Scheduling tool that supports threads
- Posting time

## Quick Reference

| Element | Rule | Why |
|---------|------|-----|
| Hook (tweet 1) | No links, no hashtags | Links reduce reach |
| Visual placement | Tweet 2-4 | Visible in timeline preview |
| Tweet spacing | 1-2 minutes | Thread unfolds naturally |
| Auto-plug trigger | After [20+ likes or 60+ min] | Early link kills engagement |
| Link in final tweet | Always allowed | Expected, doesn't hurt reach |
| Reply structure | Each tweet replies to PREVIOUS tweet | Creates true thread structure |
| Max length | 12 tweets | Beyond 12, engagement drops |

## Procedure

1. **Verify thread mechanics:**
   - Tweet 1: under 280 chars, no link, no hashtag
   - Each subsequent tweet: replies to the previous tweet in sequence
   - Final tweet: includes summary + CTA + link

2. **Set tweet spacing:**
   - Min: 30 seconds between tweets
   - Optimal: 1-2 minutes between tweets
   - Max: 5 minutes (longer gaps lose momentum)

3. **Place visual media:**
   - 1 visual per thread recommended
   - Best position: tweet 2, 3, or 4
   - Include alt-text

4. **Configure auto-plug:**
   - Link to insert
   - Trigger threshold: "After tweet 1 reaches [20] likes OR [60] minutes, whichever comes first"
   - Action: reply to tweet 1 with CTA text + link
   - Example: "If you want these frameworks in your inbox every week: [newsletter link]"

5. **For multi-part threads:**
   - Label clearly: "Part 1/3", "Part 2/3" in the first tweet
   - Space parts across different days
   - Each part must work as a standalone thread

6. **Schedule the thread:**
   - Use threading features in your scheduling tool
   - Verify each tweet replies to the correct parent
   - Schedule for optimal thread time (weekday mornings)

## Output Format

```markdown
# Thread Structure: [Thread Title]

## Sequence
| Tweet # | Text (truncated) | Parent | Media | Notes |
|---------|-----------------|--------|-------|-------|
| 1 | [Hook] | (root) | None | No link, no hashtag |
| 2 | [Context] | Tweet 1 | Image | Credibility |
| ... | | | | |
| Final | [Summary + CTA + link] | Tweet N-1 | None | |

## Auto-Plug Configuration
- **Link:** [URL]
- **Trigger:** [N] likes OR [N] minutes
- **Reply text:** [Auto-plug message + link]

## Thread Settings
- **Total tweets:** [N]
- **Spacing:** [N] seconds/minutes
- **Scheduled for:** [Day, time]
- **Scheduling tool:** [Name]
```

## Done Criteria

The skill is complete when:
1. Tweet sequence is verified (each replies to correct parent)
2. Tweet 1 has no links or hashtags
3. Visual placement is specified (if any)
4. Auto-plug rules are configured with trigger and reply text
5. Tweet spacing is defined

## Pitfalls

- Replying all tweets to tweet 1 instead of each previous (breaks thread UI)
- Zero spacing between tweets (thread doesn't unfold)
- Auto-plugging too early (5 likes = desperate)
- Auto-plugging too late (thread dead by hour 6)
- Forgetting to configure auto-plug at all

## Verification

Preview the thread in your scheduling tool. Does the order look right? Does each tweet reply to the correct parent? Is auto-plug configured and the link correct?
