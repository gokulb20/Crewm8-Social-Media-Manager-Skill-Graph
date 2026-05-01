---
name: ab-test-analyze
description: Analyze A/B tests across hook variations, posting times, content formats, and CTAs — declare statistical winners, document learnings, and build an always-on optimization engine.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, analytics, ab-testing, experimentation, optimization, data-driven]
related_skills: [metrics-track, hook-write, cta-craft, performance-report]
inputs_required: [test-hypothesis, test-results-data, control-and-variant-descriptions]
deliverables: [ab-test-analysis-with-winner-declaration]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: ["EXTERNAL_ANALYTICS_LINK"]
required_env_vars: ["EXTERNAL_ANALYTICS_LINK"]
---

# A/B Test Analyze

Structure, run, and analyze A/B tests on social content to determine what actually drives better performance. Social media optimization without experimentation is superstition. This skill turns "I think this works" into "this works, and here's the data."

## Purpose

Every content decision is a guess until you test it. Hook variation A vs B, thread format vs short post, morning posting vs afternoon — this skill takes the guesswork out by running controlled experiments and declaring clear winners.

## When to Use

- Testing hook variations for the same content
- Testing posting times
- Testing formats (thread vs short post vs carousel)
- Testing CTAs
- After 2+ weeks with controlled variations

## Inputs Required

- Test hypothesis: "We believe [change] will improve [metric] by [X]%"
- Control condition description
- Variant condition description
- Result data (from `metrics-track`)

## Quick Reference

| Test Type | Control | Variant | Min Sample | Duration |
|-----------|---------|---------|-----------|---------|
| Hook A/B | Current hook style | New hook, same body | 2 per condition, same day of week, different weeks | 2 weeks |
| Time A/B | Current best time | Alternative time | 2 per condition | 2 weeks |
| Format A/B | Current format | Different format, same message | 2 per condition | 2 weeks |
| CTA A/B | Current CTA | Different CTA, same post | 2 per condition | 2 weeks |

## Procedure

1. **Define hypothesis clearly:**
   - "We believe [change] will improve [specific metric] by [X]%"
   - Example: "We believe leading with a statistic instead of a question will improve ER by 15%"
   - Bad hypothesis: "See what works better" (too vague)

2. **Design the test:**
   - Independent variable: what you're changing
   - Dependent variable: what you're measuring
   - Control: current version
   - Variant: new version
   - Controlled factors: same platform, day of week, topic weight

3. **Run minimum duration:**
   - Single-week tests unreliable (algorithm luck)
   - Min: 2 variations per condition over 2 weeks (4 data points per condition)
   - Never run two A/B tests simultaneously on the same platform (variable contamination)

4. **Analyze results:**
   - Average performance for control vs variant
   - Calculate % difference
   - Assess significance: >20% difference = significant; 10-20% = directional; <10% = inconclusive

5. **Declare winner:**
   - Clear winner: variant outperformed control by >20%
   - Directional: 10-20% — worth re-testing
   - Tie/conclusive: <10% — keep control
   - Loser: revert, document why

6. **Document learning:** What was tested, result, what to change, what to test next.

## Output Format

```markdown
# A/B Test: [Test Name]

## Design
**Hypothesis:** [Specific prediction]
**Variable:** [What changed]
**Metric:** [What was measured]
**Control:** [Condition]
**Variant:** [Condition]
**Platform:** [X / LinkedIn / IG / TikTok]
**Duration:** [Start to end]
**Sample:** [N posts per condition]

## Results
| Condition | Avg [Metric] | vs Control |
|-----------|-------------|------------|
| Control | [N] | — |
| Variant | [N] | [+/-N]% |

**Winner:** [Control / Variant / Inconclusive]

## Analysis
**What happened:** [Plain-English summary]
**Why:** [Theory]
**Confidence:** [High / Medium / Low]

## Decision & Next Steps
**Action:** [Adopt / Keep / Re-test]
**Implementation:** [What changes to make]
**Next test:** [What to test next]
```

## Done Criteria

The skill is complete when:
1. Hypothesis is specific and measurable
2. Test was designed with proper controls
3. Minimum sample size was met (4+ data points per condition)
4. Winner is declared with confidence assessment
5. Learning is documented for the always-on learnings doc

## Pitfalls

- Declaring winner from 1 data point per condition (anecdote, not test)
- Changing multiple variables at once (can't attribute result)
- Testing during abnormal weeks (holiday, launch, crisis)
- Cherry-picking data (confirmation bias)

## Verification

Would you bet $1,000 of the founder's money on this result being reproducible? If not, don't change strategy based on it yet.
