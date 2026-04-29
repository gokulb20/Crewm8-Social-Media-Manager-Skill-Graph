---
name: ab-test-analyze
description: Analyze A/B tests across hook variations, posting times, content formats, and CTAs — declare statistical winners, document learnings, and apply insights to future content.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Analytics, A/B-Testing, Experimentation, Optimization]
    related_skills: [metrics-track, hook-write, cta-craft, performance-report]
---

# A/B Test Analyze

Structure, run, and analyze A/B tests on social content to determine what actually drives better performance. Social media optimization without experimentation is superstition. This skill turns "I think this works" into "this works, and here's the data."

## When to Use

- Testing hook variations for the same content (post A vs post B, different hooks)
- Testing posting times (same post, same platform, two different time slots on different weeks)
- Testing formats (same message as thread vs. short post vs. carousel)
- Testing CTAs ("follow for more" vs "reply with your take" vs "save for later")
- After any 2+ week period with controlled variations — run analysis
- Founder asks "should we [change something]?" — test it instead of guessing

## Quick Reference

| Test Type | Control Group | Variant | Minimum Sample | Duration |
|-----------|--------------|---------|---------------|---------|
| Hook A/B | Post with current hook style | Post with new hook style, same body | 2 posts each, same day of week, different weeks | 2 weeks (4 posts total) |
| Time A/B | Post at current best time | Same post at alternative time | 2 posts each, different weeks | 2 weeks (4 posts total) |
| Format A/B | Post in current format | Same message in different format | 2 posts each, same platform, different weeks | 2 weeks |
| CTA A/B | Post with current CTA | Same post with different CTA | 2 posts each | 2 weeks |
| Visual vs. text | Post with image | Same post text-only | 2 posts each | 2 weeks |
| Thread length A/B | 6-tweet thread | 10-tweet thread (same topic) | 2 threads | 2-4 weeks |

## Procedure

1. Define the test hypothesis clearly:
   - "We believe [change] will improve [specific metric] by [X]%"
   - Example: "We believe leading with a statistic instead of a question will improve engagement rate by 15%"
   - Bad hypothesis: "We want to see what works better" (too vague to act on)

2. Design the test:
   - What's the independent variable? (the thing you're changing)
   - What's the dependent variable? (the metric you're measuring)
   - What's the control? (the current version)
   - What's the variant? (the new version)
   - How will you control for confounding factors? (same platform, same day of week, similar topic weight)

3. Run the test over the minimum duration:
   - Single-week tests are unreliable (one post could have algorithmic luck)
   - Minimum: 2 variations each over 2 weeks (4 total data points per condition)
   - Better: 4 variations each over 4 weeks (8+ data points per condition)
   - NEVER run two A/B tests simultaneously on the same platform (variables contaminate each other)

4. Collect data from `metrics-track`:
   - Primary metric: the one directly tied to the hypothesis
   - Secondary metrics: related metrics that might also be affected
   - Control for outlier posts (exclude posts that went unexpectedly viral for external reasons)

5. Analyze results:
   - Calculate average performance for control group vs variant group
   - Compute % difference
   - Assess significance (is the difference big enough to be real, not random noise?)
   - Rule of thumb for social A/B: >20% difference = significant; 10-20% = directional; <10% = inconclusive

6. Declare a winner:
   - Clear winner: variant outperformed control by >20% on primary metric
   - Directional: variant outperformed control by 10-20% — worth testing again
   - Tie / inconclusive: difference <10% — keep the control, or re-test with bigger sample
   - Loser: variant underperformed control — revert, document why

7. Document the learning:
   - What was tested
   - What was the result
   - What should change going forward
   - What should be tested next

## Output Format

```markdown
# A/B Test Analysis: [Test Name]

## Test Design
**Hypothesis:** [Specific prediction — "we believe X will improve Y by Z%"]
**Independent variable:** [What we changed]
**Dependent variable:** [Primary metric we measured]
**Control:** [Description of control condition]
**Variant:** [Description of variant condition]
**Platform:** [X / LinkedIn / IG / TikTok]
**Duration:** [Start date to end date]
**Sample size:** [N] posts per condition

---

## Results

### Primary Metric: [Metric name]

| Condition | Post 1 | Post 2 | Post 3 | Post 4 | Average |
|-----------|--------|--------|--------|--------|---------|
| Control | [N] | [N] | [N] | [N] | [N] |
| Variant | [N] | [N] | [N] | [N] | [N] |

**Difference:** [+/-N]% 
**Winner:** [Control / Variant / Inconclusive]

### Secondary Metrics

| Metric | Control Avg | Variant Avg | % Change |
|--------|-----------|------------|----------|
| [Metric] | [N] | [N] | [+/-N]% |
...

---

## Analysis & Interpretation

**What happened:** [Plain-English summary of results]

**Why it might have happened:** [Theory — why did the variant win/lose?]

**Confidence level:** [High / Medium / Low] — [why]

**Confounding factors:** [Any external events that might have influenced results? Algorithm changes, news events, seasonal effects?]

---

## Decision & Next Steps

**Action:** [Adopt variant / Keep control / Re-test]
**Implementation:** [What changes to make to future content based on this test]
**Next test:** [What to test next — A/B testing is continuous]

**Added to learnings doc:** [Yes / No — reference to always-on learnings document]
```

## Pitfalls

- Declaring a "winner" from 1 data point per condition (that's not a test, that's an anecdote)
- Changing multiple variables at once (you can't know which change caused the result)
- Testing things the audience can't perceive (font size on carousel slide 3 — nobody will notice)
- Testing during abnormal weeks (holidays, product launches, crises — everything is skewed)
- Running A/B tests without controlling for topic weight (comparing a hot-take post to a mild educational post = not a fair test)
- Cherry-picking data that supports the hypothesis (confirmation bias kills learning)

## Verification

Can you answer: what changed, what was measured, how big was the difference, and is it big enough to be real? Would you bet $1,000 of the founder's money on this result being reproducible? If not, don't change strategy based on it yet.
