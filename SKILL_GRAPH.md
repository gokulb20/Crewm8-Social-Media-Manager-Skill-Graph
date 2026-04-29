# Skill Graph

Below is the dependency graph showing how skills chain together in a typical weekly workflow. Each arrow means "output from this skill feeds into" the target skill.

## Full Dependency Map

```mermaid
flowchart TD
  BV["brand-voice-system 🏁"]
  PS["positioning-statement 🏁"]
  CP["content-pillars"]
  CT["cadence-timing"]
  CC["content-calendar"]
  TM["trend-monitor"]
  HW["hook-write"]
  PC["post-create"]
  TC["thread-create"]
  CW["caption-draft"]
  CA["cta-craft"]
  BTT["blog-to-thread"]
  PTC["podcast-to-clips"]
  NTP["newsletter-to-posts"]
  VP["visual-plan"]
  IP["image-prompt"]
  AF["asset-format"]
  MC["meme-create"]
  DR["draft-review"]
  TS["thread-structure"]
  SQ["schedule-queue"]
  XP["cross-post-adapt"]
  CR["comment-reply"]
  DM["dm-respond"]
  MM["mention-monitor"]
  IO["influencer-outreach"]
  EP["engagement-poll"]
  NR["news-response"]
  TB["trending-briefing"]
  MT["metrics-track"]
  AB["ab-test-analyze"]
  PR["performance-report"]
  CRS["crisis-respond"]
  AP["apology-draft"]
  IM["impersonator-monitor"]
  PA["profile-audit"]
  PRF["presence-refresh"]

  BV --> CC
  PS --> CC
  CP --> CC
  CT --> CC
  TM --> CC

  CC --> HW
  HW --> PC
  HW --> TC
  HW --> CW

  PC --> CA
  TC --> CA
  CW --> CA

  BTT --> TC
  PTC --> PC
  NTP --> PC

  VP --> IP
  VP --> AF
  VP --> MC

  PC --> DR
  TC --> DR
  CW --> DR
  DR --> TS
  DR --> SQ

  TS --> SQ
  SQ --> XP
  SQ --> CR

  CR --> DM
  CR --> MM
  MM --> CRS
  CRS --> AP
  CRS --> IM

  SQ --> MT
  MT --> AB
  MT --> PR
  PR --> TB

  PA --> PRF
  IO --> CR
  EP --> PC
  NR --> PC
```

## Legend

- **🏁** = Foundation skills. Run these first when onboarding a new brand.
- **→** = "feeds into" or "its output is used by"
- **Diamond** = Multiple skills converge on a single downstream skill (e.g., 7 creation skills feed into `draft-review`)

## Typical Weekly Sequence

1. **Sunday/Monday morning:** `trend-monitor` → `content-calendar` (injects trending opportunities into the week's plan)
2. **Monday:** Run creation skills against calendar slots (`hook-write` → `post-create`, `thread-create`, `caption-draft`)
3. **Monday-Tuesday:** Run repurpose skills if there's existing content to mine (`blog-to-thread`, `podcast-to-clips`, `newsletter-to-posts`)
4. **Tuesday:** Plan visuals if needed (`visual-plan` → `image-prompt` / `asset-format`)
5. **Tuesday-Wednesday:** `draft-review` gate (founder signs off)
6. **Wednesday:** Structure threads and schedule queue (`thread-structure` → `schedule-queue`)
7. **Daily (ongoing):** `comment-reply` + `dm-respond` + `mention-monitor` for engagement
8. **Friday:** `metrics-track` (pull weekly data) → `performance-report` → `trending-briefing`
9. **Monthly:** `profile-audit` → `presence-refresh`

## Independent Skills

These skills can run on their own without depending on the calendar pipeline:
- `meme-create` (run when trending format detected or engagement needs a boost)
- `engagement-poll` (run when audience research needed)
- `cross-post-adapt` (run when content needs platform-specific versions)
- `influencer-outreach` (run quarterly, independent of daily workflow)
- `ab-test-analyze` (run after enough A/B test data accumulates)
- `crisis-respond` / `apology-draft` / `impersonator-monitor` (event-driven, not scheduled)
