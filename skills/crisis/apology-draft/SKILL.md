---
name: apology-draft
description: Draft apology and correction posts with tone calibration for the situation — from minor correction to serious mea culpa — with founder review and approval gating.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Crisis, Apology, Reputation, Tone]
    related_skills: [crisis-respond, brand-voice-system, draft-review]
---

# Apology Draft

Draft public apologies and corrections when the brand needs to address a mistake, misstep, or controversy. An apology done right can strengthen trust; an apology done wrong makes everything worse. This skill calibrates the response to the severity of the situation.

## When to Use

- Brand posted something that contained a factual error
- Brand posted something that offended or alienated part of the audience
- Product or service failure affecting customers (outage, bug, delay)
- Founder made a statement that needs contextualization or clarification
- Something the brand did is being criticized fairly in the public conversation
- Never: for trolls, bad-faith criticism, or situations where silence is the better strategy

## Quick Reference

| Severity | Apology Type | Tone | Elements | Platforms |
|----------|-------------|------|---------|-----------|
| Minor error (typo, wrong date, broken link) | Correction post | Light, self-aware, quick | "We got [X] wrong — here's the correction" | Platform where the error was posted |
| Medium (insensitive framing, poor word choice) | Acknowledgment + apology | Genuine, non-defensive, learning-focused | 1. Acknowledge impact 2. Apologize without excuses 3. Commit to doing better | All active platforms |
| Serious (product failure, customer harm, offensive content) | Full apology | Serious, accountable, action-oriented | 1. What happened 2. Full apology (no "if" or "but") 3. What we're doing about it 4. How we'll prevent it | All platforms + email + website |
| Crisis (legal, ethical, safety) | Crisis statement with founder | Founder-led, vetted by legal if applicable | Founder's voice, transparent, specific actions | All platforms + press + direct communication |

## Procedure

1. Assess the situation and severity level using the Quick Reference table.

2. For any apology above "minor":
   - Gather the full context: what exactly happened, who was affected, what's the fallout
   - Identify the specific harm (who was hurt and how)
   - Draft NOTHING until you understand the full picture
   - This requires founder involvement — the AI drafts, the founder owns the apology

3. Draft the apology using the severity-appropriate structure:

   **Minor correction:**
   - 1-2 sentences acknowledging the error
   - Correct information
   - Brief self-aware note ("Good catch from @user who pointed this out")
   - Delete or edit the original post if possible (add "EDIT:" note)

   **Medium apology:**
   - Acknowledge what you got wrong (be specific — not "we made a mistake," but "our post about X used language that minimized Y")
   - Acknowledge the impact (how it affected people, not just what you intended)
   - Apologize directly: "I'm sorry" or "We apologize" — never "we're sorry if anyone was offended"
   - State what you'll do differently
   - Keep it brief (long apologies read as defensive)

   **Serious apology:**
   - State exactly what happened (transparency builds trust)
   - Full, unconditional apology
   - Concrete actions being taken (not promises — actual steps)
   - Timeline for resolution if applicable
   - Contact point for affected people
   - Founder's voice — serious apologies should come from the person, not the brand

4. Avoid apology-killing language:
   - "We're sorry if anyone was offended" (conditional apology — not an apology)
   - "Mistakes were made" (passive voice — no accountability)
   - "This is not who we are" (if you did it, it IS who you are in that moment)
   - "We were just trying to..." (explanation as deflection)
   - Over-explaining (more words = more chances to make it worse)

5. Plan the distribution:
   - Minor: platform where error occurred only
   - Medium: all active platforms + pin the apology for 48 hours
   - Serious: all platforms + email to affected users + website post + press statement if applicable
   - Crisis: founder-led multi-channel, potentially with PR/legal review

6. Prepare for the response:
   - Monitor replies to the apology
   - Have `crisis-respond` ready for follow-up
   - Don't argue with people in the replies to your apology
   - The apology is not the end — the actions that follow are

## Output Format

```markdown
# Apology Draft: [Situation]

## Situation Summary
**What happened:** [Specific description]
**Severity:** [Minor / Medium / Serious / Crisis]
**Who was affected:** [People, groups, customers]
**Platform(s):** [Where the original issue occurred]

---

## Draft Apology

### Platform: [Primary platform]
```
[Full apology text, formatted exactly as it should appear]

---
[For serious/crisis: additional distribution notes]
```

---

## Language Audit
- [ ] Uses "I'm sorry" or "We apologize" (not conditional "if")
- [ ] Acknowledges specific impact
- [ ] No defensive or explanatory language that undermines the apology
- [ ] Includes concrete action, not just words
- [ ] Founder's voice (not corporate PR-speak)

## Review Gate
**Founder review required:** [Yes / No — "Yes" for all Medium+ severity]
**Legal review recommended:** [Yes / No — for Serious and Crisis]
**Deadline for posting:** [Recommended timeframe]

## Post-Apology Monitoring
- **Monitor window:** [Next 24-72 hours]
- **Watch for:** [Continued criticism, acceptance, new information emerging]
- **Follow-up if needed:** [What would trigger a second statement]
```

## Pitfalls

- Apologizing for things that don't need an apology (gives legitimacy to bad-faith criticism)
- The "non-apology apology" — using language that sounds like an apology but takes no responsibility
- Over-apologizing (a 10-paragraph apology for a minor error looks bizarre)
- Apologizing on behalf of the founder without their direct approval (never do this)
- Not following through on the promised action (the apology sets an expectation — failing to meet it creates a second crisis)
- Apologizing too fast (before understanding the full picture) or too slow (after the narrative has hardened)
- Using humor to deflect from a serious situation (reads as not taking it seriously)

## Verification

Strip the apology down to "I [did X]. It caused [Y]. I'm sorry. I will [do Z]." If removing the surrounding language reveals that the core apology is missing or weak, rewrite. Also: would you accept this apology if it were directed at you?
