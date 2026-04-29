---
name: crisis-respond
description: Detect negative comments, trolls, and PR issues early — draft calm, professional responses with clear escalation guidelines for what the AI handles vs. what goes to the founder.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Crisis, Reputation, Response, Escalation]
    related_skills: [mention-monitor, dm-respond, apology-draft, impersonator-monitor]
---

# Crisis Respond

Detect and respond to negative social situations before they become crises. Speed and tone are everything — a well-handled complaint can build trust; an ignored or defensive response can cause reputational damage that takes months to undo.

## When to Use

- Negative comment or reply detected on a brand post
- Spike in negative mentions (from `mention-monitor`)
- Trolls or coordinated negative engagement pattern detected
- Customer complaint goes public on social
- Founder or brand is being criticized in the industry conversation
- Potential PR issue brewing (monitor, don't engage unless necessary)

## Quick Reference

| Situation | Response Approach | Escalation Rule |
|-----------|-----------------|----------------|
| Legitimate customer complaint | Acknowledge, empathize, offer to resolve privately (DM/email) | Escalate to founder if: high-value customer, technical issue, refund needed |
| Fair criticism of content/opinion | Thank them, engage respectfully with perspective, don't get defensive | Escalate if the criticism is from an influential industry voice |
| Misunderstanding / factual error | Politely clarify with facts, link to source if available | Escalate if clarification might make things worse |
| Troll / bad-faith engagement | Do NOT engage. Hide/report if platform allows. | Escalate if troll is impersonating brand or spreading false claims |
| Coordinated attack | Flag immediately. Do not respond individually. | Escalate to founder immediately |
| Personal attack on founder | Hide/block. One calm response maximum from founder if they choose. | Let founder decide if they want to respond |

## Procedure

1. Detection:
   - `mention-monitor` flags negative sentiment mentions
   - `dm-respond` surfaces complaints received via DM
   - Manual feed check for comments on brand posts that need response
   - Set up keyword alerts for "[brand] sucks", "[brand] scam", "[brand] terrible"
   - Detection must be fast — 1 hour is the difference between contained and viral

2. Triage each situation using the Quick Reference table:
   - Is this a legitimate complaint or bad-faith engagement?
   - Is this a one-off or part of a pattern?
   - What's the worst-case scenario if this escalates?

3. For legitimate complaints (handle directly):
   - Acknowledge first: "I hear you on this" — don't jump to defense or solution
   - Validate their feeling even if you disagree with their conclusion
   - Offer a path to resolution: "DM me and I'll personally make sure this gets resolved" or "Email [support] and reference this post"
   - Keep it public for the first reply (others see you're responsive), then move to private
   - NEVER argue, minimize, or dismiss in public

4. For trolls and bad-faith engagement (do not engage):
   - Hide the comment if the platform allows (they want attention — don't give it)
   - Report if it violates platform policies
   - Do NOT reply publicly (feeding trolls encourages more trolling)
   - Monitor to see if others pile on (if so, one calm "We appreciate feedback. If you have a genuine concern, our DMs are open." and stop)

5. For coordinated attacks (escalate immediately):
   - Flag to founder with full context
   - Do not reply to individual attackers
   - Prepare a single measured response if the founder decides to address it
   - Monitor volume and sentiment trajectory

6. Document every crisis interaction:
   - What triggered it
   - What response was given
   - What was the outcome
   - What should be done differently next time
   - Build a pattern library — repeated complaint types should inform product/strategy

## Output Format

```markdown
# Crisis Response: [Situation]

## Detection
**Time detected:** [Timestamp]
**Platform:** [X / LinkedIn / IG / TikTok]
**Source:** [Comment / DM / Mention / Coordinated]
**Trigger:** [What was said]

---

## Assessment

**Type:** [Legitimate complaint / Troll / Fair criticism / Attack / Misunderstanding]
**Severity:** [Low / Medium / High / Critical]
**Pattern check:** [One-off / Recurring issue — has this happened before?]

---

## Response Plan

### Drafted Response
**Public reply (if applicable):**
```
[Full response text, tone-calibrated to situation]
```

**Follow-up (DM/private if moving off-platform):**
```
[DM text if taking conversation private]
```

**OR: No Response**
**Why:** [Troll / Bad faith / Better to stay silent]

---

## Escalation
**Escalate to founder:** [Yes / No]
**Founder briefing (if yes):**
[Summary of situation, what happened, what's been done, what's needed from founder]

---

## Monitoring
**Watch for:** [Volume increase, sentiment shift, media pickup, platform action]
**Check frequency:** [Every 30 min / 1 hour / 4 hours / daily]

---

## Resolution
**Status:** [Resolved / Ongoing / Escalated / Contained]
**Outcome:** [What happened after response]
**Learning:** [What to do differently next time — add to pattern library]
```

## Pitfalls

- Responding defensively ("actually, you're wrong because...") — validates the complainer and escalates the conflict
- Responding too slowly (a 4-hour-old complaint with 50 replies piling on is much harder to contain)
- Engaging with trolls (every reply is fuel)
- Deleting legitimate criticism (creates a Streisand effect — screenshots exist)
- Using corporate crisis language ("We take this matter seriously") — sounds like a PR robot, not a human brand
- Not escalating when you should (the AI can't make judgment calls on legally sensitive situations)
- Over-escalating (flagging every mild complaint to the founder burns their trust in the system)

## Verification

Read your drafted response. Does it sound like a human who genuinely cares, or a PR department? Would the complainer feel heard after reading it? Is it short enough that it won't be screenshotted out of context? Have you checked with the founder before sending anything that could go viral for the wrong reasons?
