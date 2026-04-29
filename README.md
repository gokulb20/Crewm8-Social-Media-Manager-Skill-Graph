# Hermes Social Manager Skill Pack

A comprehensive, granular skill pack for Hermes Agent covering all 12 functions of startup social media management. 37 discrete SKILL.md files organized by category with cross-references, platform-specific formatting rules, and chained workflow support.

## Installation

### Option 1: Install from a Git repository (recommended)

1. Push this folder to a GitHub repository:
   ```bash
   cd ~/Desktop/hermes-social-skills
   git init && git add . && git commit -m "Initial social manager skill pack"
   git remote add origin https://github.com/YOUR_USERNAME/hermes-social-skills.git
   git push -u origin main
   ```

2. Add the repository as a Hermes tap:
   ```bash
   hermes skills tap add YOUR_USERNAME/hermes-social-skills
   ```

3. Install individual skills as needed:
   ```bash
   hermes skills install YOUR_USERNAME/hermes-social-skills/skills/strategy/brand-voice-system
   ```

### Option 2: Copy directly to Hermes skills directory

```bash
cp -r ~/Desktop/hermes-social-skills/skills/* ~/.hermes/skills/
```

## Skill Index

### Category: Strategy

| # | Skill | Description |
|---|-------|-------------|
| 1 | brand-voice-system | Extract brand voice, build do/don't guide, detect drift |
| 2 | positioning-statement | Craft elevator pitch and niche positioning |
| 3 | content-pillars | Define 3-5 content pillars and topic taxonomy |

### Category: Planning

| # | Skill | Description |
|---|-------|-------------|
| 4 | content-calendar | Weekly/monthly day-by-day content plan |
| 5 | cadence-timing | Posting frequency and per-platform best times |

### Category: Creation

| # | Skill | Description |
|---|-------|-------------|
| 6 | post-create | Platform-native single posts for all four platforms |
| 7 | thread-create | Multi-tweet X threads with hooks, pacing, and CTAs |
| 8 | hook-write | Generate 5-10 hook variations for any content |
| 9 | cta-craft | Select and write optimal call-to-action per post |

### Category: Repurpose

| # | Skill | Description |
|---|-------|-------------|
| 10 | blog-to-thread | Blog post / newsletter into X thread |
| 11 | podcast-to-clips | Podcast transcripts into multi-platform social assets |
| 12 | newsletter-to-posts | Newsletter edition into standalone posts |

### Category: Visual

| # | Skill | Description |
|---|-------|-------------|
| 13 | visual-plan | Carousel slide-by-slide copy, banners, quote cards |
| 14 | meme-create | Branded meme concepts with text overlay and posting context |
| 15 | image-prompt | AI image prompts for Midjourney, DALL-E, SDXL |
| 16 | asset-format | Platform dimensions, safe zones, export settings |

### Category: Captions

| # | Skill | Description |
|---|-------|-------------|
| 17 | caption-draft | IG and LinkedIn captions with hooks, body, CTAs, hashtags |

### Category: Publishing

| # | Skill | Description |
|---|-------|-------------|
| 18 | schedule-queue | Queue posts to scheduling tools per platform timing |
| 19 | cross-post-adapt | One piece of content into platform-native variants |
| 20 | thread-structure | Thread sequencing, auto-plug, link placement rules |
| 21 | draft-review | Draft review queue + founder sign-off checklist |

### Category: Engagement

| # | Skill | Description |
|---|-------|-------------|
| 22 | comment-reply | Replies on own posts + value-add comments on others' |
| 23 | dm-respond | DM triage with categorization and response drafts |
| 24 | mention-monitor | Detect brand mentions, reply within 2-4 hours |
| 25 | influencer-outreach | Micro-influencer identification + cold outreach |
| 26 | engagement-poll | Design polls and audience questions |

### Category: Trends

| # | Skill | Description |
|---|-------|-------------|
| 27 | trend-monitor | Daily scan of trending topics, formats, hashtags |
| 28 | news-response | Quick-response posts to industry news |
| 29 | trending-briefing | Daily/weekly "what's trending" briefing for founder |

### Category: Analytics

