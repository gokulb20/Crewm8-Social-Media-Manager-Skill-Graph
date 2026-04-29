---
name: presence-refresh
description: Optimize and refresh social bios, rotate pinned posts when high-performing content drops, update header/banner images, and manage link-in-bio pages for maximum conversion.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, profile, optimization, bio, link-in-bio, presence]
related_skills: [profile-audit, brand-voice-system, positioning-statement, cta-craft]
inputs_required: [current-profile-state, high-performing-posts, campaign-schedule]
deliverables: [presence-refresh-plan-with-timeline]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Presence Refresh

Keep the brand's social presence fresh, current, and optimized for conversion. Static profiles signal a dead brand. This skill manages ongoing profile optimization triggered by content performance and campaign cycles.

## Purpose

A stale profile is a signal that the brand isn't active. Fresh bios, current pinned posts, and updated banners communicate "we're here, we're active, and we have something worth paying attention to right now."

## When to Use

- High-performing content drops (pin it, reference in bio)
- Campaign or product launch
- Seasonal update
- `profile-audit` found issues
- Link-in-bio needs optimization

## Inputs Required

- Current bio per platform
- High-performing posts to consider for pinning
- Campaign/event schedule
- Brand visual assets (if updating banners)

## Quick Reference

| Element | Refresh Trigger | Frequency |
|---------|----------------|-----------|
| Bio text | New offer, new positioning, campaign focus | Monthly or per campaign |
| Pinned post | New top-10% post by engagement | As needed |
| Header/banner | Campaign, season, rebrand | Quarterly or per campaign |
| Link in bio | Campaign priority shift | Per campaign or weekly |
| IG Story highlights | New content themes | Monthly |

## Procedure

1. **Review current bios.** Does each clearly state who you help, what you do, why it matters? Draft updated bio variants. Founder approval required.

2. **Check pinned posts.** After every `performance-report`, flag posts in top 10% of engagement. Pin criteria: high engagement + represents current focus + has working CTA + not time-sensitive.

3. **Update headers/banners** for campaigns, seasonal refresh, or visual rebrand. Delegate visual concept to `visual-plan` + `image-prompt`.

4. **Optimize link-in-bio:** What's the single most important action right now? Update destination. Remove outdated links from link-in-bio tool.

5. **Refresh IG Story highlights.** Archive outdated, add new categories, design branded covers.

## Output Format

```markdown
# Presence Refresh: [Date / Trigger]

## Bio Updates
**X:** Current "[bio]" → Proposed "[new bio]"
**LinkedIn:** [Same]
**IG:** [Same]
**TikTok:** [Same]

## Pinned Post Rotation
**Platform:** [Name] | **Current:** [Post] | **Proposed:** [New post] | **Status:** [Approved / Live]

## Header/Banner
**Platform:** [Name] | **Current:** [Description] | **Proposed:** [Concept] | **Status:** [In design / Live]

## Link-in-Bio
**Destination:** [URL] — [What it promotes]
**Status:** [Updated / Needs update]

## Refresh Summary
| Element | Last Updated | Next Scheduled | Status |
|---------|-------------|---------------|--------|
| Bios | [Date] | [Date] | [Current / Needs update] |
| Pinned posts | [Date] | Weekly | [Current / Needs update] |
| Banners | [Date] | [Date] | [Current / Needs update] |
| Link-in-bio | [Date] | Weekly | [Current / Needs update] |
```

## Done Criteria

The skill is complete when:
1. Bios are reviewed and updated per platform
2. Pinned posts reflect current best content
3. Banners are current (no outdated campaign visuals)
4. Link-in-bio destination matches the current priority
5. Founder has approved all changes

## Pitfalls

- Changing bio too frequently (audience forgets what you do)
- Pinning a post just because it performed well (it also needs to represent current focus)
- "Link in bio" going to homepage instead of a specific destination
- Updating link for a post but forgetting to update it back after the window closes

## Verification

Open every profile. Clear message in under 5 seconds? Pinned posts worth pinning? Links work? Would a first-time visitor know exactly what to do next?
