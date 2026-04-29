---
name: impersonator-monitor
description: Monitor for brand impersonators, fake accounts, and phishing attempts — draft platform report copy and escalation guidance for takedown requests.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, crisis, impersonation, security, brand-protection, safety]
related_skills: [crisis-respond, mention-monitor, apology-draft]
inputs_required: [brand-handles, platforms-to-monitor]
deliverables: [impersonation-detection-report-and-escalation-plan]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
requires_capabilities: [web-search]
---

# Impersonator Monitor

Detect and respond to brand impersonation, fake accounts, and phishing attempts. Impersonators erode trust and confuse customers. Fast detection and reporting are critical.

## Purpose

Impersonator accounts are inevitable once a brand has any visibility. This skill makes detection systematic — weekly sweeps, customer report intake, and platform takedown procedures — so impersonators are caught before they cause real damage.

## When to Use

- Routine weekly sweep for fake accounts
- Customer reports suspicious account
- Spike in "is this you?" DMs
- After viral post (impersonator activity spikes)
- Phishing DMs detected

## Inputs Required

- Official brand handles per platform
- Customer contact channels (for reports)
- Platform support contacts

## Quick Reference

| Impersonator Type | Risk | Detection | Response |
|------------------|------|----------|----------|
| Exact handle clone | High | Search for similar handles | Immediate platform report |
| Lookalike account | High | Manual search, follower reports | Report + warn audience if active |
| DM phishing | Critical | Audience reports, inbox monitoring | Report + public warning if widespread |
| Parody/satire | Low-Medium | Platform search | Monitor unless confusing consumers |
| Fake support account | Critical | Customer complaints | Immediate report + legal if needed |

## Procedure

1. **Weekly sweep:**
   - Search for brand name variations across all platforms
   - Google Alerts for "[brand] fake" and "[brand] scam"
   - Check recent "is this you?" DMs

2. **Document each impersonator:**
   - Platform, handle, URL
   - Activity level (dormant, active, scamming)
   - Followers count
   - Evidence (screenshots)

3. **Assess severity:**
   - Low: dormant, no followers. Report and move on.
   - Medium: active but distinguishable. Report + monitor.
   - High: actively impersonating or messaging customers. Report immediately + public warning.
   - Critical: running scams or causing financial harm. Report + warning + legal.

4. **Draft platform report:**
   - Use impersonation/trademark violation form
   - Provide evidence (screenshots, handle comparison)
   - Follow up if no action after 72 hours for high/critical cases

5. **Post public warning if warranted:**
   - "Our only official accounts are: [list]. We never DM asking for payment."
   - Pin warning for duration of impersonation activity

## Output Format

```markdown
# Impersonator Monitor: [Date]

## Detected
**Platform:** [X / LinkedIn / IG / TikTok]
**Handle:** [Fake handle]
**Severity:** [Low / Medium / High / Critical]
**Activity:** [Dormant / Active / Scamming]
**Followers:** [N]

## Action
- [ ] Platform report filed ([date])
- [ ] Public warning posted ([date/link])
- [ ] Follow-up scheduled (72h for high+)

**Status:** [Reported — awaiting takedown / Resolved / Ongoing]

## Impersonation Log
| Date | Platform | Handle | Severity | Reported | Resolved |
|------|----------|--------|----------|----------|----------|
...

## Patterns
- Most active platform: [Platform]
- Recurrence triggers: [After viral / During launches]
```

## Done Criteria

The skill is complete when:
1. Weekly sweep is conducted across all active platforms
2. Each impersonator is documented (handle, severity, activity)
3. Platform reports are filed for high+ severity
4. Audience warning posted if impersonator is active
5. Impersonation log is updated

## Pitfalls

- Not doing routine sweeps (only find impersonators after damage done)
- Engaging directly with impersonators (report, don't argue)
- Not warning audience when active impersonation happening
- Not following up on platform reports

## Verification

Search for "[brand]" plus "official" / "support" / "help" on each platform. Any results that aren't yours? Check "is this you?" DMs from last 30 days — any accounts people are confused about?
