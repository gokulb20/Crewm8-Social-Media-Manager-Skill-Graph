---
name: performance-report
description: Generate weekly and monthly performance summary reports — top/bottom posts, content type analysis, follower growth, conversion tracking, and an always-on learnings document.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Analytics, Reporting, Performance, Learnings]
    related_skills: [metrics-track, ab-test-analyze, content-calendar]
---

# Performance Report

Generate structured weekly and monthly performance reports that turn raw metrics into actionable insights. The report should answer three questions: what happened, why it happened, and what we should do differently next week.

## When to Use

- Weekly: Monday morning review of the previous week's performance
- Monthly: First week of the month — review trends across 4 weeks
- Campaign post-mortem: within 48 hours of campaign end
- Founder asks "how's social performing?"
- Quarterly strategy review — pull all monthly reports for trend synthesis
- Pitching for more resources: "here's the data that justifies this investment"

## Quick Reference

| Report Type | Frequency | Key Sections | Audience |
|------------|-----------|-------------|---------|
| Weekly Snapshot | Every Monday | Top posts, bottom posts, metrics summary, 1 insight, 1 action | Founder + content team |
| Monthly Deep-Dive | First week of month | Trends, format analysis, growth trajectory, competitor benchmarks, forecast | Founder + strategy discussions |
| Campaign Post-Mortem | After campaign ends | Goals vs actuals, top performers, lessons, format winners | Founder + team |
| Quarterly Review | End of quarter | Long-term trends, strategy assessment, pillar effectiveness, next quarter plan | Founder + board/investors (potentially) |

## Procedure

1. Gather all data inputs:
   - `metrics-track` data for the reporting period
   - `ab-test-analyze` results from any active tests
   - Competitor benchmark data (from `competitor-audit` if available)
   - Content calendar — what was planned vs. what actually went out
   - Any external events that might have influenced performance

2. Build the top-level metrics summary:
   - Total posts per platform
   - Total impressions across all platforms
   - Average engagement rate per platform
   - Follower growth (net new, growth rate %)
   - Link clicks / conversion actions
   - Compare each metric to the previous period (% change)

3. Identify top 3 and bottom 3 posts overall:
   - Top posts: what made them work? (Hook? Topic? Format? Timing? Trend alignment?)
   - Bottom posts: what held them back? (Weak hook? Wrong time? Off-brand? Boring topic?)
   - For each: include the metric that defined its position

4. Analyze by content type:
   - Threads vs. short posts vs. carousels vs. videos — which format is winning?
   - Has the winning format changed from last period?
   - Is the brand over-indexing on a format that isn't performing?

5. Analyze by content pillar:
   - Which pillar is driving the most engagement?
   - Which pillar is driving the most conversions?
   - Is the pillar mix matching the strategy?

6. Track conversion funnel:
   - Impressions → engagement → profile visits → link clicks → signups/demos
   - Where is the biggest drop-off? (That's where to focus improvement)

7. Extract 3-5 key learnings:
   - What worked that we should do more of?
   - What didn't work that we should stop doing?
   - What's worth testing next week?
   - Update the "always-on learnings" document with each new insight

8. Provide 2-3 actionable recommendations for next period:
   - Each recommendation must be specific and testable
   - "Post more" is not a recommendation. "Increase thread cadence from 2/week to 3/week, targeting Tuesday and Thursday mornings" is.

## Output Format

```markdown
# [Weekly / Monthly] Performance Report: [Period]

## Executive Summary
[3-4 sentences — the TL;DR the founder can read in 30 seconds]

---

## Metrics at a Glance

| Metric | This Period | Last Period | % Change |
|--------|-----------|------------|----------|
| Total posts | [N] | [N] | [+/-N]% |
| Total impressions | [N] | [N] | [+/-N]% |
| Avg engagement rate (X) | [N]% | [N]% | [+/-N]% |
| Avg engagement rate (LinkedIn) | [N]% | [N]% | [+/-N]% |
| Avg engagement rate (IG) | [N]% | [N]% | [+/-N]% |
| Avg engagement rate (TikTok) | [N]% | [N]% | [+/-N]% |
| Follower growth | [+N] | [+N] | [+/-N]% |
| Link clicks | [N] | [N] | [+/-N]% |
| Conversions (if tracked) | [N] | [N] | [+/-N]% |

---

## Top 3 Posts

### 1. [Post title / hook truncated]
**Platform:** [X / LinkedIn / IG / TikTok]
**Format:** [Thread / Short post / Carousel / Video]
**Impressions:** [N] | **ER:** [N]% | **Link clicks:** [N]
**Why it worked:** [Specific analysis — was it the hook, the timing, a trending topic, the format?]

### 2. ...
### 3. ...

## Bottom 3 Posts

### 1. [Post title / hook truncated]
**Impressions:** [N] | **ER:** [N]%
**Why it underperformed:** [Diagnosis — weak hook? Bad timing? Off topic?]

### 2. ...
### 3. ...

---

## Format Analysis

| Format | Posts This Period | Avg ER% | vs. Overall Avg |
|--------|------------------|---------|----------------|
| Thread | [N] | [N]% | [+/-N]% |
| Short post | [N] | [N]% | [+/-N]% |
| Carousel | [N] | [N]% | [+/-N]% |
| Video | [N] | [N]% | [+/-N]% |

**Format winner this period:** [Format]

---

## Pillar Performance

| Pillar | Posts | Avg ER% | Top Post |
|--------|-------|---------|----------|
| Education | [N] | [N]% | [Title] |
| POV | [N] | [N]% | [Title] |
| Proof | [N] | [N]% | [Title] |
| BTS | [N] | [N]% | [Title] |
| CTA | [N] | [N]% | [Title] |

**Pillar mix:** [Education]% / [POV]% / [Proof]% / [BTS]% / [CTA]% (Target: [target mix])

---

## Key Learnings
1. [Specific learning with supporting data]
2. ...
3. ...

## Recommendations for Next Period
1. [Specific, actionable recommendation]
2. ...
3. ...

## Always-On Learnings Doc Updated
[Yes / No — link to doc if applicable]
```

## Pitfalls

- Report as data dump without insight (metrics without interpretation = noise)
- Comparing metrics across platforms naively (X ER is not comparable to LinkedIn ER — different engagement patterns)
- Highlighting problems without proposing solutions (report should drive action, not just document failure)
- Cherry-picking favorable comparisons from the previous period (honesty > looking good)
- Report so long nobody reads it (founder wants the highlights, not the spreadsheet)
- Not updating the always-on learnings doc (the same insight will be "discovered" every month)

## Verification

Can the founder read the executive summary and know whether it was a good week or bad week? Are there at least 2 actionable recommendations? Are the learnings specific enough that they could change what gets created next week? Does this report make the next `content-calendar` smarter than the last one?
