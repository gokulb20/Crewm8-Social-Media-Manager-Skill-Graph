---
name: draft-review
description: Create and maintain a draft review queue with founder sign-off checklist — categorize drafts by readiness, flag issues, track approvals, and manage revision cycles.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Publishing, Review, Approval, Workflow]
    related_skills: [schedule-queue, brand-voice-system, content-calendar]
---

# Draft Review

Manage a review queue that gets social content from "written" to "approved" to "scheduled" with clear sign-off gates. The founder's time is the scarcest resource — this skill minimizes review friction while maintaining quality control.

## When to Use

- Content batch is drafted and ready for review
- Setting up a recurring review cadence with the founder
- Founder says "I want to review everything before it goes out"
- Review is becoming a bottleneck (posts piling up, nothing getting published)
- Need to track which posts are approved, which need revision, and which are rejected

## Quick Reference

| Draft Status | Meaning | Action Required |
|-------------|---------|----------------|
| Draft | Initial content written, not yet reviewed | Send to review queue |
| Needs Revision | Founder flagged issues | Revise and re-submit |
| Conditionally Approved | Approved with minor changes noted | Apply changes, no re-review needed |
| Approved | Ready for scheduling | Move to `schedule-queue` |
| Rejected | Concept doesn't work | Archive with reason; salvage usable elements |

## Procedure

1. Collect all content drafts for the review window:
   - Posts, threads, captions, and visual briefs from all creation skills
   - Organize by platform and scheduled date

2. Pre-review each draft internally (before sending to founder):
   - Run through brand voice check (from `brand-voice-system`)
   - Verify character counts and platform formatting
   - Flag any factual claims that need sourcing
   - Check for link correctness (do all URLs work?)
   - Note any sections where you're unsure (better to flag than guess)

3. Build the review package:
   - Format drafts cleanly for founder consumption (founders don't want to read raw markdown)
   - Group by urgency: "must review today", "this week", "when you have time"
   - Include context: why this post, what pillar, expected posting day/time
   - Limit each review batch to 10-15 items (decision fatigue is real)

4. Send for review with clear decision options:
   - Thumbs up = approved as-is
   - "Changes:" = approved with notes (apply changes, no re-review needed)
   - "Let's rework:" = needs revision (clarify what needs changing)
   - "Skip:" = reject (not right for the brand right now)

5. Track review status:
   - Maintain a review log: draft name → status → reviewer notes → date
   - Flag drafts that have been "needs revision" for more than 48 hours (bottleneck)
   - Escalate if founder hasn't reviewed by the scheduling deadline

6. After review:
   - Move approved drafts to `schedule-queue`
   - Apply revision notes and re-submit "needs revision" drafts
   - Archive rejected drafts with notes on WHY (patterns will emerge over time)
   - Maintain a "founder preferences" document: what gets rejected and why

7. Optimize the review process over time:
   - If founder approves 90%+ of drafts as-is, propose skipping review for certain content types
   - If founder consistently rejects certain formats/pillars, stop drafting them
   - Target: reduce review-to-scheduled time to under 24 hours for standard content

## Output Format

```markdown
# Draft Review Queue: [Week of Date]

## Review Batch [#]
**Review deadline:** [Date/time — when this needs to be back for scheduling]

### Item 1: [Post/Thread Title]
**Platform:** [X / LinkedIn / IG / TikTok]
**Pillar:** [Education / POV / Proof / BTS / CTA]
**Scheduled for:** [Day, time]
**Preview:** [Full post text, formatted]

**Decision:**
- [ ] Approved
- [ ] Approved with changes: [notes]
- [ ] Needs revision: [what to revise]
- [ ] Rejected: [reason]

### Item 2: ...

---

## Review Summary
- **Total in queue:** [N]
- **Urgent (review by EOD):** [N]
- **This week:** [N]
- **Carry-over from last review:** [N] (still waiting)

## Approval Patterns (Last 4 Weeks)
- **Approval rate:** [N]% approved as-is
- **Top rejection reasons:** [Pattern 1], [Pattern 2]
- **Founder preferences noted:** [What to adjust going forward]
```

## Pitfalls

- Sending the founder 30 drafts at once (they'll skim 5 and ignore the rest)
- No pre-review before sending to founder (founder catches basic formatting errors = trust erodes)
- No clear deadline on review ("whenever you get to it" = never)
- Founder becomes the bottleneck and posting stops (propose a "trust me" tier of content that doesn't need review)
- Rejections without reasons (you keep making the same "mistake" because you don't know what the mistake was)
- Review process that takes longer than content creation (process is broken)

## Verification

Check the review turnaround time: draft submitted → founder approved. Target: under 24 hours. Check the approval rate: if consistently high, propose reducing review friction. Check rejection patterns: if any format or pillar is rejected more than 30% of the time, stop drafting it entirely.
