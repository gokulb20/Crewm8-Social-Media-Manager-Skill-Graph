---
name: cadence-timing
description: Recommend posting frequency and per-platform best posting times based on audience activity patterns, industry benchmarks, and platform-specific algorithms. Covers X, LinkedIn, Instagram, and TikTok.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, planning, cadence, timing, platform-strategy, optimization]
related_skills: [content-calendar, schedule-queue, metrics-track, performance-report]
inputs_required: [audience-geography-data-if-available, platform-analytics-export, past-post-performance-data]
deliverables: [cadence-and-timing-guide]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Cadence & Timing

Define how often and when to post on each platform. The right content at the wrong time might as well not exist. This skill determines the optimal rhythm for the brand, calibrated to audience behavior and platform dynamics.

## Purpose

Post frequency and timing are the two variables most founders get wrong — they either post nothing (invisible) or post everything at once (noise). This skill sets a sustainable cadence that maximizes reach without burning out the audience or the creator.

## When to Use

- Setting up a new platform presence
- Engagement is declining despite good content
- After audience geography shifts (new time zones dominate)
- Quarterly cadence review based on analytics
- Before building any content calendar

## Inputs Required

- Platform analytics (peak activity times, past post performance by hour/day)
- Audience geography (what time zones they live in)
- Content production capacity (how many posts per week can the team actually produce?)
- Competitor posting patterns (optional, for benchmarking)

## Quick Reference

| Platform | Recommended Min | Max Before Diminishing Returns | Best Time Zones to Target |
|----------|----------------|-------------------------------|--------------------------|
| X | 1-2 posts/day | 3-4 posts/day | ET mornings + lunch |
| LinkedIn | 3-4 posts/week | 1x/day | ET/CT Tue-Thu mornings |
| Instagram | 1 feed post/day + stories | 2 feed posts/day | Varies; evenings often strong |
| TikTok | 1-2/day | 3/day | Late afternoons, weekends |

## Procedure

1. **Gather audience data.** Pull platform analytics for the last 30-90 days. Look for:
   - Days with highest engagement
   - Hours with highest impressions in the first 60 minutes (algorithmic lift)
   - Audience geography distribution

2. **For each platform, identify:**
   - Primary posting window (highest historical engagement)
   - Secondary window (backup)
   - Dead zone (avoid — typically late night in primary audience time zone)

3. **Set weekly cadence by tier:**
   - Must-have posts (non-negotiable minimum per week)
   - Target posts (ideal number)
   - Cap limit (after which engagement per post declines)

4. **Define cadence rules per content type:**
   - Threads: weekday mornings only, never weekends, spaced 48+ hours apart
   - Carousels: LinkedIn mornings, IG evenings
   - Link posts: mid-morning, never first tweet in a thread
   - Stories: spread throughout the day, not all at once

5. **Build the timing decision tree:**
   - Urgent/trending content: post immediately, regardless of window
   - Evergreen content: schedule for best window
   - Empty slot: skip rather than post filler
   - High-stakes content (launch, apology): post at best window, not reactive urgency

## Output Format

```markdown
# [Brand] Cadence & Timing — [Date]

## X
- **Cadence:** [N] posts/day (excl. replies), [N] threads/week
- **Best days:** [Day, Day, Day]
- **Best times:** [Time window ET]
- **Avoid:** [Time window ET]
- **Thread spacing:** Max [N]/week, 48+ hours apart

## LinkedIn
- **Cadence:** [N] posts/week
- **Best days:** [Day, Day, Day]
- **Best times:** [Time window ET]
- **Avoid:** [Time window]

## Instagram
- **Cadence:** [N] feed posts/day, [N] stories/day
- **Best days:** [data-driven]
- **Best times:** [data-driven]
- **Avoid:** [data-driven]

## TikTok
- **Cadence:** [N] posts/day
- **Best days:** [data-driven]
- **Best times:** [data-driven]
- **Avoid:** [data-driven]

## Timing Decision Tree
- Urgent/trending → Post immediately
- Evergreen → Schedule for best window
- Empty slot → Skip (don't fill with filler)
- Thread → Weekday morning only
- Launch/Apology → Best window, scheduled advance
```

## Done Criteria

The skill is complete when:
1. Each active platform has a documented minimum, target, and maximum cadence
2. Posting windows (primary + secondary + avoid) are specified per platform
3. Content type rules (threads, carousels, links, stories) are documented
4. The timing decision tree covers at least 4 scenarios
5. All recommendations note whether they're based on brand data or industry defaults

## Pitfalls

- Copying generic "best times" from blog posts instead of using actual audience data
- Setting a cadence the team can't sustain (better 3 great posts/week than 10 mediocre ones)
- Ignoring time zone shifts (audience in PT vs ET vs GMT changes everything)
- Not adjusting for platform algorithm changes (X in 2026 requires different timing than 2023)

## Verification

Pull the last 30 posts per platform. Sort by engagement rate. Do the top quartile posts cluster around specific days/times? If the data contradicts the recommendation, trust the data. If the brand posts at its "best time" for 2 weeks and sees no improvement, re-run the analysis with fresh data.

## Example

*Input:* SaaS brand targeting US-based B2B founders. Past 90 days of X analytics show top posts cluster Tue-Thu 8:30-9:30 AM ET and Mon/Wed lunch 12-1 PM ET. LinkedIn shows Tue-Thu 7:30-8:30 AM ET. Lowest engagement across all platforms: Friday after 2 PM ET.

*Output:*
- X cadence: 2 posts/day primary + replies. Tue-Thu AM primary, Mon/Wed lunch secondary. No posts Friday PM.
- LinkedIn: 4 posts/week. Tue-Thu AM. Friday skip.
- IG: 5 feed posts/week + daily stories. Evenings Tue-Sat.
- TikTok: 1/day. Late afternoons Mon-Fri. Weekend mornings.
