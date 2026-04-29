---
name: cadence-timing
description: Recommend posting frequency and per-platform best posting times based on audience activity patterns, industry benchmarks, and platform-specific algorithms.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Planning, Cadence, Timing, Platform-Strategy]
    related_skills: [content-calendar, schedule-queue, metrics-track]
---

# Cadence & Timing

Define how often and when to post on each platform. The right content at the wrong time is wasted content. This skill determines the optimal rhythm for the brand.

## When to Use

- Setting up a new platform presence
- Engagement is declining despite good content
- After audience geography shifts (new time zones dominate)
- Quarterly cadence review based on analytics
- Before building any content calendar

## Quick Reference

| Platform | Recommended Min | Max Before Diminishing Returns | Best Time Zones to Target |
|----------|----------------|-------------------------------|--------------------------|
| X | 1-2 posts/day (excluding replies) | 3-4 posts/day | ET mornings + lunch |
| LinkedIn | 3-4 posts/week | 1x/day | ET/CT Tue-Thu mornings |
| Instagram | 1 feed post/day + stories | 2 feed posts/day | Varies by audience; evenings often strong |
| TikTok | 1-2/day | 3/day | Late afternoons, weekends |

## Procedure

1. Gather available audience data:
   - Platform analytics (peak activity times from native analytics)
   - Past post performance by day and hour (from `metrics-track` skill data)
   - Audience geography — what time zones do they live in?
   - Competitor posting patterns (from `competitor-audit` if available)

2. For each platform, analyze:
   - What days drive the highest engagement? (X: often Tue-Thu, but verify with data)
   - What hours drive the most impressions in the first 60 minutes? (critical for algorithmic boost)
   - Is there a "dead zone" (e.g., late night in primary audience time zone)?

3. Set the weekly cadence:
   - Must-have slots (the non-negotiable posts per week)
   - Nice-to-have slots (additional posts if content is available)
   - Cap limit (after which engagement per post declines)

4. Assign timing windows per platform:
   - Primary window (highest engagement historically)
   - Secondary window (backup if primary is missed)
   - Avoidance window (never post in this block)

5. Define cadence rules for special content types:
   - Threads: best on weekday mornings, avoid weekends
   - Carousels: LinkedIn mornings, IG evenings
   - Link posts: post mid-morning, never first tweet in a thread
   - Stories: spread throughout the day, not all at once

6. Document the "timing decision tree":
   - If a post is high-urgency (news, trend): post immediately regardless of window
   - If a post is evergreen: stick to the best window
   - If a slot is empty: better to skip than post filler at a bad time

## Output Format

```markdown
# [Brand] Cadence & Timing

## X (Twitter)
- **Cadence:** [N] posts/day (excl. replies), [N] threads/week
- **Best days:** [e.g., Tue, Wed, Thu]
- **Best times:** [e.g., 8:30-9:15 AM ET, 12:00-1:00 PM ET]
- **Avoid:** [e.g., After 9 PM ET, Sunday mornings]
- **Thread cadence:** Max [N] threads/week, spaced at least 48 hours apart

## LinkedIn
- **Cadence:** [N] posts/week
- **Best days:** [e.g., Tue, Wed, Thu]
- **Best times:** [e.g., 7:30-8:30 AM ET]
- **Avoid:** [e.g., Weekends, Friday afternoons]

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
- Urgent / trending content → Post immediately
- Evergreen content → Schedule for best window
- Empty slot → Skip rather than post filler
- Thread → Weekday morning only
```

## Pitfalls

- Copying generic "best times" from blog posts instead of using actual audience data
- Posting on a cadence the team can't sustain (better 3 great posts/week than 10 mediocre ones)
- Ignoring time zone shifts (audience in PT vs ET vs GMT changes everything)
- Not adjusting for platform algorithm changes (X in 2025 is not X in 2023)

## Verification

Pull the last 30 posts per platform. Sort by engagement rate. Do the top quartile posts cluster around specific days/times? If the data contradicts the recommendation, trust the data.
