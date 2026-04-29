---
name: impersonator-monitor
description: Monitor for brand impersonators, fake accounts, and phishing attempts — draft platform report copy and escalation guidance for takedown requests.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Crisis, Impersonation, Security, Brand-Protection]
    related_skills: [crisis-respond, mention-monitor, apology-draft]
---

# Impersonator Monitor

Detect and respond to brand impersonation, fake accounts, and phishing attempts targeting the brand or its audience. Impersonators erode trust, confuse customers, and in serious cases can be used for scams. Fast detection and reporting are critical.

## When to Use

- Routine weekly sweep for fake accounts
- Customer reports seeing a suspicious account claiming to be the brand
- Spike in DMs asking "is this account you?"
- After the brand gains visibility (impersonator activity spikes after viral posts)
- Competitor or bad actor creates a parody/confusion account
- Phishing DMs or comments detected pretending to be from the brand

## Quick Reference

| Impersonator Type | Risk Level | Detection Method | Response |
|------------------|-----------|-----------------|----------|
| Exact handle clone | High | Platform search for similar handles | Immediate report to platform |
| Lookalike account (similar name/photo) | High | Manual search, follower reports | Report + warn audience if active |
| DM phishing | Critical | Audience reports, manual inbox monitoring | Report + public warning post if widespread |
| Parody/satire account | Low-Medium | Platform search | Assess: is it clearly parody? If yes, monitor. If ambiguous (confusing consumers), report. |
| Fake customer support account | Critical | Customer complaints about being scammed | Immediate report + public warning + legal if needed |

## Procedure

1. Set up monitoring:
   - Weekly manual search for variations of the brand name/handle across all platforms
   - Set up Google Alerts for "[brand] fake account" and "[brand] scam"
   - Encourage audience to report suspicious accounts (public post: "we will never DM you asking for payment")
   - Monitor common impersonation patterns: adding "support", "help", "official", numbers, underscores to the brand name

2. When an impersonator is detected, document:
   - Platform and handle/URL
   - Screenshot of the account and any posts/DMs
   - What they're doing (passive existence vs. active impersonation vs. scamming)
   - How many followers they have (is anyone being fooled?)
   - Whether they've interacted with your real audience

3. Assess severity:
   - **Low:** Dormant account, no followers, no activity. Report and move on.
   - **Medium:** Active account but clearly distinguishable. Report + monitor.
   - **High:** Actively impersonating, messaging customers, or gaining followers. Report immediately + consider public warning.
   - **Critical:** Running scams, phishing, or causing financial harm. Report immediately + public warning + legal counsel.

4. Draft the platform report:
   - Use the platform's impersonation/trademark violation reporting form
   - Provide clear evidence (screenshots, handle comparison, examples of deception)
   - Most platforms: impersonation violates ToS and is taken seriously, but response times vary (24 hours to 2 weeks)
   - Follow up if no action after 72 hours for High/Critical cases

5. If the situation warrants a public warning:
   - Post across all platforms: "We are aware of fake accounts impersonating [brand]. Our ONLY official accounts are: [list handles]. We will NEVER DM you asking for payment or personal information. Please report any suspicious accounts."
   - Pin this warning for the duration of the impersonation activity
   - Update when the fake accounts are removed

6. Maintain an impersonation log:
   - Every detected impersonator with dates, actions taken, and resolution
   - Patterns: certain platforms worse than others? Recurring after specific events?
   - This log is valuable for platform escalation and potential legal action

## Output Format

```markdown
# Impersonator Monitor: [Date / Sweep]

## Detection

### Impersonator 1
**Platform:** [X / LinkedIn / IG / TikTok]
**Handle/URL:** [Fake handle]
**Detected via:** [Routine sweep / Customer report / DM inquiry]
**Real brand handle:** [Our actual handle for comparison]
**Severity:** [Low / Medium / High / Critical]

**Activity:**
- Followers: [N]
- Posts: [N]
- What they're doing: [Passive / Active impersonation / DM phishing / Scamming]
- Evidence: [Screenshots or links]

**Action Taken:**
- [ ] Platform report filed (date: [date])
- [ ] Follow-up scheduled (72 hours for High+)
- [ ] Public warning posted ([date / link to post])
- [ ] Legal counsel contacted ([date if applicable])

**Status:** [Reported — awaiting takedown / Resolved — removed / Ongoing]

---

## Impersonation Log (Running)

| Date | Platform | Fake Handle | Type | Severity | Reported | Resolved | Recurrence? |
|------|----------|------------|------|----------|----------|----------|-------------|
| [date] | X | @fakehandle | Clone | High | 3/15 | 3/17 | No |
...

## Patterns
- **Most active platform for impersonation:** [Platform]
- **Recurrence triggers:** [After viral posts / During product launches / Always on weekends]
- **Most common type:** [Handle clone / Support impersonation / Phishing DMs]

## Audience Protection
- **Warning post live on:** [X / LinkedIn / IG / TikTok — date posted and pinned]
- **Next sweep scheduled:** [Date]
```

## Pitfalls

- Not doing routine sweeps (you only find impersonators when they've already scammed someone)
- Engaging directly with an impersonator (don't argue — just report)
- Not warning the audience when active impersonation is happening (they need to know)
- Reporting once and never following up (platforms are slow — you need to escalate)
- Not maintaining a log (patterns become invisible, repeat impersonators go undetected)
- Assuming parody accounts are harmless ("clearly parody" is not always clear to the audience)

## Verification

Search for "[brand]" plus "official", "support", "help", "team" on each platform. Do any accounts appear that aren't yours? Check the last 30 days of DMs and mentions — did anyone ask "is this you?" about an account? If yes, that account needs investigation. Is the audience warning post live and pinned?
