---
name: brand-voice-system
description: Extract brand voice from existing content, create a comprehensive do/don't guide, and maintain tone rules to detect voice drift over time.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Strategy, Brand-Voice, Tone, Consistency]
    related_skills: [positioning-statement, content-pillars]
---

# Brand Voice System

Extract, codify, and maintain the brand's unique voice across all social content. This skill defines how the brand sounds so every post, reply, and DM feels like it came from the same person.

## When to Use

- Onboarding a new client or brand
- Founder feedback indicates "this doesn't sound like us"
- Voice drift is detected across platforms or over time
- Quarterly voice audit and refresh
- After a major rebrand or pivot

## Quick Reference

| Component | What It Covers |
|-----------|---------------|
| Voice traits | 3-5 adjectives that describe the brand (e.g., "warm, direct, playful, zero-BS") |
| Do guide | Specific language patterns, sentence structures, and words to use |
| Don't guide | Banned phrases, corporate jargon, cliches, competitor phrases |
| Platform variations | How the voice flexes between X (punchier), LinkedIn (more polished), IG (more visual-led), TikTok (more casual/trend-aware) |
| Swear/edge policy | What level of edginess is allowed, if any |

## Procedure

1. Gather source material: last 3 months of social posts, blog posts, newsletters, podcast transcripts, founder interviews, customer support tone.

2. Read everything and highlight patterns. Look for:
   - Sentence length (short and punchy? long and thoughtful?)
   - Vocabulary range (technical? accessible? industry jargon?)
   - Punctuation habits (em dashes? ellipses? all lowercase?)
   - Humor style (dry? absurd? self-deprecating? none?)
   - Emotional register (excited? calm? urgent? reassuring?)

3. Distill into 3-5 voice traits. Each trait gets:
   - A one-word label
   - A one-sentence definition
   - A real example from the source material

4. Build the Do guide:
   - Sentence structure rules (e.g., "lead with the strongest word, max 18 words per sentence on X")
   - Preferred words and phrases (the brand's "signature vocabulary")
   - Transition patterns ("But here's the thing:", "The part nobody talks about:")

5. Build the Don't guide:
   - Banned words (corporate cliches, buzzwords, competitor-specific language)
   - Banned formats ("10 ways to...", "Unlock your potential", "In today's fast-paced world")
   - Tone violations ("Too salesy", "Too vague", "Too formal for this platform")

6. Define platform-specific voice flex:
   - X: Shortest sentences, highest energy, most conversational
   - LinkedIn: Slightly more structured, still human, less emoji
   - IG: Voice works with visuals, captions can breathe more
   - TikTok: Most casual, trend-aware, hook in first 1.5 seconds

7. Write a "voice test" — 5 sentences that the agent can use to check if new content matches voice before publishing.

## Output Format

```markdown
# [Brand Name] Voice Guide

## Voice Traits
1. [Trait] — [definition + example]
2. [Trait] — [definition + example]
3. [Trait] — [definition + example]

## Do This
- [specific language pattern]
- [preferred phrase / construction]

## Don't Do This
- [banned phrase or pattern]
- [tone violation]

## Platform Voice Flex
- X: [how it differs]
- LinkedIn: [how it differs]
- IG: [how it differs]
- TikTok: [how it differs]

## Voice Test
1. [Sentence that passes]
2. [Sentence that would fail + why]
```

## Pitfalls

- Over-codifying voice so it sounds robotic — leave room for spontaneity
- Confusing the founder's speaking voice with a social-media-optimized version of it
- Making rules too generic ("be authentic" — that's not a rule, that's a prayer)
- Forgetting to update after 6 months — voice evolves as the brand grows

## Verification

Run 3 recent high-performing posts through the voice guide. They should match. Run 1 post that felt "off" through the guide — it should flag specific violations. Share the guide with the founder and ask: "Does this sound like you?"
