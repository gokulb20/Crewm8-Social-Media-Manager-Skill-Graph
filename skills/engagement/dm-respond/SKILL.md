---
name: dm-respond
description: Draft DM responses to inbound messages with categorization and appropriate tone — sales, support, collaboration, spam — and escalation rules for the founder.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, engagement, dms, customer-service, triage, founder]
related_skills: [comment-reply, mention-monitor, crisis-respond]
inputs_required: [inbound-dms-across-platforms, existing-response-templates-if-any]
deliverables: [dm-responses-per-category-with-escalation-decisions]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# DM Respond

Triage and draft responses to direct messages across platforms. DMs are high-trust interactions — a good DM response can convert a prospect or save a customer. A bad or ignored DM erodes that trust permanently.

## Purpose

The DM inbox is where real relationships happen. But it's also where spam, support tickets, sales inquiries, and fan mail all pile up together. This skill separates them, prioritizes them, and drafts appropriate responses so nothing falls through the cracks.

## When to Use

- Daily DM inbox check (all platforms)
- New inbound message needs categorization
- Founder overwhelmed by DM volume
- Sensitive DM (angry customer, legal concern) — needs escalation

## Inputs Required

- All new DMs across platforms
- Brand voice guide (DM voice should feel like the founder typing)
- Escalation contacts (founder, support email)

## Quick Reference

| Category | Priority | Response Time | Tone | Escalate? |
|----------|---------|--------------|------|-----------|
| Sales inquiry | High | Within 2 hours | Helpful, informative | Route if high-value prospect |
| Support / complaint | Critical | Within 1 hour | Empathetic, solution-focused | If technical or account-specific |
| Collaboration | Medium | Within 24 hours | Professional, open, qualifying | Route with summary |
| Spam / irrelevant | Low | Ignore or block | N/A | No |
| Personal / founder connection | Medium | Within 24 hours | Warm, personal | Forward to founder |
| Press / media | High | Within 4 hours | Professional, prepared | Immediate escalation |

## Procedure

1. **Review new DMs** across all platforms daily (ideally 2x/day during business hours).

2. **Categorize each message** using the Quick Reference table.

3. **Draft the response:**
   - Sales: acknowledge their interest, provide helpful info, offer next step. Collect context for routing.
   - Support: acknowledge frustration first (not solution). Apologize if appropriate. Ask clarifying questions. Escalate if needed.
   - Collaboration: thank them, ask qualifying questions. Don't commit in first reply. Route with summary.
   - Spam: do not engage. Block/report if aggressive.
   - Personal: flag for founder to reply. If unclear, ask gentle qualifying question.

4. **Apply brand voice.** DM voice should feel human, not templated. Not overly casual, not stiff.

5. **Track status:** Replied / Escalated / Pending / Ignored.

## Output Format

```markdown
# DM Inbox: [Date]

## Message 1
**Platform:** [X / LinkedIn / IG / TikTok]
**From:** @handle
**Category:** [Sales / Support / Collaboration / Spam / Personal / Press]
**Priority:** [Critical / High / Medium / Low]
**Message:** "[Full DM text]"

**Response Draft:**
[Full response text]

**Action:** [Send / Escalate / Ignore]
**If escalated — founder summary:** [Who, what they want, your recommendation]

---

## Daily Summary
- Total new: [N] | Replied: [N] | Escalated: [N] | Pending: [N] | Ignored: [N]
- Avg response time: [N] hours
```

## Done Criteria

The skill is complete when:
1. All new DMs are categorized
2. Sales/support/collaboration DMs have response drafts
3. Spam is identified and marked (no response drafted)
4. Escalated DMs have a founder summary
5. Response time priority is met (critical < 1 hour)

## Pitfalls

- Templated responses that feel automated
- Responding to troll or spam DMs
- Sending a link without context (spammy)
- Ignoring support DMs (fastest way to create a public complainer)

## Verification

Read each draft. Does it sound human? Would the founder feel good about this being sent in their name? For escalated DMs, is the founder summary enough to reply without reading the full thread?
