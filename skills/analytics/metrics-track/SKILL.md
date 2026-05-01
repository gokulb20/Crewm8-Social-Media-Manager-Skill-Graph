---
name: metrics-track
description: Track post-level metrics across all platforms — impressions, engagement rate, profile clicks, follows, link clicks — with weekly aggregation and trend detection for performance analysis.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, analytics, metrics, tracking, data, reporting]
related_skills: [ab-test-analyze, performance-report, cadence-timing]
inputs_required: [platform-analytics-access, post-list-for-tracking-period]
deliverables: [metrics-snapshot-with-anomaly-flags]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: ["EXTERNAL_ANALYTICS_LINK"]
required_env_vars: ["EXTERNAL_ANALYTICS_LINK"]
---

# Metrics Track

Pull and track post-level metrics across every platform. Data without tracking is just guessing. This skill defines what to measure, how to pull it, and how to interpret it so the brand knows what's actually working.

## Purpose

Most social media managers track everything and understand nothing. This skill focuses on the metrics that matter — engagement rate (quality), follower growth (reach), link clicks (conversion) — and flags anomalies worth investigating.

## When to Use

- Daily pull for recently published posts
- Weekly aggregation for performance reporting
- Before `performance-report` generation
- After a campaign or launch

## Inputs Required

- Platform analytics access (native or third-party)
- List of posts for the tracking period
- Historical baselines (for anomaly detection)

## Quick Reference

| Metric | What It Measures | Why It Matters |
|--------|-----------------|---------------|
| Impressions | How many times content was shown | Top of funnel — are we being seen? |
| Engagement rate | (Likes+comments+shares+saves) / impressions | Content quality — are people responding? |
| Profile visits | Clicks to profile from content | Brand interest — are people exploring? |
| Follows / growth | New followers (net) | Is the audience expanding? |
| Link clicks | Clicks on links | Is content driving action? |
| Saves / bookmarks | Posts saved for later | Value density — worth keeping? |
| Shares / reposts | Content shared by others | Virality potential |
| Video retention | % of video watched | Video quality |

## Procedure

1. **Pull metrics per post:** impressions, likes, comments, shares, saves, link clicks, profile visits, follows.

2. **Calculate derived metrics:**
   - ER% = (likes + comments + shares + saves) / impressions * 100
   - Follower growth rate = net new / total followers * 100
   - CTR = link clicks / impressions * 100

3. **Build running database:** Track every post with metrics for 90+ days. Store: post ID, platform, date, format, pillar, hook type, metrics.

4. **Establish baselines:**
   - Average ER per platform (trailing 30 days)
   - Average impressions per post type
   - Average weekly follower growth
   - "Normal" range for anomaly detection

5. **Flag anomalies:**
   - 2x above baseline (investigate what worked)
   - Below 50% of baseline (investigate what broke)
   - Sudden follower spike or drop

## Output Format

```markdown
# Metrics Track: [Week]

## Weekly Snapshot
| Platform | Avg Impressions | Avg ER% | Best Post | Worst Post | Follower Change |
|----------|----------------|---------|-----------|------------|----------------|
| X | [N] | [N]% | [Title] | [Title] | [+N] |
| LinkedIn | [N] | [N]% | [Title] | [Title] | [+N] |
| IG | [N] | [N]% | [Title] | [Title] | [+N] |
| TikTok | [N] | [N]% | [Title] | [Title] | [+N] |

## Anomaly Flags
- **Overperformer:** [Post] — [ER% vs baseline]. Why? [Hypothesis]
- **Underperformer:** [Post] — [ER% vs baseline]. Why? [Hypothesis]

## Running Benchmarks (30 Days)
| Platform | Avg ER% | Best Format | Best Day/Time |
|----------|---------|-------------|---------------|
| X | [N]% | [Format] | [Day/Time] |
...
```

## Done Criteria

The skill is complete when:
1. Metrics are pulled for all posts in the tracking period
2. ER%, growth rate, and CTR are calculated
3. Anomalies are flagged (overperformers and underperformers)
4. Running benchmarks are updated
5. Data is ready for `performance-report`

## Pitfalls

- Tracking vanity metrics (impressions without engagement)
- Comparing ER across platforms directly (X ER != LinkedIn ER != IG ER)
- Pulling metrics too early (post under 6 hours old isn't reliable)
- Not tracking saves/bookmarks (strongest signal of value density)
- Ignoring video retention

## Verification

Can you answer "what was our best post this week and why?" from this data? Can you answer "are we growing faster or slower than last month?" If not, the tracking is incomplete.
