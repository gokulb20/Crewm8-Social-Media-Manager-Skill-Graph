---
name: caption-draft
description: Write Instagram and LinkedIn captions with scroll-stopping hooks, value-dense bodies, platform-appropriate CTAs, and strategic hashtag sets — optimized for each platform's reading behavior and visual context.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, captions, instagram, linkedin, writing, hashtags]
related_skills: [hook-write, cta-craft, post-create, visual-plan]
inputs_required: [visual-asset-description, core-message, target-platform, cta-requirement]
deliverables: [platform-formatted-caption-with-hashtags]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Caption Draft

Write captions for Instagram and LinkedIn that make people stop scrolling, read, and act. Captions are not descriptions of the visual — they're standalone content that works WITH the visual but delivers value on its own.

## Purpose

On Instagram, the visual stops the scroll; the caption earns the save and share. On LinkedIn, the text is the content. This skill writes captions that serve the visual without describing it, and adds value the visual alone couldn't deliver.

## When to Use

- Visual asset (carousel, image, video) is ready and needs a caption
- Instagram feed post, Reel, or Story needs text
- LinkedIn post with an image or carousel needs a supporting caption
- Repurposing a blog post or thread into a caption

## Inputs Required

- Visual asset description (what it shows, what emotion it conveys)
- Core message (one sentence)
- Target platform (IG or LinkedIn)
- Any link or tag requirements
- Hashtag direction (branded tags, campaign tags, audience tags)

## Quick Reference

| Platform | Ideal Length | Structure | Hashtag Strategy |
|----------|-------------|-----------|-----------------|
| IG Feed | 125-150 words (first 2 lines critical) | Hook → Value → CTA → Hashtags | 5-10 relevant + 2-3 branded, in caption or first comment |
| IG Reels | 50-75 words (video does the work) | Hook → Context → CTA | 3-5 |
| IG Stories | 1-2 lines + sticker/poll | Quick hit + interactive element | 1-2 |
| LinkedIn | 900-1,200 chars (300-600 words) | Hook → Story/Insight → Lesson → CTA → Hashtags | 3-5 relevant |

## Procedure

1. **Study the visual.** What emotion or idea does it communicate on its own? The caption should ADD something, not describe what's already visible.

2. **Write the hook (first 2 lines):**
   - IG: First 2 lines before "more" expand. Lead with a question, bold claim, or story opener.
   - LinkedIn: First ~210 characters before "see more" cut. Must hook immediately.
   - Do NOT describe the visual ("Swipe through to see...") — that's filler.

3. **Write the body:**
   - IG: Value-first. Front-load the insight. Line breaks for rhythm. Write like you talk.
   - LinkedIn: Story structure (setup → conflict → resolution → lesson → applicability).
   - Single-sentence paragraphs. Walls of text get scrolled past.

4. **Write the CTA:**
   - IG: "Save this," "Share with someone who needs this," "Comment '[X]' below," "Link in bio"
   - LinkedIn: "Agree? Disagree?" "Save for later," "Repost if this resonated"
   - Match CTA intensity to content value (see `cta-craft`)

5. **Build the hashtag set:**
   - IG: 5-10 relevant + 2-3 branded. Mix of sizes (1-2 large, 3-5 medium, 3-5 niche).
   - LinkedIn: 3-5 hashtags at end. All relevant, no fluff.
   - Place: end of caption (both platforms) or first comment (IG only).

6. **Do the "would I read this" test.** If you saw this in your feed, would you expand it? Does the first like make you want to read more?

## Output Format

```markdown
# Caption: [Post Title]

## Platform: [Instagram / LinkedIn]

[Full caption text, formatted exactly as it should appear — including line breaks, emoji placement, and hashtags]

---
**Hook style:** [Question / Story / Bold claim / Observation / Statistic]
**Body structure:** [Story-led / Framework / List / Single insight]
**CTA:** [Type + text]
**Hashtags:** [Number + examples]
**Character count:** [N]
```

## Done Criteria

The skill is complete when:
1. First 2 lines form a complete hook that makes you want to read more
2. Caption adds value beyond what the visual communicates
3. CTA is matched to content value and platform norms
4. Hashtag count and density match platform conventions
5. Character count is within platform limits

## Pitfalls

- Captions that describe what the visual already shows (redundant)
- Leading with "Link in bio" — wastes the most valuable real estate
- Instagram captions under 50 characters (looks lazy)
- LinkedIn captions that read like tweets (too short, no depth)
- Hashtag stuffing on LinkedIn (more than 5 looks desperate)
- Forgetting that the Instagram first line is the ONLY thing people see before tapping "more"

## Verification

Preview on mobile. Do the first 2 lines make you tap "more"? Read it out loud — does it sound human? Would the founder feel good about this? Does the caption add something the visual doesn't?

## Example

*Input:* IG carousel about "5 signs your pricing is wrong." Visual shows a 5-slide carousel with the signs. Goal = saves + shares.

*Output:*
```
your pricing is probably wrong. here's how to tell.

slide 2 is the one that hurts most. (it's the one we were guilty of too.)

if any of these 5 feel familiar, it's time to audit your prices:

→ your churn is under 60% but above 30% (you're in no-man's land)
→ your best customers took >3 months to convert (price was a barrier)
→ you've never raised prices (inflation exists, your pricing should too)
→ your competitors don't know your pricing (you're hiding, not strategic)
→ your sales team discounts more than 20% of deals (your list price is wrong)

which one hits closest? drop the number in the comments.

#saaspricing #founder #startupadvice #pricingstrategy #b2bsaas
```

Hook: Bold claim ("your pricing is probably wrong") | Body: List + personal note | CTA: "drop the number in the comments"
