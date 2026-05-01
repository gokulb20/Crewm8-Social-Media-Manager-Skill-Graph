---
name: post-create
description: Write individual platform-native posts for X, LinkedIn, Instagram, and TikTok — with proper hooks, value-dense bodies, and CTAs optimized to each platform's format, audience, and algorithm.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, creation, posts, platform-native, writing, content]
related_skills: [hook-write, cta-craft, brand-voice-system, caption-draft, cross-post-adapt]
inputs_required: [topic-or-angle, brand-voice-guide, target-platform, desired-cta-type]
deliverables: [platform-formatted-post-text]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 2
required_tools: []
required_env_vars: []
---

# Post Create

Write a single platform-native post that earns attention, delivers value, and drives action. Each platform demands different structure, length, and energy. A post written for X does not belong on LinkedIn, and vice versa. This skill produces posts that feel native, not cross-posted.

## Purpose

The single biggest mistake brands make is writing one post and copying it to every platform. That doesn't save time — it wastes reach. This skill writes for the platform first, preserving the core message but expressing it in the format the audience expects to see there.

## When to Use

- Content calendar says "post needed for [platform]"
- Founder sends a half-formed idea
- Quick-win opportunity (trending topic, timely take)
- Reply to a competitor post that deserves a standalone response
- Filling a flex slot in the weekly calendar

## Inputs Required

- Topic or angle (from content calendar or founder input)
- Brand voice guide
- Target platform
- Any link, CTA, or hashtag requirements
- Optional: hook draft (can delegate to `hook-write`)

## Quick Reference

| Platform | Char Limit | Hook Style | Link Rules | Hashtag Rules | Best Format |
|----------|-----------|------------|------------|---------------|-------------|
| X | 280 (premium: 25K) | First 3 words are everything | Avoid in first tweet; use reply or final tweet | 0-1 per post | Short takes, hot takes, observations |
| LinkedIn | 3,000 (ideal: 900-1,200) | First 2 lines before "see more" | Anywhere, ideally after hook | 3-5 at end | Stories, lessons, frameworks |
| Instagram | 2,200 (ideal: 125-150) | Visual + first line of caption | Bio link only (no clickable links in caption) | 5-10 relevant + 2-3 branded | Visual-led, micro-blogging in captions |
| TikTok | 4,000 caption (video leads) | First 1.5s of video + text overlay | Bio link only | 3-5 trending | Video-first, captions secondary |

## Procedure

1. **Load inputs.** Topic, brand voice guide, platform rules, CTA requirements.

2. **Write the hook.** The hook is the single most important sentence. Delegate to `hook-write` for 5-10 variations, or write one directly:
   - X: First 3-5 words must stop the scroll. Lead with the strongest word.
   - LinkedIn: First line before "see more." Tease without clickbait.
   - IG: Visual does 70% of the hook work. Caption hook reinforces it.
   - TikTok: First 1.5 seconds of video + text overlay hook. Caption supports.

3. **Write the body:**
   - X: One clear idea. No fluff. Line breaks for visual whitespace.
   - LinkedIn: Story → lesson → applicability. Single-sentence paragraphs.
   - IG: Value-dense. First line delivers immediately.
   - TikTok: Video does the work. Caption adds context or CTA.

4. **Write the CTA.** Delegate to `cta-craft` if needed:
   - X: "Follow for more" or "Reply with your take" or link in reply
   - LinkedIn: "Agree? Disagree?" or "Save this" or link
   - IG: "Save," "Share to stories," "Comment your [X]"
   - TikTok: "Follow for part 2," "Link in bio"

5. **Apply platform formatting:**
   - X: No markdown. Line breaks only. 0-1 hashtag.
   - LinkedIn: No raw markdown. 3-5 hashtags at end.
   - IG: No clickable links. Hashtags in first comment or end.
   - TikTok: Caption short. 3-5 trending hashtags.

6. **Run brand voice check.** Does the post sound like the brand or like a generic AI output? Would the founder actually say this?

## Output Format

```markdown
## Post: [Platform]

[Full post text, formatted exactly as it should appear on the platform]

---
**Platform:** [X / LinkedIn / IG / TikTok]
**Pillar:** [Education / POV / Proof / BTS / CTA]
**Hook type:** [Question / Contrarian / Statistic / Story / Observation]
**CTA:** [Follow / Reply / Save / Link / DM / Share]
**Best posting time:** [Day + time window]
**Visual suggestion:** [Image/video idea if applicable]
**Voice check:** [Passes brand voice? Y/N + brief note]
```

## Done Criteria

The skill is complete when:
1. Post text is formatted exactly as it should appear on the target platform
2. Character count is within platform limits
3. Hook earns its place (it's specific, not generic)
4. CTA is matched to post goal and value delivered
5. Brand voice check passes (the founder would say this)

## Pitfalls

- Writing one post and copying it to other platforms with minor tweaks
- Overwriting: 280 characters is a constraint, not a suggestion
- Underwriting: LinkedIn posts under 200 characters feel like tweets
- Hashtag vomit on Instagram (30 hashtags looks desperate)
- Forgetting that TikTok is video-first — no caption can save a bad video

## Verification

Read the post out loud. Does it sound human? Count filler words ("really," "very," "actually," "just") — remove them. Check character count against platform limits. Does the hook make you want to read the next line?

## Example

*Input:* Topic: "Most cold outreach fails because it's not personal enough." Platform: X. Goal: engagement + new followers.

*Output:*
```
cold outreach isn't dead.

it's just lazy.

"hey saw you're a founder, check out my tool" = deleted in 0.5s

here's what actually works from 10,000+ cold emails analyzed:

1/ personalize the FIRST sentence
not the last one. first.

if you open with a template line, they never read past it.
start with something only THEY would say.

2/ lead with VALUE, not your product
"i can help you grow" = spam
"your pricing page has a pricing error that costs you 15%" = meeting booked

3/ make the ask TINY
not "hop on a call"
"reply with your top metric — i'll tell you if we can improve it"

follow for more cold outreach frameworks. next post goes deep on subject lines.
```

Platform: X | Pillar: Education | Hook type: Contrarian | CTA: Follow
