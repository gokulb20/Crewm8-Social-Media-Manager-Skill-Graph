---
name: metrics-track
description: Track post-level metrics across all platforms — impressions, engagement rate, profile clicks, follows, and conversion metrics — with weekly summaries and trend detection.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Analytics, Metrics, Tracking, Data]
    related_skills: [ab-test-analyze, performance-report, cadence-timing]
---

# Metrics Track

Pull and track post-level metrics across every platform. Data without tracking is just guessing. This skill defines what to measure, how to pull it, and how to interpret it so the brand knows what's working and what isn't.

## When to Use

- Daily metrics pull for recently published posts
- Weekly aggregation for performance reporting
- Before the weekly `performance-report` generation
- After a campaign or launch — pull campaign-specific metrics
- Founder asks "how are we doing on social?"

## Quick Reference

| Metric | What It Measures | Platform Availability | Why It Matters |
|--------|-----------------|----------------------|---------------|
| Impressions | How many times content was shown | All platforms | Top of funnel — are we being seen? |
| Engagement rate | (Likes+comments+shares+saves) / impressions | All platforms | Content quality — are people responding? |
| Engagement per post | Absolute likes + comments + shares + saves | All platforms | Which specific posts perform? |
| Profile visits | Clicks to profile from content | X, LinkedIn, IG | Brand interest — are people exploring? |
| Follows / audience growth | New followers gained (net) | All platforms | Growth — is the audience expanding? |
| Link clicks | Clicks on links in bio/posts | X, LinkedIn | Traffic — is content driving action? |
| Saves / bookmarks | Posts saved for later | IG, LinkedIn, X | Value density — was this worth keeping? |
| Shares / reposts | Content shared by others | All platforms | Virality — did this break out of our audience? |
| Replies / comments | Number of comments generated | All platforms | Conversation — are we sparking discussion? |
| Video retention | % of video watched | IG, TikTok, X | Video quality — are people watching all the way through? |

## Procedure

1. Set up metrics collection:
   - Platform-native analytics: X Analytics, LinkedIn Analytics, Instagram Insights, TikTok Analytics
   - Third-party: Buffer Analytics, Hypefury analytics, Typefully, Fathom (link tracking)
   - Manual extraction: export CSVs from each platform for custom aggregation if needed
   - Define the standard "metrics pull window" (every Monday for last week, plus daily for real-time)

2. For each post, pull:
   - Post-level: impressions, likes, comments, shares, saves, link clicks
   - Profile-level: profile visits, follows gained, follows lost (net growth)
   - Video-specific: views, average watch time, completion rate
   - Platform-specific: any unique metrics the platform offers

3. Calculate derived metrics:
   - Engagement rate = (likes + comments + shares + saves) / impressions * 100
   - Follower growth rate = (new followers - lost followers) / total followers * 100
   - Click-through rate = link clicks / impressions * 100
   - Save rate = saves / impressions * 100

4. Build a running metrics database:
   - Track every post with its metrics for at least 90 days
   - Store: post ID, platform, date, format, pillar, hook type, metrics
   - This database is what powers `ab-test-analyze` and `performance-report`

5. Establish baselines and benchmarks:
   - Average engagement rate per platform (over last 30 days)
   - Average impressions per post type (thread, short post, carousel, video)
   - Average follower growth per week
   - Identify "normal" range — so you can spot anomalies (good or bad)

6. Flag anomalies:
   - Any post performing 2x above baseline (investigate: what made it work?)
   - Any post performing below 50% of baseline (investigate: what broke?)
   - Sudden follower growth spike or drop (what caused it?)

## Output Format

```markdown
# Metrics Track: [Week of Date]

## Weekly Snapshot

### X (Twitter)
| Post | Impressions | Likes | Comments | Shares | Saves | ER% | Link Clicks |
|------|------------|-------|----------|--------|-------|-----|------------|
| [Title/hook] | [N] | [N] | [N] | [N] | [N] | [N]% | [N] |
...

**Weekly averages:** Impressions [N], ER [N]%, Link clicks [N]
**vs. baseline:** [+X% / -X%]

### LinkedIn
...

### Instagram
...

### TikTok
...

## Anomaly Flags
- **Overperformer:** [Post] — [ER% vs baseline]. Why? [Hypothesis]
- **Underperformer:** [Post] — [ER% vs baseline]. Why? [Hypothesis]

## Follower Growth
| Platform | Start | End | Net Change | Growth Rate |
|----------|-------|-----|------------|-------------|
| X | [N] | [N] | [+/-N] | [N]% |
...

## Running Benchmarks (Last 30 Days)
| Platform | Avg ER% | Avg Impressions/Post | Best Format | Best Day/Time |
|----------|---------|---------------------|-------------|---------------|
| X | [N]% | [N] | [Format] | [Day/Time] |
...
```

## Pitfalls

- Tracking vanity metrics (impressions without engagement) and calling it success
- Not differentiating between organic and paid reach (they're different games)
- Comparing engagement rates across platforms directly (X ER ≠ LinkedIn ER ≠ IG ER — different baselines)
- Pulling metrics too early (post under 6 hours old doesn't have reliable data yet)
- Not tracking saves/bookmarks (they're the strongest signal of value density)
- Ignoring video retention (3,000 views at 5% retention = people clicked away instantly)

## Verification

Are you tracking the SAME metrics every week for the SAME period? (Inconsistent tracking = garbage comparisons.) Can you answer "what was our best post this week and why?" from this data? Can you answer "are we growing faster or slower than last month?"
