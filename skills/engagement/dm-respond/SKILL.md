---
name: dm-respond
description: Draft DM responses to inbound messages with categorization (sales, support, collaboration, spam) and appropriate tone, routing, and escalation rules.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Engagement, DMs, Customer-Service, Triage]
    related_skills: [comment-reply, mention-monitor, crisis-respond]
---

# DM Respond

Triage and draft responses to direct messages across platforms. DMs are high-trust interactions — a good DM response can convert a prospect or save a customer. A bad or ignored DM erodes that trust permanently.

## When to Use

- Daily DM inbox check (across X, LinkedIn, Instagram, TikTok)
- New inbound message requires categorization and response draft
- Founder is overwhelmed by DM volume and needs triage
- DM is sensitive (angry customer, legal concern, partnership offer) — needs escalation
- Building response templates for common DM types to speed up future replies

## Quick Reference

| Category | Priority | Response Time | Tone | Escalation Rule |
|----------|---------|--------------|------|----------------|
| Sales inquiry | High | Within 2 hours | Helpful, informative, warm | Route to founder if high-value prospect |
| Support / complaint | Critical | Within 1 hour | Empathetic, solution-focused, calm | Escalate if technical or account-specific |
| Collaboration / partnership | Medium | Within 24 hours | Professional, open, qualifying | Route to founder with summary |
| Spam / irrelevant | Low | Ignore or block | N/A | Do not engage |
| Personal / founder connection | Medium | Within 24 hours | Personal, warm | Forward to founder directly |
| Press / media inquiry | High | Within 4 hours | Professional, prepared | Route to founder immediately |

## Procedure

1. Review new DMs across all platforms (minimum daily; ideally 2x/day during business hours).

2. Categorize each message using the Quick Reference table.

3. For each category, draft an appropriate response:

   **Sales inquiry:**
   - Acknowledge their interest and specific question
   - Provide clear, helpful information (no hard sell in first reply)
   - Offer a clear next step: "Would you like me to set up a quick call with [founder]?" or "Here's a link to learn more"
   - Collect relevant context if routing to founder (company, use case, budget indicator)

   **Support / complaint:**
   - Acknowledge their frustration first (don't jump to solution)
   - Apologize if appropriate (genuine, not formulaic)
   - Ask clarifying questions if needed
   - Provide resolution or next step
   - Escalate to founder if: technical issue, account problem, refund request, or high-value customer at risk

   **Collaboration / partnership:**
   - Thank them for reaching out
   - Ask qualifying questions: what they have in mind, audience size, what they're looking for
   - Don't commit to anything in the first reply
   - Route to founder with a summary: who they are, what they want, your assessment of fit

   **Spam / irrelevant:**
   - Do not engage
   - Block/report if aggressive or repeated
   - No response needed

   **Personal / founder connection:**
   - If clearly someone the founder knows: acknowledge warmly, flag for founder to reply personally
   - If unclear: ask a gentle qualifying question before routing

4. Apply brand voice to every response:
   - Sales: informative, not pushy
   - Support: empathetic, not defensive
   - Collaboration: professional, not desperate
   - The DM voice should feel like the founder typing, not a customer service bot

5. Track response status:
   - Replied: response sent
   - Escalated: routed to founder with summary
   - Pending: waiting on information before replying
   - Ignored: spam or explicitly not worth responding to

## Output Format

```markdown
# DM Inbox: [Date]

## Message 1
**Platform:** [X / LinkedIn / IG / TikTok]
**From:** @handle / [Name]
**Category:** [Sales / Support / Collaboration / Spam / Personal / Press]
**Priority:** [Critical / High / Medium / Low]
**Message:** "[Full DM text]"

**Response Draft:**
[Full response text, formatted for platform]

**Action:** [Send / Escalate to founder / Ignore]
**If escalated — summary for founder:** [Who, what they want, your recommendation]

---

## Daily DM Summary
- Total new: [N]
- Replied: [N]
- Escalated to founder: [N]
- Pending (waiting on info): [N]
- Ignored (spam): [N]
- Avg response time: [N] hours
```

## Pitfalls

- Using the same templated response for every DM (people can tell)
- Responding to spam or trolls (rewards bad behavior, wastes time)
- DMing a link without context or relationship (spammy even if well-intentioned)
- Ignoring support DMs (the fastest way to create a public complainer)
- Over-promising in DMs ("founder will reach out personally today" unless actually true)
- Not tracking unresolved DMs (they pile up and become a reputation problem)

## Verification

Read each drafted response. Does it sound human? Would the founder feel good about this being sent in their name? Does the response actually answer their question or address their concern? For escalated DMs, is the founder summary enough for them to reply without reading the full thread?
