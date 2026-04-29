---
name: profile-audit
description: Audit all social profiles for cross-platform consistency — name, photo, bio, link, banner, and branding — flag inconsistencies and generate a remediation plan.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, profile, audit, consistency, branding, presence]
related_skills: [presence-refresh, brand-voice-system, positioning-statement]
inputs_required: [profile-urls-per-platform, brand-guidelines-if-available]
deliverables: [profile-audit-with-consistency-score-and-remediation-plan]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Profile Audit

Audit every social profile the brand owns for consistency, completeness, and optimization. The profile is the digital storefront — inconsistent profiles erode trust.

## Purpose

A first-time visitor decides whether to follow your brand in under 3 seconds based on your profile. If the name, photo, bio, or link doesn't match across platforms, they hesitate. This skill catches inconsistencies before visitors do.

## When to Use

- Quarterly profile audit
- After a rebrand or visual refresh
- New platform added
- Before a major launch or campaign

## Inputs Required

- Full list of active profile URLs per platform
- Brand visual guidelines (colors, logo, typography)
- Current positioning statement

## Quick Reference

| Element | What to Check | When to Update |
|---------|--------------|---------------|
| Profile photo | Same across all platforms | Quarter / Rebrand |
| Display name | Consistent format | Quarter / Name change |
| Handle | As close to identical as possible | Setup / Rebrand |
| Bio | Core value prop, platform-appropriate length | Monthly / New offer |
| Link in bio | Working, optimized destination | Weekly check |
| Header/banner | On-brand, current | Quarter / Campaign |
| Pinned post | Current, high-performing | Monthly / When new high-performer drops |

## Procedure

1. **Inventory all profiles.** X, LinkedIn, IG, TikTok + any secondary (Threads, YouTube, Reddit, etc.).

2. **Capture each profile:** screenshot (mobile view), bio text, profile photo, banner, pinned post, link, follower/following count.

3. **Create side-by-side comparison:**
   - Display names match?
   - Same value prop in bio?
   - Profile photos match?
   - Links work?

4. **Flag inconsistencies:**
   - Critical: name mismatch, broken link, wrong URL
   - High: bio missing value prop, outdated photo, stale pinned post
   - Medium: banner not optimized, inconsistent handle
   - Low: followers/following cleanup

5. **Generate remediation plan:**
   - Quick wins (under 10 min — do immediately)
   - This week (important but not urgent)
   - Next sprint (visual refreshes)

## Output Format

```markdown
# Profile Audit: [Date]

## Profile Inventory
### X: [URL] | LinkedIn: [URL] | IG: [URL] | TikTok: [URL]

## Consistency Scorecard
| Element | X | LinkedIn | IG | TikTok | Consistent? |
|---------|---|---|-----|--------|-------------|
| Display name | [Name] | [Name] | [Name] | [Name] | [Yes/No] |
| Handle | @x | @x | @x | @x | [Yes/No] |
| Bio value prop | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] |
| Profile photo | [Variant] | [Variant] | [Variant] | [Variant] | [Yes/No] |
| Link working | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] |

**Score:** [N]/[Total]

## Issues Found
### Critical: [Issue + fix]
### High: [Issue + fix]
### Medium: [Issue + fix]

## Remediation Plan
### Quick Wins (<10 min): [Fix 1], [Fix 2]
### This Week: [Fix]
### Next Sprint: [Fix]
```

## Done Criteria

The skill is complete when:
1. All active profiles are inventoried
2. Consistency scorecard is complete (every element checked per platform)
3. Issues are triaged by severity
4. Remediation plan is prioritized
5. Next audit date is set

## Pitfalls

- Auditing only the "main" platform (the rest are usually worse)
- Not checking links (broken link = wasted traffic)
- Desktop-only review (most visitors see profiles on mobile)
- Deliberate variations flagged as inconsistencies (some platforms need different approaches — be intentional)

## Verification

Open each profile on mobile. Does it look professional in under 3 seconds? Can visitors instantly tell what the brand does? Do all links work?
