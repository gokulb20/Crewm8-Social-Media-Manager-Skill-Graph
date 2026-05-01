---
name: crisis-respond
description: Detect negative comments, trolls, and PR issues early — draft calm, professional responses with clear escalation guidelines for what the agent handles vs. what goes to the founder.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, crisis, reputation, response, escalation, brand-protection]
related_skills: [mention-monitor, dm-respond, apology-draft, impersonator-monitor]
inputs_required: [situation-details, sentiment-assessment, escalation-contacts]
deliverables: [crisis-response-plan-with-drafted-responses]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: ["FIRECRAWL_API_KEY"]
required_env_vars: ["FIRECRAWL_API_KEY"]
---

# Crisis Respond

Detect and respond to negative social situations before they become crises. Speed and tone are everything — a well-handled complaint can build trust; an ignored or defensive response can cause reputational damage that takes months to undo.

## Purpose

One hour is the difference between a contained complaint and a viral crisis. This skill triages situations, drafts appropriate responses, and knows exactly when to escalate to the founder.

## When to Use

- Negative comment detected on brand post
- Spike in negative mentions
- Customer complaint goes public
- Founder or brand is being criticized
- Potential PR issue brewing

## Inputs Required

- The triggering comment, mention, or DM
- Context (one-off or pattern)
- Brand voice guide (for tone calibration)
- Escalation contacts

## Quick Reference

| Situation | Response | Escalate When |
|-----------|---------|--------------|
| Legitimate complaint | Acknowledge, empathize, move to private | High-value customer, technical issue, refund |
| Fair criticism of content | Thank them, engage respectfully, no defensiveness | Criticism from influential voice |
| Misunderstanding / error | Politely clarify with facts | Clarification might make it worse |
| Troll / bad-faith | Do NOT engage. Hide/report if possible | Impersonating brand or spreading false claims |
| Coordinated attack | Flag immediately. No individual responses. | Immediately to founder |

## Procedure

1. **Detect** via `mention-monitor`, `dm-respond`, or manual feed check.

2. **Triage:**
   - Legitimate complaint or bad-faith?
   - One-off or pattern?
   - Worst-case scenario if it escalates?

3. **For legitimate complaints:** Acknowledge first. Validate feeling. Offer path to resolution (DM/email). Keep first reply public (others see responsiveness).

4. **For trolls:** Do not reply. Hide/block. Report if violating policies.

5. **For coordinated attacks:** Escalate to founder immediately. Do not reply individually.

6. **Document every interaction:** What triggered, what response, outcome, what to do differently.

## Output Format

```markdown
# Crisis Response: [Situation]

## Detection
**Time:** [Timestamp] | **Platform:** [X / LinkedIn / IG / TikTok]
**Source:** [Comment / DM / Mention / Coordinated]
**Trigger:** [What was said]

## Assessment
**Type:** [Complaint / Troll / Criticism / Attack / Misunderstanding]
**Severity:** [Low / Medium / High / Critical]
**Pattern:** [One-off / Recurring]

## Response
**Drafted reply:** [Full text, tone-calibrated]
**OR no response:** [Why]

## Escalation
**To founder:** [Yes / No]
**Founder briefing:** [Who, what, what's been done, what's needed]

## Monitoring
**Watch for:** [Volume, sentiment, media pickup]
**Check frequency:** [Every 30 min / 1 hour / 4 hours]
```

## Done Criteria

The skill is complete when:
1. Situation is triaged and categorized
2. Response is drafted (or "no response" decision made)
3. Escalation decision is clear
4. Monitoring plan is set

## Pitfalls

- Responding defensively (validates the complaint and escalates)
- Responding too slowly (4-hour-old complaint with 50 replies is harder to contain)
- Engaging with trolls (every reply is fuel)
- Deleting legitimate criticism (Streisand effect)
- Using corporate crisis language ("we take this matter seriously")

## Verification

Read drafted response. Does it sound like a human who cares? Would the complainer feel heard? Is it short enough to not be screenshot-worthy? Has the founder been informed if needed?
