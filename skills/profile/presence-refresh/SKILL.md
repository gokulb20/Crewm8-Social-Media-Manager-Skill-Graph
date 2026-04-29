---
name: presence-refresh
description: Optimize and refresh social bios, rotate pinned posts when high-performing content drops, update header/banner images, and manage link-in-bio pages for maximum conversion.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Profile, Optimization, Bio, Link-in-Bio]
    related_skills: [profile-audit, brand-voice-system, positioning-statement, cta-craft]
---

# Presence Refresh

Keep the brand's social presence fresh, current, and optimized for conversion. Static profiles signal a dead brand. This skill manages ongoing profile optimization — bios, pinned posts, banners, and link-in-bio pages — triggered by content performance and campaign cycles.

## When to Use

- High-performing content drops (pin it, update bio to reference it)
- Campaign or product launch (refresh headers, bio link, pinned post)
- Seasonal update (new year, conference season, major event)
- `profile-audit` found issues that need ongoing maintenance
- Link-in-bio page needs optimization (which link is the #1 priority?)
- Founder updated their personal brand (need to propagate to company profiles)

## Quick Reference

| Element | Refresh Trigger | Frequency | Who Does It |
|---------|----------------|-----------|------------|
| Bio text | New positioning, new offer, campaign focus | Monthly or per campaign | AI drafts, founder approves |
| Pinned post | New high-performer (top 10% by engagement) | Whenever a post qualifies | AI flags, founder approves pin |
| Header/banner | Campaign, season, new visual brand | Quarterly or per campaign | Designer + AI concept |
| Link in bio | Campaign priority shift (CTO: what's the ONE action?) | Per campaign or weekly | AI manages, founder confirms destination |
| Story highlights (IG) | New content themes, outdated covers | Monthly | Designer + AI curation |

## Procedure

1. **Bio optimization:**
   - Review current bio on each platform
   - Does it clearly state: who you help, what you do, why it matters?
   - Is there a value prop hook, not just a job title?
   - Are keywords optimized for platform search? (LinkedIn, IG, TikTok are search engines)
   - Draft updated bio variants: full version, short version (for platforms with limits)
   - Run through brand voice check
   - Founder approval required before any bio change

2. **Pinned post rotation:**
   - After every `performance-report`, identify any post in the top 10% of engagement (by platform)
   - Check current pinned post — is it still the best representation of the brand?
   - Criteria for pinning:
     - High engagement (top 10% of all brand posts)
     - Represents the brand's current focus/message
     - Has a working CTA (link to product, newsletter, or resource)
     - Not time-sensitive (still relevant in 4 weeks)
   - When pinning new content, document what was unpinned and why
   - Frequency: check weekly, rotate when a clear upgrade is available (not every week)

3. **Header/banner update:**
   - Review current banners across X and LinkedIn
   - Are they on-brand? Current? Properly sized? (see `asset-format`)
   - Update triggers:
     - Major campaign or product launch
     - Seasonal refresh (Q1 goals, conference season, year-end)
     - Visual rebrand
   - Draft banner concepts: text + visual direction + CTA if applicable
   - Generate AI image prompt for execution (delegate to `image-prompt`)
   - Founder approval before deploying

4. **Link-in-bio optimization:**
   - Determine the SINGLE most important action right now (not 15 links)
   - Options: newsletter signup, product demo, latest launch, waitlist, Linktree/campsite page
   - If using a link-in-bio tool (Linktree, Campsite, Beacons):
     - Audit the page: is the top link the highest priority?
     - Remove outdated links (old campaigns, expired offers)
     - Ensure mobile optimization (this is where traffic lands)
   - Update bio link destination whenever the priority shifts
   - Coordinate: if a post says "link in bio," the bio must match BEFORE the post goes live

5. **IG Story highlights refresh:**
   - Audit current highlights: are they organized by theme? Are covers branded?
   - Archive outdated stories (old launches, past events)
   - Add new highlight categories based on current content pillars
   - Design highlight covers (consistent visual style)
   - This is "set and refresh quarterly" work, not weekly

6. **Presence refresh schedule:**
   - Weekly: check pinned posts, verify links work
   - Monthly: bio review + minor updates
   - Quarterly: full presence refresh (bios, banners, highlights, link-in-bio)
   - Campaign-triggered: immediate refresh aligned to campaign launch

## Output Format

```markdown
# Presence Refresh: [Date / Trigger]

## Bio Updates

### X (Twitter)
**Current:** "[Current bio]"
**Proposed:** "[New bio — with value prop hook, keywords, link CTA]"
**Change reason:** [New positioning / Campaign focus / Keyword optimization]
**Status:** [Draft / Founder approved / Live]

### LinkedIn / IG / TikTok
... [same structure]

---

## Pinned Post Rotation

### [Platform]
**Currently pinned:** [Post title + date + engagement metrics]
**Proposed new pin:** [Post title + date + why it's an upgrade]
**Status:** [Proposed / Approved / Switched]

---

## Header/Banner Refresh

### [Platform — X / LinkedIn]
**Current banner:** [Description + screenshot ref]
**Proposed banner:** [Concept description + AI prompt]
**Change reason:** [Campaign / Seasonal / Rebrand]
**Specs:** [Dimensions from asset-format]
**Status:** [Draft / In design / Live]

---

## Link-in-Bio Update

**Current destination:** [URL + what it promotes]
**Proposed destination:** [URL + why it's the priority now]
**Link-in-bio tool (if applicable):** [Linktree / Campsite / etc.]
- Audit notes: [Top link, outdated links to remove, mobile check]
**Status:** [Updated / Needs updating — date]

---

## IG Story Highlights
**New highlights needed:** [List categories]
**Outdated to archive:** [List]
**Cover design:** [Style direction]
**Status:** [Planned / In design / Updated]

---

## Refresh Summary
| Element | Last Updated | Next Scheduled | Status |
|---------|-------------|---------------|--------|
| Bios | [Date] | [Date] | [Current / Needs update] |
| Pinned posts | [Date] | Weekly check | [Current / Needs update] |
| Banners | [Date] | [Date] | [Current / Needs update] |
| Link-in-bio | [Date] | Weekly check | [Current / Needs update] |
| IG highlights | [Date] | [Date] | [Current / Needs update] |
```

## Pitfalls

- Changing bio too frequently (audience can't remember what you do if it changes monthly)
- Pinning a post just because it performed well (it also needs to represent the brand's CURRENT focus)
- "Link in bio" that goes to a homepage instead of a specific, optimized destination (wasted opportunity)
- Updating link-in-bio for a post but forgetting to update it BACK after the post window closes
- Banner images that aren't mobile-optimized (text gets cropped on phone screens)
- Letting profiles go stale for 6+ months (signals the brand is dormant)

## Verification

Open every profile. Does each one communicate a clear, consistent message in under 5 seconds? Are pinned posts actually worth pinning? Does every link go where it should? Would a first-time visitor know exactly what to do next?
