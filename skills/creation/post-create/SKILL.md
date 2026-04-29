---
name: post-create
description: Write indivual platform-native posts for X, LinkedIn, Instagram, and TikTok with proper hooks, body, and CTAs optimized to each platform's format and audience expectations.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Creation, Posts, Platform-Native, Writing]
    related_skills: [hook-write, cta-craft, brand-voice-system, caption-draft, thread-create]
---

# Post Create

Write a single platform-native post that earns attention, delivers value, and drives action. Each platform demands different structure, length, and energy. This skill produces posts that feel native, not cross-posted.

## When to Use

- Content calendar says "post needed for [platform]"
- Founder sends a half-formed idea: "Can you turn this into a post?"
- Quick-win opportunity (trending topic, timely take)
- Reply to a competitor post that deserves a standalone response
- Filling a flex slot in the weekly calendar

## Quick Reference

| Platform | Character/Time Limit | Hook Style | Link Rules | Hash Tag Rules | Best Formats |
|----------|---------------------|------------|------------|---------------|--------------|
| X | 280 chars (premium: 25K) | First 3 words are everything | Avoid in first tweet | 0-1 per post | Short takes, hot takes, observations |
| LinkedIn | 3,000 chars (ideal: 900-1,200) | First 2 lines before "see more" | Anywhere, ideally after hook | 3-5 relevant | Stories, lessons, frameworks |
| Instagram | 2,200 chars (ideal: 125-150) | Visual + first line of caption | Bio link only (no clickable links in caption) | 5-10 relevant + 2-3 branded | Visual-led, micro-blogging in captions |
| TikTok | 4,000 chars caption (but text overlay on video matters more) | First 1.5 seconds of video + text overlay | Bio link only | 3-5 trending | Video-first, captions are secondary |

## Procedure

1. Load inputs:
   - The topic/angle from the content calendar (or the raw idea from the founder)
   - Brand voice guide
   - Platform-specific format rules (from Quick Reference above)
   - Any required CTA (signup link, "reply with your take", "save for later")

2. Write the hook (delegate to `hook-write` skill if needed):
   - X: First 3-5 words must stop the scroll. Lead with the strongest word.
   - LinkedIn: First line before the "see more" cut. Tease without clickbait.
   - IG: Visual does 70% of the hook work. Caption hook reinforces it.
   - TikTok: First 1.5 seconds of video + text overlay hook.

3. Write the body:
   - X: One clear idea. No fluff. Use line breaks for visual whitespace.
   - LinkedIn: Story → lesson → applicability. Use single-sentence paragraphs.
   - IG: Value-dense caption. People scroll past if the first line doesn't deliver.
   - TikTok: Video does the work. Caption adds context or CTA.

4. Write the CTA (delegate to `cta-craft` skill if needed):
   - X: "Follow for more on [topic]" or "Reply with your take" or link in reply
   - LinkedIn: "Agree? Disagree?" or "Save this for later" or link
   - IG: "Save," "Share to stories," "Comment your [X],"
   - TikTok: "Follow for part 2," "Link in bio"

5. Apply platform formatting:
   - X: No markdown. Line breaks only. 0-1 hashtag. No link in first post.
   - LinkedIn: No markdown, but bold/italic via LinkedIn formatting. 3-5 hashtags at end.
   - IG: No clickable links in caption. Hashtags in first comment or end of caption.
   - TikTok: Caption short. 3-5 trending hashtags. No links except bio.

6. Run through brand voice check:
   - Does it match the do/don't guide?
   - Does it sound like the brand or like ChatGPT?
   - Would the founder actually say this?

7. Add visual/format notes if applicable:
   - What image/video would amplify this post?
   - What's the alt-text for accessibility?

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
**Voice check:** [Does it match brand voice guide? Y/N + brief note]
```

## Platform Notes

- X: Brevity rules. If a sentence doesn't earn its place, cut it. Line breaks are free — use them.
- LinkedIn: "Agree?" comments boost reach. Structure: hook → context → insight → CTA → hashtags.
- IG: The visual sells the stop. The caption sells the save/share. Always design them together.
- TikTok: Hook in first 1.5s. Pattern interrupt every 3-5 seconds. Caption supports, doesn't lead.

## Pitfalls

- Writing one post and copying it to other platforms with minor tweaks (audiences can tell)
- Overwriting: 280 characters is a constraint, not a suggestion
- Underwriting: LinkedIn posts under 200 characters feel like tweets, not thoughtful content
- Hashtag vomit on Instagram (30 hashtags looks desperate)
- Forgetting that TikTok is video-first — a great caption can't save a bad video

## Verification

Read the post out loud. Does it sound like a human? Count filler words ("really," "very," "actually," "just"). Remove them. Check character count against platform limits. Does the hook make you want to read the next line?
