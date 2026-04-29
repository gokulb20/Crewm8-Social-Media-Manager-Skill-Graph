---
name: newsletter-to-posts
description: Repurpose a newsletter edition into 3-5 standalone posts across X, LinkedIn, and Instagram — extracting individual insights, stories, or frameworks as native social content.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, repurpose, newsletter, multi-platform, content-bank]
related_skills: [post-create, thread-create, blog-to-thread, caption-draft]
inputs_required: [newsletter-full-text, newsletter-subscribe-link, brand-voice-guide]
deliverables: [multi-post-package-with-posting-sequence]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# Newsletter to Posts

Turn one newsletter edition into a week's worth of standalone social posts. Newsletters typically contain 3-5 distinct sections, each of which can become its own platform-native post. Stop announcing your newsletter — start atomizing it.

## Purpose

Your newsletter subscribers get the full edition. Your social audience gets the highlights — packaged as posts that stand on their own AND drive newsletter signups. This is how one piece of writing (the newsletter) feeds the entire social engine.

## When to Use

- Newsletter just went out to subscribers
- Back-catalog mining: repurpose old high-performing editions
- Content drought: need posts but no creative bandwidth for net-new ideas
- Newsletter has a section too valuable to keep email-only

## Inputs Required

- Full newsletter edition text
- Newsletter subscribe link
- Brand voice guide
- Which sections to extract (or let the agent identify them)

## Quick Reference

| Newsletter Section | Best Social Format | Platform |
|-------------------|-------------------|---------|
| Founder's note / personal essay | Story-driven post or short thread | X, LinkedIn |
| Framework / how-to | Thread or carousel | X, LinkedIn |
| Curated links / resources | Thread (one link + insight per tweet) | X |
| Data / metrics breakdown | Stat-led post or thread | X, LinkedIn |
| Reader question / AMA | Engagement post or poll | X, LinkedIn, IG |
| Behind the scenes | Photo + caption or video | IG, TikTok |

## Procedure

1. **Read the full newsletter.** Highlight every self-contained section that could work as an independent social post.

2. **For each section, assess:**
   - Can this stand alone without the reader needing newsletter context?
   - Is this section valuable enough on its own?
   - What's the best platform and format for this specific section?

3. **For each qualifying section, draft a platform-native post:**
   - New hook (don't reuse the newsletter subheading)
   - Adapted body (newsletter tone is slightly more formal than social)
   - Platform-appropriate CTA
   - Soft attribution: "From this week's newsletter" (not the hook, not the focus)

4. **Structure the CTAs:**
   - At least 1 post directly promotes newsletter signup
   - The rest soft-promote ("this was from the newsletter — link in bio to subscribe")

5. **Sequence posts across the week:**
   - Day 1-2: Best 2 posts (highest standalone value)
   - Day 3: Newsletter signup promo post
   - Day 4-5: Remaining posts
   - Don't cluster all newsletter content together

6. **Include "read the full edition" link** in bio or as reply, never in main post body (link penalty on X, constraints on IG/TikTok).

## Output Format

```markdown
# Posts from: [Newsletter Edition / Date]

## Source
[Newsletter link]

## Posts

### Post 1: [Topic]
**Platform:** [X / LinkedIn / IG / TikTok]
**Format:** [Short post / Thread / Carousel / Video]
**Source section:** [Which part of newsletter]
**Hook:** [Platform-formatted hook]
**Body:** [Full text]
**CTA:** [Text]
**Attribution:** "From [newsletter name] — link in bio"

### Post 2...
...

## Posting Sequence
- [Day/Time]: Post [N] on [Platform]
...

## Newsletter Signup Prompt
[Dedicated signup post with unique hook]
```

## Done Criteria

The skill is complete when:
1. At least 3 posts are extracted from the newsletter
2. Each post stands alone (no newsletter context needed)
3. Each post has a unique hook (not the newsletter subheading)
4. At least 1 post directly promotes newsletter signup
5. Posting sequence is specified across at least 3 days
6. Link placement follows platform rules

## Pitfalls

- Posting the newsletter as-is on social (nobody reads a 2,000-word LinkedIn post that was clearly an email)
- Every post saying "from my newsletter" without delivering standalone value
- Same CTA ("subscribe!") on every post — dilutes the ask
- Cannibalizing newsletter value: if social covers everything, why subscribe?

## Verification

For each post: would this make someone who's never heard of the newsletter want to subscribe? If a post is so complete that subscribing feels unnecessary, cut it back to a teaser.

## Example

*Input:* Newsletter edition "The State of B2B Cold Outreach — Q1 2026" (2,500 words). 5 sections: opening data essay, framework (3-part outreach sequence), tool recommendation, reader question, founder note.

*Output:*
- Post 1 (X, thread): "Cold outreach open rates dropped 22% in Q1. Here's what changed." — extracts the data essay.
- Post 2 (LinkedIn, post): "The 3-part outreach sequence that booked us 15 meetings" — extracts the framework.
- Post 3 (X, short post): "Tool we're loving this month: [name] — automated our follow-ups" — extracts tool recommendation.
- Post 4 (LinkedIn, post): "A reader asked me: 'how many follow-ups is too many?' Great question." — extracts reader Q&A.
- Post 5 (IG, story): "Behind the newsletter: how I wrote this week's edition" — extracts founder note as BTS.

Signup post: "Every week I share cold outreach data + frameworks in my newsletter. 2,500+ founders read it. Join them → link in bio."
