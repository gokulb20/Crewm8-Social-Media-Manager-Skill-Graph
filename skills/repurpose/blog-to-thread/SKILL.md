---
name: blog-to-thread
description: Repurpose a blog post or newsletter into a high-performing X thread — extract top insights, write a scroll-stopping hook, and structure for maximum engagement.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, repurpose, blog, thread, x, long-form]
related_skills: [thread-create, hook-write, cta-craft, newsletter-to-posts]
inputs_required: [blog-post-url-or-full-text, target-cta]
deliverables: [thread-draft-with-traffic-strategy]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Blog to Thread

Transform long-form written content into X threads that drive traffic back to the original piece. A good thread does not summarize — it extracts the most shareable insights and packages them for the X format.

## Purpose

Your blog has insights your X audience has never seen. A thread is the bridge: extract the best parts into snackable tweets, tease the deeper analysis, and send people to the full piece. This is how content compounds.

## When to Use

- New blog post or newsletter just published
- Old high-performing post needs a second life
- Founder wrote a long piece and says "put this on X"
- Guest post published on another site (drive traffic back)
- Competitor published something worth responding to

## Inputs Required

- Full blog post text or URL
- Brand voice guide
- Target CTA (newsletter signup, product, full article)
- Link to full piece

## Quick Reference

| Source Length | Thread Length | Insight Density |
|--------------|--------------|----------------|
| 500-1,000 words | 5-7 tweets | Extract 3-5 insights |
| 1,000-2,000 words | 7-10 tweets | Extract 5-7 insights |
| 2,000+ words | 10-12 tweets max | Extract 7-9 insights |

## Procedure

1. **Read the full piece.** Do not skim. You can't extract the right insights without understanding the whole argument.

2. **Identify the 1-3 most quotable/surprising/contrarian moments:**
   - Data points with specific numbers
   - Counterintuitive claims
   - Frameworks (especially if distillable to 3-5 bullets)
   - Personal stories or specific examples

3. **Pick the thread angle using reuse patterns:**
   - Blog post: Extract top 5-7 insights, one per tweet
   - Case study: Challenge → What they tried → What worked → Results → Lesson
   - How-to guide: Step-by-step, one per tweet
   - Contrarian: Common belief → Why it's wrong → What works → Examples

4. **Write the hook tweet.** Lead with the single most interesting claim or stat. No warm-up. No context.

5. **Map insights to tweets:**
   - Tweet 2: Why this matters / credibility / context
   - Tweets 3-N-1: One specific insight per tweet
   - Final tweet: Summary + link to full article + CTA

6. **Ensure each tweet stands alone.** Someone should be able to retweet tweet 4 and it makes sense. No "as I mentioned above."

7. **Link in final tweet only.** Configure auto-plug for link-in-hook after engagement threshold (see `thread-structure`).

## Output Format

```markdown
# Thread from: [Blog Title]

## Source
[Title] — [URL]

## Top Extractable Insights
1. [Insight with specific data]
2. ...

## Thread Draft
[Full thread in thread-create output format]

## Traffic Strategy
- Link placement: final tweet only
- Auto-plug: add link to first tweet after [X likes / Y minutes]
- Follow-up: standalone tweet 2h after thread referencing a specific stat
```

## Done Criteria

The skill is complete when:
1. Thread hook is extracted from the most interesting content in the piece
2. Each insight maps to exactly one tweet
3. No tweet exceeds 280 characters
4. Each tweet works independently (no "as mentioned earlier")
5. Link placement and auto-plug rules are specified
6. Thread length is proportional to source length

## Pitfalls

- Summarizing instead of extracting (table of contents ≠ thread)
- Making the reader feel like they got everything from the thread (no reason to click)
- Extracting the wrong insights (what you find interesting vs. what the audience does)
- Too many insights per tweet (one per tweet is a rule)
- Forgetting to link to the source (the thread exists to drive traffic)

## Verification

Would this thread make sense to someone who hasn't read the blog? Would it make them WANT to read the blog? If either is "no," restructure.

## Example

*Input:* 2,000-word blog post: "The 5 pricing models every B2B SaaS founder should consider" — includes data on flat-rate vs. usage-based vs. tiered vs. per-seat vs. hybrid pricing.

*Output:* 10-tweet thread.
- Tweet 1: "5 pricing models for B2B SaaS. 1 kills growth. 1 scales infinitely. Here they are."
- Tweets 2-9: One model per tweet with data point + example + verdict
- Tweet 10: "The 5 models summarized: flat rate (simple, capped), usage (scales, complex), tiered (balanced), per-seat (standard), hybrid (best of both). Which one are you using? The full breakdown (with revenue impact data) → [link]"
