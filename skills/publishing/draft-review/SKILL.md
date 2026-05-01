---
name: draft-review
description: Create and maintain a draft review queue with founder sign-off checklist — categorize drafts by readiness, flag issues, track approvals, and minimize review friction.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, publishing, review, approval, workflow, founder]
related_skills: [schedule-queue, brand-voice-system, content-calendar]
inputs_required: [content-drafts-for-review-window, review-cadence, founder-availability]
deliverables: [draft-review-queue-with-status-tracking]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: []
required_env_vars: []
---

# Draft Review

Manage a review queue that gets content from "written" to "approved" to "scheduled" with clear sign-off gates. The founder's time is the scarcest resource — this skill minimizes review friction while maintaining quality control.

## Purpose

Founders are the bottleneck. If they need to review 30 drafts at once, they'll skim 5 and ignore the rest. This skill batches, prioritizes, and pre-clears drafts so the founder only sees what needs their judgment — and the rest flows through automatically.

## When to Use

- Content batch is drafted and ready for review
- Setting up recurring review cadence
- Founder says "review everything before it goes out"
- Review is becoming a bottleneck
- Tracking approval patterns over time

## Inputs Required

- Drafts for the review window (posts, threads, captions, visual briefs)
- Brand voice guide (for pre-review checks)
- Any flagged uncertainties from the content creator

## Quick Reference

| Draft Status | Meaning | Action |
|-------------|---------|--------|
| Draft | Written, unreviewed | Send to review queue |
| Needs Revision | Founder flagged issues | Revise and re-submit |
| Conditionally Approved | Approved with minor changes | Apply changes; no re-review |
| Approved | Ready to schedule | Move to `schedule-queue` |
| Rejected | Concept doesn't work | Archive with reason |

## Procedure

1. **Collect all drafts** for the review window. Organize by platform and scheduled date.

2. **Pre-review each draft** before sending to founder:
   - Brand voice check (from `brand-voice-system`)
   - Character counts and platform formatting verified
   - Factual claims sourced
   - URLs verified working
   - Uncertainties flagged

3. **Build the review package:**
   - Group by urgency: "must review today / this week / when you have time"
   - Include context: why this post, what pillar, expected posting day/time
   - Limit each batch to 10-15 items

4. **Send for review with clear decision options:**
   - Thumbs up = approved as-is
   - "Changes:" = conditionally approved (apply changes, no re-review)
   - "Let's rework:" = needs revision (clarify what)
   - "Skip:" = reject (add reason)

5. **Track review status:**
   - Draft name → status → reviewer notes → date
   - Flag drafts "needs revision" for 48+ hours
   - Escalate if founder hasn't reviewed by scheduling deadline

6. **Optimize over time:**
   - If 90%+ approved as-is, propose skipping review for certain content types
   - If founder consistently rejects certain formats/pillars, stop drafting them
   - Target: review-to-scheduled under 24 hours for standard content

## Output Format

```markdown
# Draft Review Queue: [Week of Date]

## Review Batch [N]
**Deadline:** [Date/time]

### Item 1: [Post Title]
**Platform:** [X / LinkedIn / IG / TikTok]
**Pillar:** [Pillar]
**Scheduled for:** [Day, time]
**Preview:** [Full text]

**Decision:**
- [ ] Approved
- [ ] Approved with changes: [notes]
- [ ] Needs revision: [what]
- [ ] Rejected: [reason]

### Item 2...
...

## Review Summary
- **Total in queue:** [N]
- **Urgent (by EOD):** [N]
- **Approval rate (trailing 4 weeks):** [N]%
- **Top rejection reasons:** [Pattern 1], [Pattern 2]
```

## Done Criteria

The skill is complete when:
1. All drafts are pre-reviewed (voice check + formatting + links)
2. Review package is organized by urgency
3. Decision options are clearly specified per draft
4. Review status is tracked
5. Approval patterns are documented (for process improvement)

## Pitfalls

- Sending founder 30 drafts at once (they skim 5, ignore the rest)
- No pre-review before founder sees it (erodes trust)
- No clear deadline ("whenever" = never)
- Founder is bottleneck and posting stops (propose "trust me" tier)
- Rejections without reasons (you keep making the same mistake)

## Verification

Check turnaround: draft submitted → founder approved. Target: under 24 hours. Check approval rate: if consistently high (90%+), reduce review friction. Check rejection patterns: if a format/pillar is rejected >30%, stop drafting it.
