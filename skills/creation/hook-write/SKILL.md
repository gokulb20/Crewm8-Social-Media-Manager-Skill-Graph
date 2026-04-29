---
name: hook-write
description: Generate 5-10 hook variations for any post, thread, or caption across X, LinkedIn, Instagram, and TikTok — using different styles (question, contrarian, statistic, story, observation, promise) so the best one can be tested or selected.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, creation, hooks, attention, writing, optimization]
related_skills: [post-create, thread-create, caption-draft, cta-craft, ab-test-analyze]
inputs_required: [core-idea-or-topic, target-platform, target-audience-pain-point]
deliverables: [hook-variations-with-scores-and-recommendations]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Hook Write

Generate high-performing hooks for any content type and platform. The hook is the single most important element — if nobody stops scrolling, the rest doesn't matter. This skill produces multiple variations so the best one can be A/B tested or selected.

## Purpose

90% of the post's success is determined before the reader finishes the first sentence. Most failed posts aren't bad posts — they have bad hooks. This skill separates the hook from the body so each can be optimized independently.

## When to Use

- Before writing any post or thread (hook-first writing)
- A/B testing variations (deploy 2 versions, measure which wins)
- Existing post underperformed — diagnose if the hook was the problem
- Content calendar needs hooks drafted in advance
- Founder says "I have an idea" but doesn't know how to open

## Inputs Required

- Core idea (one sentence — what this content communicates)
- Target platform
- Desired emotional reaction (curiosity, recognition, urgency, validation)
- Brand voice constraints (any hook styles that are off-limits)

## Quick Reference

| Hook Style | Pattern | Best Platform | Example |
|-----------|---------|--------------|---------|
| Promise | "I [did X]. Here's what I found" | X, LinkedIn | "I analyzed 100 pricing pages. Found 3 patterns." |
| Contrarian | "[Common belief] is wrong" | X, LinkedIn | "Everyone says niche down. Here's when you shouldn't." |
| Statistic / Lede | Lead with a surprising number | X, LinkedIn | "97% of cold outreach gets no reply. The 3% share one trait." |
| Story Hook | Start mid-narrative | X, LinkedIn, IG | "We hit $10K MRR. Then almost lost it all." |
| Question | Ask a provocative question | LinkedIn, IG | "What's the one metric that actually changed your decisions?" |
| Observation | State the unstated | X, LinkedIn | "The best founders I know are terrible at celebrating wins." |
| How-to Promise | "How to [X] without [Y]" | LinkedIn, IG, TikTok | "How to price your SaaS without guesswork." |
| Pattern Interrupt | Unexpected format/opener | IG, TikTok | Visual hook saying the opposite of what you'd expect |

## Procedure

1. **Define the core idea.** One sentence: "This post is about [X] and the reader should feel [Y]."

2. **Select the target emotion:**
   - Curiosity ("I need to know more")
   - Recognition ("That's exactly me")
   - Intrigue ("Wait, is that true?")
   - Urgency ("I need this now")
   - Validation ("Someone finally said it")

3. **Generate 5-10 hooks across 5-6 styles** (selecting the most suitable for platform and topic):
   - At least 1 Promise-style
   - At least 1 Contrarian-style
   - At least 1 Story-style (if applicable)
   - At least 1 Question-style (for LinkedIn/IG)
   - At least 1 Statistic/Number-led (if data available)
   - At least 1 Observation-style (for X)

4. **Adapt each hook to the target platform:**
   - X: First 3-5 words are everything. Max 280 chars total.
   - LinkedIn: First 2 lines (before "see more"). Tease without clickbait.
   - IG: Hook works with the visual. First line of caption is critical.
   - TikTok: Text overlay + first 1.5 seconds of audio/visual.

5. **Score each hook on:**
   - Curiosity gap: does it make you need to know more? (1-10)
   - Specificity: is it concrete vs. generic? (1-10)
   - Brand-fit: does it sound like the brand? (1-10)
   - Platform-fit: does it follow platform rules? (1-10)

6. **Rank and recommend.** Top 2 hooks: one primary pick + one A/B challenger.

## Output Format

```markdown
# Hook Variations: [Post Topic / Platform]

## Core Idea
[One sentence — what this post is about]

## Hook Variations

### 1. [Style: Promise/Contrarian/etc.]
[Hook text, formatted for platform]
**Curiosity:** [1-10] **Specificity:** [1-10] **Brand-fit:** [1-10] **Platform-fit:** [1-10]

### 2. [Style]
...

## Top Picks
1. **Recommended:** [Hook + why]
2. **A/B challenger:** [Alternate + why]

## Platform Adaptations
- X version: [shorter, punchier]
- LinkedIn version: [slightly more professional framing]
- IG version: [visual-led version]
- TikTok version: [text overlay + hook timing]
```

## Done Criteria

The skill is complete when:
1. At least 5 hook variations exist across different styles
2. Each hook is formatted for the target platform
3. Hooks are scored on all 4 dimensions
4. A primary and challenger hook are recommended
5. Platform adaptations are provided (if applicable)

## Pitfalls

- Hooks that overpromise ("This one trick will 10x your revenue") — kills trust
- Hooks that are all sizzle, no steak (the post doesn't deliver on the promise)
- Question hooks where the audience already knows the answer
- Clickbait that would embarrass the founder
- Using the same hook style for every post (pattern fatigue)

## Verification

For each top hook: what does it promise? Does the actual post deliver that exact promise? If the answer is "sort of," rewrite either the hook or the post until it's a clean match.

## Example

*Input:* Topic = "Why most SaaS startups fail at cold email." Platform = X. Emotion = curiosity + recognition.

*Output:*
1. (Promise) "I read 50,000 cold emails. Here are the 3 that booked meetings." — Curiosity: 9, Specificity: 9, Brand-fit: 8, Platform-fit: 10
2. (Contrarian) "Everyone tells you to personalize cold emails. That's wrong." — Curiosity: 8, Specificity: 8, Brand-fit: 7, Platform-fit: 9
3. (Statistic) "97% of cold emails get ignored. The 3% that work share 1 pattern." — Curiosity: 9, Specificity: 9, Brand-fit: 8, Platform-fit: 10
4. (Story) "I sent 1,000 cold emails. Got 2 replies. Here's what I changed." — Curiosity: 7, Specificity: 8, Brand-fit: 8, Platform-fit: 9
5. (Observation) "The cold emails that work don't look like cold emails." — Curiosity: 7, Specificity: 7, Brand-fit: 9, Platform-fit: 10

Recommended: #3 (statistic-led, highest combined score). Challenger: #2 (contrarian, different angle).
