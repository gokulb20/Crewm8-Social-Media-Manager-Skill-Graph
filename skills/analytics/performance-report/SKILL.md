---
name: performance-report
description: Generate weekly and monthly performance summary reports — top/bottom posts, content type analysis, pillar performance, follower growth, conversion tracking, and actionable recommendations.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, analytics, reporting, performance, insights, executive]
related_skills: [metrics-track, ab-test-analyze, content-calendar, trending-briefing]
inputs_required: [metrics-data-for-period, ab-test-results-if-any, content-calendar-for-reference]
deliverables: [weekly-monthly-performance-report]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Performance Report

Generate structured weekly and monthly performance reports that turn raw metrics into actionable insights. The report answers three questions: what happened, why it happened, and what we should do differently.

## Purpose

A performance report that nobody reads is worse than no report at all. This skill produces reports designed for one specific reader — the founder — and answers exactly what they need to know in the order they need to know it.

## When to Use

- Weekly: Monday morning review of previous week
- Monthly: First week of month — trends across 4 weeks
- Campaign post-mortem: within 48 hours of campaign end
- Founder asks "how's social performing?"

## Inputs Required

- Metrics data for the period (from `metrics-track`)
- A/B test results (from `ab-test-analyze`)
- Content calendar (planned vs actual)
- Any external events that might have influenced performance

## Quick Reference

| Report Type | Frequency | Key Sections | Audience |
|------------|-----------|-------------|---------|
| Weekly Snapshot | Every Monday | Top/bottom posts, metrics summary, 1 insight, 1 action | Founder + team |
| Monthly Deep-Dive | First week of month | Trends, format analysis, growth trajectory, forecast | Founder + strategy |
| Campaign Post-Mortem | After campaign | Goals vs actuals, lessons, format winners | Founder + team |

## Procedure

1. **Gather data:** metrics, A/B test results, competitor benchmarks, content calendar.

2. **Build metrics summary:**
   - Total posts per platform
   - Total impressions
   - Average ER per platform
   - Follower growth (net + growth rate)
   - Link clicks / conversions
   - Compare to previous period

3. **Identify top 3 and bottom 3 posts:**
   - What made them work/fail (hook, format, timing, topic)?
   - Include the defining metric

4. **Analyze by content type:**
   - Threads vs short posts vs carousels vs videos — which format wins?
   - Has the winning format changed?

5. **Analyze by content pillar:**
   - Which pillars drive engagement vs conversions?
   - Is the pillar mix matching strategy?

6. **Track conversion funnel:** Impressions → engagement → profile visits → link clicks → signups.

7. **Extract 3-5 key learnings:**
   - What worked (do more)
   - What didn't (stop doing)
   - What to test next
   - Update always-on learnings doc

8. **Provide 2-3 actionable recommendations:**
   - Specific and testable (not "post more")
   - "Increase thread cadence from 2/week to 3/week targeting Tue/Thu mornings"

## Output Format

```markdown
# [Weekly / Monthly] Report: [Period]

## Executive Summary
[3-4 sentences — founder reads this in 30 seconds]

## Metrics at a Glance
| Metric | This Period | Last Period | % Change |
|--------|-----------|------------|----------|
| Total posts | [N] | [N] | [+/-N]% |
| Total impressions | [N] | [N] | [+/-N]% |
| Avg ER (X) | [N]% | [N]% | [+/-N]% |
| Avg ER (LinkedIn) | [N]% | [N]% | [+/-N]% |
| Follower growth | [+N] | [+N] | [+/-N]% |
| Link clicks | [N] | [N] | [+/-N]% |

## Top 3 Posts
### 1. [Title]
**Platform:** [X / LinkedIn / IG / TikTok] | **Format:** [Type]
**Impressions:** [N] | **ER:** [N]% | **Why it worked:** [Analysis]
### 2-3...

## Bottom 3 Posts
### 1. [Title]
**Impressions:** [N] | **ER:** [N]% | **Why it underperformed:** [Diagnosis]

## Format Analysis
| Format | Posts | Avg ER% | vs Overall |
|--------|-------|---------|-----------|
| Thread | [N] | [N]% | [+/-N]% |
...

## Pillar Performance
| Pillar | Posts | Avg ER% | Top Post |
|--------|-------|---------|----------|
...

## Key Learnings
1. [Specific learning with supporting data]
2-3...

## Recommendations
1. [Specific, actionable recommendation]
2-3...
```

## Done Criteria

The skill is complete when:
1. Executive summary is written (founder can read in 30 seconds)
2. Top and bottom 3 posts are identified with analysis
3. Format and pillar analysis are included
4. 3-5 key learnings are extracted
5. 2-3 actionable recommendations are provided
6. Always-on learnings doc is updated

## Pitfalls

- Data dump without insight (metrics without interpretation = noise)
- Comparing platforms naively (X ER != LinkedIn ER)
- Highlighting problems without solutions
- Cherry-picking favorable comparisons
- Report so long nobody reads it

## Verification

Can the founder read the executive summary and know whether it was a good week? Are there at least 2 actionable next steps? Does this report make the next content calendar smarter than the last one?
