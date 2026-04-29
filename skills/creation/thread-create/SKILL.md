---
name: thread-create
description: Create multi-tweet X threads that hook hard, deliver escalating value across 6-10 tweets, and close with a clear CTA — optimized for X's format, algorithm, and reading behavior.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, creation, threads, x, long-form, writing]
related_skills: [hook-write, cta-craft, post-create, blog-to-thread, thread-structure]
inputs_required: [thread-topic-or-source-material, brand-voice-guide, target-cta]
deliverables: [full-thread-draft-with-auto-plug-config]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Thread Create

Build an X thread that earns every read and every retweet. Threads are the highest-leverage format on X for education, storytelling, and authority-building. A weak thread is worse than no thread — it trains the algorithm that your content isn't worth surfacing.

## Purpose

A 7-tweet thread can generate more authority than 14 individual posts. But only if every tweet earns its place. This skill produces threads that hook immediately, escalate through each tweet, and close with a satisfying CTA.

## When to Use

- Converting a blog post or newsletter into a thread
- Sharing a framework, system, or hard-won insight
- Product launch narrative
- Contrarian take that needs more than 280 characters to land
- Case study or results breakdown
- Content calendar calls for an education/POV thread

## Inputs Required

- Source material (blog post, idea, framework, case study notes)
- Brand voice guide
- Target length (6-10 tweets optimal)
- Link/CTA for final tweet
- Any data points or visuals to include

## Quick Reference

| Thread Element | Rule |
|---------------|------|
| Length | 6-10 tweets optimal. Under 5 = "long tweet." Over 12 = loses readers. |
| Hook tweet | First 3 words must stop scroll. No links. No hashtags. |
| Body tweets | One idea per tweet. Use line breaks aggressively. |
| Pacing | Escalate insight/value with each tweet. Don't front-load. |
| Final tweet | Summary + CTA. Link (if any) goes here. |
| Visuals | 1 image/chart max. Place in tweet 2-4 (visible in timeline preview). |
| Auto-plug | Add link to first tweet AFTER engagement threshold (see `thread-structure` skill). |

## Procedure

1. **Identify the thread angle from source material** using reuse patterns:
   - Blog post: extract top 5-7 insights, one per tweet
   - Product launch: Problem → Old way → Our way → Proof → CTA
   - Case study: Challenge → What they tried → What worked → Results → Lesson
   - Contrarian take: Common belief → Why it's wrong → What works → Examples
   - How-to guide: Step-by-step, one per tweet
   - Revenue update: Number → Breakdown → What worked → What failed → What's next

2. **Write the hook tweet (tweet 1):**
   - Lead with strongest word or number
   - No links, no hashtags
   - Avoid: "Here's what I learned about X" (weak), "A thread" (wastes characters)
   - 3 proven styles:
     - The Promise: "I analyzed 100 SaaS pricing pages. Found 3 patterns"
     - The Contrarian: "Everyone tells you to niche down. Here's when you shouldn't"
     - The Story Hook: "We hit $10K MRR. Then almost lost it all"

3. **Write the body (tweets 2 through N-1):**
   - Tweet 2: Establish credibility or context. Why should they trust you?
   - Tweets 3-7: Core content. One specific idea per tweet.
   - Escalate: each tweet builds toward something bigger
   - Use line breaks for visual rhythm
   - Place visual/chart in tweet 2-4

4. **Write the final tweet:**
   - Summarize key takeaway in one line
   - Clear CTA: follow, newsletter, reply
   - Link goes here, not in first tweet
   - Make it satisfying — trails off = wasted thread

5. **Quality checklist:**
   - Hook strength: does tweet 1 make you NEED to click "Show this thread"?
   - Value density: no filler, every tweet earns its place
   - Flow: does each tweet naturally lead to the next?
   - CTA: is the last tweet clear and actionable?
   - Fact check: any claims need sources?

6. **Configure auto-plug.** Link goes in hook tweet's reply AFTER engagement threshold (see `thread-structure`).

## Output Format

```markdown
🧵 THREAD: [Title/topic]

Tweet 1: [full text]
Tweet 2: [full text]
...
Final Tweet: [full text + CTA]

---
Hook strength: [brief assessment]
Expected engagement: [low/medium/high]
Best posting time: [recommendation]
Follow-up post: [suggest a standalone tweet 2h after thread]
Visual recommendation: [image/chart idea + placement]
Auto-plug link: [link + trigger rule]
```

## Done Criteria

The skill is complete when:
1. Full thread text exists for all tweets (6-10)
2. Tweet 1 has no links or hashtags
3. Each tweet is under 280 characters
4. Each tweet can stand alone (retweetable without context)
5. Final tweet has a clear CTA + link (if applicable)
6. Auto-plug rule is specified (see `thread-structure`)

## Pitfalls

- Weak hooks: "Here's what I learned about X" is not a hook
- Wall of text: use line breaks liberally
- Auto-plugging too early: wait for engagement
- Threads that don't end: every thread needs a clear conclusion + CTA
- Being too generic: specific > broad, examples > abstract claims
- First tweet over 280 characters (breaks thread unfolding)

## Verification

Read the hook tweet alone. Would you click "Show this thread"? Count filler words across all tweets — cut them. Does tweet 2 deliver on the promise of tweet 1? Does the final tweet feel like an ending or did it just stop?

## Example

*Input:* Blog post about "Why most SaaS cold outreach fails" — 2,000 words. 3 data points, 1 framework, 3 actionable tips.

*Output:* 8-tweet thread.
- Tweet 1 (hook): "I analyzed 10,000 cold outreach emails. 97% got ignored. The 3% that worked shared 1 thing."
- Tweet 2: "Most people think cold outreach fails because of timing. Wrong. It fails because it's lazy."
- Tweets 3-7: Each covers one insight from the data analysis
- Tweet 8 (final): "Summary: personalize early, value-first, tiny ask. Follow for more outreach breakdowns. Full framework in the newsletter — link below."
- Auto-plug: Add newsletter link to tweet 1 reply after 20 likes or 60 min.
