---
name: blog-to-thread
description: Repurpose a blog post or newsletter into a high-performing X thread — extract top insights, write a scroll-stopping hook, and structure for maximum engagement.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Repurpose, Blog, Thread, X]
    related_skills: [thread-create, hook-write, cta-craft, newsletter-to-posts]
---

# Blog to Thread

Transform long-form written content (blog posts, newsletters, articles) into X threads that drive traffic back to the source. A good thread does not summarize — it extracts the most shareable insights and packages them for the X format.

## When to Use

- New blog post or newsletter just published
- Old high-performing blog post needs a second life on social
- Founder wrote a long piece and says "can you put this on X?"
- Guest post published on another site (drive traffic back)
- Competitor published something you want to respond to with your own perspective

## Quick Reference

| Source Length | Thread Length | Insight Density |
|--------------|--------------|----------------|
| 500-1,000 words | 5-7 tweets | Extract 3-5 insights |
| 1,000-2,000 words | 7-10 tweets | Extract 5-7 insights |
| 2,000+ words | 10-12 tweets max | Extract 7-9 insights |

## Procedure

1. Read the full source content. Do not skim. You cannot extract the right insights without understanding the whole piece.

2. Identify the 1-3 most quotable/surprising/contrarian lines in the piece:
   - Data points with specific numbers
   - Counterintuitive claims
   - Frameworks (especially if you can distill to 3-5 bullets)
   - Personal stories or specific examples

3. Determine the thread angle using the reuse patterns table:
   - Blog post: extract top 5-7 insights, one per tweet
   - Product launch: Problem → Old way → Our way → Proof → CTA
   - Case study: Challenge → What they tried → What worked → Results → Lesson
   - Contrarian take: Common belief → Why it's wrong → What actually works → Examples
   - How-to guide: Step-by-step, one step per tweet, tools/suggestions
   - Revenue update: Number → Breakdown → What worked → What failed → What's next

4. Write the hook tweet:
   - Find the single most interesting claim or stat from the piece
   - Lead with it. No warm-up. No context.
   - If the blog has a great headline, steal it (you're the same brand)

5. Map insights to tweets:
   - Tweet 2: Why this matters / credibility / context
   - Tweets 3 through N-1: One specific insight per tweet
   - Final tweet: Summary + link to full article + CTA

6. Ensure each tweet can stand alone:
   - Someone should be able to retweet tweet 4 and it makes sense on its own
   - No "as I mentioned above" — each tweet is a self-contained unit

7. Add the "read the full piece" link in the final tweet only.

8. Pass to `thread-create` for formatting, quality checklist, and auto-plug rules.

## Output Format

```markdown
# Thread from: [Blog Title / URL]

## Source
[Title] — [URL]

## Top Extractable Insights
1. [Insight with specific data/quote if available]
2. ...

## Thread Draft
[Full thread in thread-create output format]

## Traffic Strategy
- Link placement: final tweet only
- Auto-plug: add link to first tweet after [X likes / Y minutes]
- Follow-up: post a standalone tweet 2 hours after thread referencing a specific stat from the article
```

## Pitfalls

- Summarizing instead of extracting — "the blog said X" is not a thread, it's a table of contents
- Making the reader feel like they got the whole article in the thread (no reason to click through)
- Extracting the wrong insights (the ones you find interesting vs. the ones the X audience finds interesting)
- Too many insights jammed into one tweet (one per tweet is a rule, not a suggestion)
- Forgetting to link to the source (the thread exists to drive traffic)

## Verification

Would this thread make sense to someone who hasn't read the blog? Would it make them WANT to read the blog? If the answer to either is "no," restructure.
