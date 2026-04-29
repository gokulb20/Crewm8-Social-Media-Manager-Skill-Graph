---
name: apology-draft
description: Draft apology and correction posts with tone calibration for the situation — from minor correction to serious mea culpa — with founder review and approval gating.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, crisis, apology, reputation, tone, trust]
related_skills: [crisis-respond, brand-voice-system, draft-review]
inputs_required: [situation-summary, severity-assessment, founder-availability]
deliverables: [apology-draft-with-language-audit-and-review-gate]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Apology Draft

Draft public apologies and corrections when the brand needs to address a mistake, misstep, or controversy. An apology done right can strengthen trust. An apology done wrong makes everything worse.

## Purpose

Every brand will eventually need to apologize. The difference between a trust-building apology and a reputation-damaging one comes down to three things: accountability, specificity, and action. This skill ensures all three are present.

## When to Use

- Brand posted something with a factual error
- Brand posted something that offended part of the audience
- Product/service failure affecting customers
- Founder made a statement needing contextualization

## Inputs Required

- What happened (full context)
- Who was affected
- Severity assessment
- Founder's willingness to engage

## Quick Reference

| Severity | Apology Type | Tone | Key Elements |
|----------|-------------|------|-------------|
| Minor (typo, wrong date) | Correction post | Light, self-aware | "We got [X] wrong — here's the correction" |
| Medium (insensitive framing) | Acknowledgment + apology | Genuine, non-defensive | 1. Acknowledge impact 2. Apologize without excuses 3. Commit to doing better |
| Serious (product failure, offensive content) | Full apology | Serious, accountable, action-oriented | 1. What happened 2. Full apology (no "if" or "but") 3. What we're doing 4. How we'll prevent it |
| Crisis (legal, ethical, safety) | Crisis statement from founder | Founder-led, may require legal review | Founder's voice, transparent, specific actions |

## Procedure

1. **Assess severity** using the Quick Reference table.

2. **For medium+ severity:** Gather full context, identify specific harm. Draft involves founder.

3. **Draft the apology:**
   - **Minor:** 1-2 sentences acknowledging error + correct info + self-aware note
   - **Medium:** Acknowledge specific mistake → acknowledge impact → apologize directly → state what you'll do differently
   - **Serious:** State exactly what happened → full unconditional apology → concrete actions → timeline

4. **Avoid apology-killing language:**
   - "We're sorry if anyone was offended" (conditional = not an apology)
   - "Mistakes were made" (passive voice = no accountability)
   - "This is not who we are" (if you did it, it is)

5. **Founder review required** for medium+ severity. Legal review for serious/crisis.

6. **Prepare monitoring plan:** replies to apology, follow-up if needed.

## Output Format

```markdown
# Apology Draft: [Situation]

## Situation Summary
**What happened:** [Specific description]
**Severity:** [Minor / Medium / Serious / Crisis]
**Who was affected:** [People, groups, customers]

## Draft Apology
**Platform:** [Primary platform]
```
[Full apology text, formatted exactly as it should appear]
```

## Language Audit
- [ ] Uses "I'm sorry" or "We apologize" (not conditional "if")
- [ ] Acknowledges specific impact
- [ ] No defensive/explanatory language
- [ ] Includes concrete action, not just words

## Review Gate
**Founder review required:** [Yes / No]
**Legal review recommended:** [Yes / No]
**Deadline for posting:** [Timeframe]

## Post-Apology Monitoring
- Monitor for [N] hours
- Watch for: [Continued criticism / Acceptance / New info]
```

## Done Criteria

The skill is complete when:
1. Severity is accurately assessed
2. Apology includes specific impact acknowledgment
3. No conditional or passive language exists
4. Concrete actions follow the apology
5. Founder and/or legal review gates are set for anything above "minor"

## Pitfalls

- Apologizing for things that don't need it (legitimizes bad-faith criticism)
- The non-apology apology (sounds like apology but takes no responsibility)
- Over-apologizing (10 paragraphs for a typo)
- Over-explaining (more words = more chances to make it worse)
- Not following through on promised action

## Verification

Strip it down to: "I [did X]. It caused [Y]. I'm sorry. I will [do Z]." If that core is missing, rewrite. Would you accept this apology if directed at you?
