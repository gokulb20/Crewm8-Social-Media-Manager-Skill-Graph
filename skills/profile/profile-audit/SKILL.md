---
name: profile-audit
description: Audit all social profiles for cross-platform consistency — name, photo, bio, link, banner, and branding — flag inconsistencies and generate a remediation plan.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Profile, Audit, Consistency, Branding]
    related_skills: [presence-refresh, brand-voice-system, positioning-statement]
---

# Profile Audit

Audit every social profile the brand owns for consistency, completeness, and optimization. The profile is the digital storefront — inconsistent profiles erode trust and confuse visitors about who the brand actually is.

## When to Use

- Quarterly profile audit (minimum cadence)
- After a rebrand, name change, or visual refresh
- New platform added — audit against existing platforms for consistency
- Founder asks "do our profiles look professional?"
- Before a major launch or campaign (profiles need to be optimized for incoming traffic)
- Competitor profiles look sharper — time to catch up

## Quick Reference

| Audit Element | What to Check | Importance |
|-------------|--------------|-----------|
| Profile photo / avatar | Same or recognizable variant across all platforms | Critical |
| Display name | Consistent format across platforms | Critical |
| Handle / username | As close to identical as possible | High |
| Bio / description | Core value prop consistent, platform-appropriate length variations | Critical |
| Link in bio | Correct, working, optimized destination | Critical |
| Header / banner image | On-brand, current, properly sized per platform | Medium |
| Pinned post | Current, high-performing content pinned | Medium |
| Story highlights (IG) | Organized, branded covers, current content | Medium |
| Verification status | Any platforms eligible for verification? | Low (nice-to-have) |
| Following/followers cleanup | Following irrelevant or spam accounts? | Low |

## Procedure

1. Inventory all active social profiles:
   - X, LinkedIn, Instagram, TikTok
   - Any secondary platforms: YouTube, Threads, Bluesky, Mastodon, Reddit, Product Hunt
   - List every profile URL and handle

2. For each profile, capture:
   - Screenshot of the full profile page (mobile view — how 90% of visitors see it)
   - Current bio text
   - Profile photo
   - Header/banner image
   - Pinned post (if any)
   - Link in bio
   - Follower count, following count

3. Create a side-by-side comparison:
   - Display name: are they identical? (If not, is the variation intentional?)
   - Handle: can a user find you easily across platforms?
   - Bio: does each bio contain the same core value prop? (Length can vary, message shouldn't)
   - Link: does every bio link go somewhere useful and working?
   - Visual: do profile photos match? Do banners feel like the same brand?

4. Flag every inconsistency with severity:
   - **Critical:** Name mismatch, broken link, wrong URL, misleading bio
   - **High:** Bio missing key value prop, outdated photo, stale pinned post
   - **Medium:** Banner/image not optimized, inconsistent handle format, missing platform features (highlights, story covers)
   - **Low:** Following/followers needs cleanup, verification not pursued, minor visual tweaks

5. For each inconsistency, provide the fix:
   - What needs to change exactly
   - What it should change TO (specific text, image spec, link URL)
   - Priority and effort (is this a 5-minute fix or a design project?)

6. Check for optimization opportunities (beyond consistency):
   - Bio keyword optimization (searchable terms for platform discovery)
   - Link destination optimization (bio link page vs. direct link — which converts better?)
   - Pinned post optimization (is the most relevant, highest-performing post pinned?)
   - Profile category/industry tags (LinkedIn, IG business account settings)

7. Generate the remediation plan:
   - Quick wins (fixes that take under 10 minutes — do immediately)
   - This week (important but not urgent)
   - Next sprint (visual refreshes, banner redesigns)
   - Ongoing (cleanup, verification pursuit)

## Output Format

```markdown
# Profile Audit: [Date]

## Profile Inventory

### X (Twitter)
**URL:** [Profile URL]
**Handle:** @handle
**Display name:** [Name]
**Bio:** "[Bio text]"
**Link:** [URL]
**Profile photo:** [Description + note if up to date]
**Banner:** [Description + note if up to date]
**Pinned post:** [Post content + date + performance]
**Followers:** [N] | **Following:** [N]

### LinkedIn
... [same structure]

### Instagram
... [same structure]

### TikTok
... [same structure]

---

## Consistency Scorecard

| Element | X | LinkedIn | IG | TikTok | Consistent? |
|---------|---|----------|-----|--------|-------------|
| Display name | [Name] | [Name] | [Name] | [Name] | [Yes / No — note difference] |
| Handle | @x | @x | @x | @x | [Yes / No] |
| Core value prop in bio | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] |
| Profile photo | [Same/Variant] | [Same/Variant] | [Same/Variant] | [Same/Variant] | [Yes/No] |
| Link working | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] | [Yes/No] |
| Banner on-brand | [Yes/No] | [Yes/No] | N/A | N/A | [Yes/No] |

**Consistency score:** [N]/[total points]

---

## Issues Found

### Critical
1. **Platform:** [X/LinkedIn/etc.] | **Issue:** [What's wrong] | **Fix:** [What to change + specific text/URL]

### High
1. ...

### Medium
1. ...

### Low
1. ...

---

## Remediation Plan

### Quick Wins (Under 10 min each)
- [ ] [Fix 1] — [Platform, what to do]
- [ ] [Fix 2] — [Platform, what to do]

### This Week
- [ ] [Fix] — [Platform, detailed action]

### Next Sprint
- [ ] [Fix] — [Platform, detailed action]

### Ongoing
- [ ] [Action item]

---

## Next Audit
**Scheduled for:** [Quarter + 1]
```

## Pitfalls

- Auditing only the "main" platform and assuming the others are fine (they usually aren't)
- Not checking links actually work (broken link in bio = wasted traffic)
- Comparing desktop profile views only (mobile is how most people see profiles)
- Flagging deliberate variations as inconsistencies (some platforms call for slightly different names/bios — that's fine, just be intentional about it)
- Doing an audit and never implementing the fixes (wasted effort)
- Not re-auditing quarterly (profiles drift as different people update different platforms)

## Verification

Open each profile on mobile. Does it look professional in under 3 seconds? Can a visitor instantly tell what the brand does? Can they find the brand on any platform by searching the brand name? Do all links go somewhere useful?