| # | Skill | Description |
|---|-------|-------------|
| 30 | metrics-track | Post-level metrics tracking across all platforms |
| 31 | ab-test-analyze | A/B test analysis with winner declaration |
| 32 | performance-report | Weekly/monthly performance summary reports |

### Category: Crisis

| # | Skill | Description |
|---|-------|-------------|
| 33 | crisis-respond | Detect trolls, draft calm responses, escalation rules |
| 34 | apology-draft | Apology and correction posts with tone calibration |
| 35 | impersonator-monitor | Detect fake accounts, draft platform report copy |

### Category: Profile

| # | Skill | Description |
|---|-------|-------------|
| 36 | profile-audit | Cross-platform consistency check |
| 37 | presence-refresh | Bio optimization, pinned post rotation, banner updates |

---

## Function to Skill Mapping

| Function (from spec) | Skills that cover it |
|----------------------|---------------------|
| 1. Financial Operations | (Not covered — finance-specific; this pack is content/strategy/engagement) |
| 2. Content Creation | post-create, thread-create, hook-write, cta-craft |
| 3. Repurposing | blog-to-thread, podcast-to-clips, newsletter-to-posts |
| 4. Visual Assets | visual-plan, meme-create, image-prompt, asset-format |
| 5. Captions | caption-draft |
| 6. Scheduling & Publishing | schedule-queue, cross-post-adapt, thread-structure, draft-review |
| 7. Community Engagement | comment-reply, dm-respond, mention-monitor, influencer-outreach, engagement-poll |
| 8. Trend Monitoring | trend-monitor, news-response, trending-briefing |
| 9. Analytics & Reporting | metrics-track, ab-test-analyze, performance-report |
| 10. Crisis Management | crisis-respond, apology-draft, impersonator-monitor |
| 11. Profile Optimization | profile-audit, presence-refresh |
| 12. Brand Strategy | brand-voice-system, positioning-statement, content-pillars |

---

## Chained Workflow: Weekly Content Cycle

This is how skills chain together for a typical week:

```
brand-voice-system + positioning-statement + content-pillars
        |
        v
    cadence-timing
        |
        v
  content-calendar  <── trend-monitor (injects trending opportunities)
        |
        v
  post-create + thread-create + caption-draft
        |
        v
  blog-to-thread / podcast-to-clips / newsletter-to-posts (repurpose into more posts)
        |
        v
  visual-plan + image-prompt + asset-format (if visuals needed)
        |
        v
  draft-review (founder sign-off gate)
        |
        v
  thread-structure (if threads) + schedule-queue
        |
        v
  [POSTS GO LIVE]
        |
        v
  comment-reply + dm-respond + mention-monitor (daily engagement)
        |
        v
  metrics-track (daily pulls)
        |
        v
  performance-report + ab-test-analyze (weekly review)
        |
        v
  trending-briefing (founder update)
        |
        v
  profile-audit + presence-refresh (monthly/quarterly)
```

---

## Platform Coverage

Every applicable skill includes platform-specific guidance for:

- **X (Twitter):** 280-character limit, no markdown, line-break formatting, link placement rules, thread structure
- **LinkedIn:** 3,000-character limit, professional tone adjustment, carousel/PDF format, hashtag conventions
- **Instagram:** 2,200-character caption limit, visual-first, story format, link-in-bio constraints, hashtag strategy
- **TikTok:** Video-first, 9:16 format, text overlay timing, caption secondary to visual, trending audio integration

---

## Skill Format Reference

Every SKILL.md follows the Hermes Agent specification:

```yaml
---
name: skill-name
description: One-sentence description
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Category, Keywords]
    related_skills: [other-skill-names]
---
```

Body sections: **When to Use → Quick Reference → Procedure → Output Format → Pitfalls → Verification**

See [Hermes Agent Skill Creation Guide](https://hermes-agent.nousresearch.com/docs/developer-guide/creating-skills) for full documentation.

---

## Stats

- **Total skills:** 37
- **Categories:** 12
- **Platforms covered:** X, LinkedIn, Instagram, TikTok
- **Approximate total content:** ~11,000 lines of skill instruction

---

Built for Hermes Agent by Nous Research.
