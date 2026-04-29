---
name: content-calendar
description: Generate weekly and monthly content calendars with day-by-day plans including content pillars, specific topics, formats, hooks, and platform-specific posting times.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Planning, Content-Calendar, Scheduling, Strategy]
    related_skills: [content-pillars, cadence-timing, post-create, thread-create, schedule-queue]
---

# Content Calendar

Generate a day-by-day content plan that maps every post to a pillar, format, platform, and specific topic. The calendar turns abstract strategy into an executable publishing queue.

## When to Use

- Monday morning (weekly planning routine)
- Monthly content planning session
- Product launch or campaign requires a themed content block
- Founder says "let's be more consistent"
- Entering a new platform (build a launch-week calendar)

## Quick Reference

| Calendar Type | Scope | Detail Level |
|--------------|-------|-------------|
| Weekly | 7 days, all platforms | Full topic + hook draft per slot |
| Monthly | 30 days, high-level | Pillar + format + theme per slot |
| Campaign | Duration of launch/event | Themed, multi-platform, escalating urgency |

## Procedure

1. Load foundational context:
   - Content pillars (from `content-pillars` skill output)
   - Cadence rules (from `cadence-timing` skill output)
   - Brand voice guide
   - Positioning statement
   - Any upcoming events, launches, or key dates this period

2. Determine the pillar mix for each platform this week:
   - Example for X: 3 education threads, 2 POV short posts, 2 proof posts
   - Example for LinkedIn: 2 education carousels, 1 POV post, 1 case study
   - Example for IG: 3 BTS stories, 2 education carousels, 1 meme
   - Example for TikTok: 2 trend-adapted takes, 1 BTS, 1 how-to

3. Fill each slot with a specific topic from the pillar topic banks:
   - Pick fresh topics not used in the last 3 weeks
   - If there's a trending topic (from `trend-monitor`), slot it in at the highest-engagement time

4. For each slot, draft a working hook:
   - Not the final post — just the angle
   - Example: "Thread about why most SaaS onboarding fails (real data from our first 50 customers)"

5. Assign best posting times per platform and day:
   - Use `cadence-timing` data (audience activity patterns)
   - Flag any "dead zone" slots (e.g., 3 AM audience time — don't post then)

6. Check for balance:
   - Any pillar over 50% of weekly output? Rebalance.
   - Any day with zero posts? Fill it.
   - Any day with 3+ posts on the same platform? Space them out.
   - Is there at least 1 CTA/conversion post this week?

7. Leave 1-2 "flex slots" for reactive/trending content that can't be planned in advance.

## Output Format

```markdown
# Content Calendar: [Week of Date] / [Month Year]

## Weekly Overview
- Total posts: [N across all platforms]
- Pillar mix: Education [X%] | POV [X%] | Proof [X%] | BTS [X%] | CTA [X%]
- Flex slots reserved: [N]

## Day-by-Day

### Monday
| Platform | Pillar | Format | Topic / Hook Draft | Best Time |
|----------|--------|--------|--------------------|-----------|
| X | Education | Thread | [Specific topic + working hook] | 9:00 AM ET |
| LinkedIn | Education | Carousel | [Specific topic + working hook] | 8:30 AM ET |

### Tuesday
...

### [Each day through Sunday]

## Flex Slots
- Slot 1: [Platform + preferred pillar if nothing trends]
- Slot 2: [Platform + preferred pillar if nothing trends]

## Upcoming This Month
[Key dates: launches, events, announcements that will need dedicated slots]
```

## Pitfalls

- Filling every slot and leaving zero room for reactive content — the best posts are often unplanned
- Calendar that's technically "balanced" but every post sounds the same
- Planning formats the brand doesn't actually have assets for (don't schedule a carousel without visual capacity)
- Ignoring platform-specific cadence (what works on X doesn't work on LinkedIn)

## Verification

Does every slot have a specific topic, not just a pillar name? ("Education" is not a topic.) Can you trace each slot back to the brand's positioning? Is there at least 1 post this week that could genuinely surprise the audience (not just fill a slot)?
