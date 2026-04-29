---
name: cta-craft
description: Select and write the optimal call-to-action for any social post — follow, reply, DM, save, share, link, or signup — matched to platform, content type, content value, and audience psychology.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, creation, cta, conversion, writing, persuasion]
related_skills: [post-create, thread-create, caption-draft, ab-test-analyze, hook-write]
inputs_required: [post-goal, content-value-level, target-platform, desired-action-type]
deliverables: [cta-text-with-placement-and-rationale]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---

# CTA Craft

Choose and write the right call-to-action for every post. A great post with a weak CTA leaves value on the table. A strong CTA on the wrong content type feels desperate. This skill matches the ask to the context.

## Purpose

Most brands either never ask for anything (and wonder why nobody acts) or ask for too much too early (and lose trust). This skill calibrates the CTA intensity to the value delivered — so every post has a proportionate ask.

## When to Use

- Finishing any post, thread, or caption
- Testing whether a different CTA would improve conversion
- Content calendar planning (each slot needs a CTA intent)
- Founder says "we're getting engagement but no conversions"

## Inputs Required

- Post goal (engagement, growth, list-building, product conversion)
- Content value delivered (high/medium/low — based on what the post teaches/reveals)
- Target platform
- Any link or offer to include

## Quick Reference

| CTA Type | What It Asks For | When to Use | Best Platforms |
|----------|-----------------|-------------|---------------|
| Follow | "Follow @handle for more on [topic]" | End of educational threads, high-value posts | X, TikTok |
| Reply | "What's your experience? Reply below" | Contrarian/opinion posts, questions | X, LinkedIn |
| Save | "Save this for your next [context]" | Frameworks, checklists, reference posts | IG, LinkedIn |
| Share | "Share with a founder who needs this" | High-value evergreen content | LinkedIn, IG |
| DM | "DM me [word] and I'll send [resource]" | Lead gen, list building | X, IG |
| Link | "Link in bio" or "Link in next tweet" | Product, newsletter, website | All (platform rules vary) |
| Signup | "Join [N] founders getting this weekly" | Newsletter growth, waitlist | LinkedIn, X |
| Poll | "Which do you prefer: A or B?" | Engagement boost, audience research | X, LinkedIn, IG Stories |

## Procedure

1. **Determine the post's primary goal.**
   - Brand building / authority (no hard ask needed)
   - Engagement boost (reply, poll, share)
   - List growth (signup, DM, link)
   - Product conversion (link, demo)
   - Community growth (follow)

2. **Match CTA intensity to content value:**
   - High-value (framework, detailed case study, exclusive data): can ask for save + follow + share
   - Medium-value (solid take, good observation): ask for reply or follow
   - Low-value (quick thought, retweet, link drop): no ask or minimum ask
   - Rule: the more value delivered, the bigger the ask can be

3. **Write the CTA in platform-native format:**
   - X: 1 line, short. "Follow for more." "Reply with your take." No link in first post.
   - LinkedIn: 1-2 lines. "Agree? Disagree? Let me know below." "Save this for later."
   - IG: 1 line. "Save for later." "Share to your story." "Comment '[X]' below."
   - TikTok: Spoken + text overlay. "Follow for part 2." "Link in bio."

4. **Choose CTA placement:**
   - End of post: standard, expected
   - Mid-post: interrupt pattern, works when insight is strong enough
   - No CTA: let content stand alone. Valid 1-2x per week.

5. **Define CTA rotation:**
   - Rotate through reply / save / DM / follow / none throughout the week
   - Hard CTA (signup/link) maximum 1-2x per week

## Output Format

```markdown
# CTA: [Post/Thread Title]

## Post Goal
[Brand building / Engagement / List growth / Product conversion]

## Content Value Delivered
[High / Medium / Low]

## Recommended CTA
[Type + full text, formatted for platform]

## Why This CTA
[Matches post goal + proportionate to value]

## Alternate CTA (A/B Test)
[Different CTA type + full text]

## Placement
[End of post / Mid-post / No CTA]

## Link (if applicable)
[URL + where it should live per platform rules]
```

## Done Criteria

The skill is complete when:
1. A CTA is selected and matched to the post's goal and value level
2. The CTA is formatted for the target platform
3. CTA placement is specified
4. An alternate CTA is provided for A/B testing (if applicable)
5. The CTA does not over-ask relative to value delivered

## Pitfalls

- Asking for a signup on a post that gave zero value
- Same CTA every single post (pattern blindness)
- Two CTAs in one post (splits attention, reduces action)
- No CTA ever (you're building a brand, not a museum)
- CTA that contradicts the post tone (serious post + "lol DM me" = jarring)

## Verification

Read the post without the CTA. Does it feel complete? Read it with the CTA. Does the ask feel proportionate? If the post is 2/10 value, the CTA should be a 2/10 ask.

## Example

*Input:* Post goal = newsletter growth. Content = "The 3 email subject lines that got us a 45% open rate" (high value, specific data). Platform = X.

*Output:*
- CTA Type: Signup
- Text: "Want the full breakdown? I share frameworks like this in my weekly newsletter. Link in the reply below."
- Placement: End of thread
- Alternate: "Follow for more email marketing breakdowns. Newsletter every Sunday — link in bio."
- Why: The post delivered high specific value, so asking for a newsletter signup is proportionate. The link goes in the reply (not the main tweet) to avoid reach penalty.
