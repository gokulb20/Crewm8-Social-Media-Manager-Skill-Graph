---
name: content-calendar
description: Generate weekly and monthly content calendars with day-by-day plans including content pillars, specific topics, formats, hooks, and platform-specific posting times. Works with X, LinkedIn, Instagram, and TikTok.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, planning, content-calendar, scheduling, strategy, workflow]
related_skills: [content-pillars, cadence-timing, post-create, thread-create, schedule-queue, trend-monitor]
inputs_required: [content-pillar-document, cadence-rules, brand-calendar-key-dates, any-upcoming-announcements]
deliverables: [weekly-monthly-content-calendar]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Content Calendar

Generate a day-by-day content plan that maps every post to a pillar, format, platform, and specific topic. The calendar turns abstract strategy into an executable publishing queue.

## Purpose

Consistency is the single biggest predictor of social media growth. A plan on Sunday means you don't have to think on Tuesday. This skill produces a fillable calendar that ensures no day is empty, no pillar is neglected, and every post has a reason to exist.

## When to Use

- Monday morning weekly planning routine
- Monthly content planning session
- Product launch or campaign needs themed content block
- Founder says "let's be more consistent"
- Entering a new platform

## Inputs Required

- Content pillars document (from `content-pillars` skill)
- Cadence rules (from `cadence-timing` skill)
- Brand voice guide (from `brand-voice-system`)
- Positioning statement
- Any upcoming events, launches, or key dates this period
- Trend intelligence from `trend-monitor` (if available)

## Quick Reference

| Calendar Type | Scope | Detail Level | Best For |
|--------------|-------|-------------|----------|
| Weekly | 7 days, all platforms | Full topic + hook draft per slot | Standard operations |
| Monthly | 30 days, high-level | Pillar + format + theme per slot | Campaign planning |
| Campaign | Launch duration | Themed, multi-platform, escalating urgency | Product launches, events |

## Procedure

1. **Load context.** Bring in content pillars, cadence rules, voice guide, positioning, and any upcoming events or launches.

2. **Determine the pillar mix per platform this week.** Example:
   - X: 3 education threads, 2 POV short posts, 2 proof posts
   - LinkedIn: 2 education carousels, 1 POV post, 1 case study
   - IG: 3 BTS stories, 2 education carousels, 1 meme
   - TikTok: 2 trend-adapted takes, 1 BTS, 1 how-to

3. **Fill each slot with a specific topic from the pillar topic banks.** Don't use topics used in the last 3 weeks. If there are trending opportunities from `trend-monitor`, slot those at the highest-engagement time.

4. **Draft a working hook for each slot.** This is not the final post — it's the angle. Example: "Thread about why most SaaS onboarding fails (real data from first 50 customers)." Delegate to `hook-write` for the final hooks.

5. **Assign best posting times per platform and day.** Use `cadence-timing` data. Flag dead-zone slots (3 AM audience time — don't post then).

6. **Check for balance:**
   - Any pillar over 50%? Rebalance.
   - Any day with zero posts? Fill it.
   - Any day with 3+ posts on same platform? Space them out.
   - At least 1 CTA/conversion post this week?

7. **Reserve 1-2 flex slots.** Leave room for reactive/trending content that can't be planned. If nothing trends, the flex slot can be a filler-post from a pillar topic bank.

## Output Format

```markdown
# Content Calendar: [Week of Date]

## Weekly Overview
- Total posts: [N] across all platforms
- Pillar mix: Education [X]% / POV [X]% / Proof [X]% / BTS [X]% / CTA [X]%
- Flex slots reserved: [N]

## Day-by-Day

### Monday
| Platform | Pillar | Format | Topic / Hook Draft | Best Time |
|----------|--------|--------|--------------------|-----------|
| X | Education | Thread | [specific topic + working hook] | 9:00 AM ET |
| LinkedIn | Education | Carousel | [specific topic + working hook] | 8:30 AM ET |
| IG | BTS | Story | [behind the scenes update] | 12:00 PM ET |

### Tuesday
...

## Flex Slots
- Slot 1: [Platform + preferred pillar if nothing trends]
- Slot 2: [Platform + preferred pillar if nothing trends]

## Key Dates This Period
[Date — Event / Launch / Announcement]
```

## Done Criteria

The skill is complete when:
1. Every active platform has at least 1 post per active day (per cadence rules)
2. Every slot has a specific topic, not just a pillar name
3. No pillar exceeds 50% of weekly output
4. No day has zero posts
5. At least 1 flex slot is reserved
6. Every slot has a posting time assigned

## Pitfalls

- Filling every slot with zero room for reactive content (the best posts are often unplanned)
- Calendar that's technically balanced but every post sounds the same
- Planning formats the brand can't actually produce (no visuals for a carousel = don't schedule a carousel)
- Ignoring platform-specific cadence (what works on X daily doesn't work on LinkedIn daily)

## Verification

Does every slot have a specific topic, not just a pillar name? ("Education" is not a topic.) Can you trace each slot back to the brand's positioning? Is there at least 1 post this week that could genuinely surprise the audience?

## Example

*Input:* Positioning is "B2B outreach for seed-stage founders." Pillars are Education/POV/Proof/BTS/CTA. Cadence says 1 post/day on X, 3/week on LinkedIn, 5/week on IG.

*Output:* Monday: X = Education thread "Why cold email fails (and what actually works)" + LinkedIn = Carousel "The 3 data points that predict cold email success" + IG = BTS story about the morning team standup. Tuesday: X = POV short post "I don't think lead scoring works for pre-seed" + LinkedIn = Proof post "Case study: how [customer] got 3 meetings from 50 DMs". Total: 14 posts across platforms, 20% flex, balanced pillars.
