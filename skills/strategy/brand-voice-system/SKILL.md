---
name: brand-voice-system
description: Extract a brand's unique voice from existing content, build a do/don't guide with specific language rules, and maintain tone standards to detect drift over time. Works with X, LinkedIn, Instagram, and TikTok.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, strategy, brand-voice, tone, consistency, identity]
related_skills: [positioning-statement, content-pillars]
inputs_required: [social-post-samples, founder-interviews-or-voice-references, existing-brand-guidelines-if-any]
deliverables: [brand-voice-guide-document]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Brand Voice System

Extract, codify, and maintain the brand's unique voice across all social content. This skill defines how the brand sounds so every post, reply, and DM feels like the same person wrote it — no ghostwriting whiplash, no platform dissonance.

## Purpose

A brand without a documented voice sounds like four different people on four different platforms. This skill gives you a single source of truth for tone, vocabulary, and platform-specific flex — so every piece of content reinforces the same identity.

## When to Use

- Onboarding a new brand or client
- Founder says "this doesn't sound like us"
- Voice drift detected across platforms or over time
- Quarterly voice audit and refresh
- After a rebrand, pivot, or leadership change
- Prepping for a multi-platform launch (voice needs to flex predictably)

## Inputs Required

- **Social post samples:** 15-20 recent posts from each active platform (mix of high and low performers)
- **Founder voice references:** interviews, customer support replies, email drafts, podcast clips, loom videos, or any raw founder communication
- **Brand guidelines (if any):** existing style guide, mission statement, taglines, values
- **Competitor voice samples (optional):** how 2-3 key competitors sound

## Quick Reference

| Component | What It Covers |
|-----------|---------------|
| Voice traits | 3-5 adjectives describing the brand (e.g., "warm, direct, playful, zero-BS") |
| Do guide | Specific language patterns, sentence structures, preferred words |
| Don't guide | Banned phrases, corporate jargon, cliches, competitor vocabulary |
| Platform flex | How the voice adapts per platform |
| Edge policy | Swearing, controversy, humor boundaries |
| Voice tests | 5 sample sentences to check new content against before publishing |

## Procedure

1. **Gather source material.** Collect the last 3 months of social posts, blog content, newsletters, podcast transcripts, founder interviews, and customer support replies. The more source material, the more accurate the voice extraction.

2. **Analyze for patterns.** Read everything and note:
   - Sentence length: short and punchy? Long and thoughtful? A mix?
   - Vocabulary: technical or accessible? Jargon-heavy or plain English?
   - Punctuation habits: em dashes? ellipses? all lowercase? exclamation overload?
   - Humor style: dry? absurd? self-deprecating? inside-jokey? None?
   - Emotional register: excited? calm? urgent? reassuring? confrontational?
   - Rhythm: do they lead with questions, stories, stats, or declarations?

3. **Distill into 3-5 voice traits.** Each trait gets:
   - A one-word label
   - A one-sentence definition
   - A real example from source material
   - A counterexample of what it ISN'T

4. **Build the Do guide:**
   - Sentence structure rules: "Lead with the strongest word. Max 18 words per sentence on X."
   - Signature vocabulary: words and phrases the brand owns
   - Transition patterns: "But here's the thing:", "The part nobody talks about:"
   - Opening patterns: how 80% of posts should start

5. **Build the Don't guide:**
   - Banned words: corporate cliches, buzzwords, competitor-specific language
   - Banned formats: "10 ways to...", "Unlock your potential", "In today's fast-paced world"
   - Tone violations: "too salesy", "too vague", "too formal for this platform"
   - Topic restrictions: what the brand does NOT talk about

6. **Define platform voice flex:**
   - X: shortest sentences, highest energy, most conversational
   - LinkedIn: slightly more structured, human not corporate, less emoji
   - IG: voice works with visuals, captions can breathe, 1-3 emoji max
   - TikTok: most casual, trend-aware, hook in first 1.5 seconds, voice in the captions AND the video script

7. **Write the voice test.** 5 pre-written sentences that the agent can test any new content against before publishing. Each sentence tests a different voice dimension (tone, vocabulary, structure, energy, platform-fit).

8. **Document edge policy explicitly:**
   - Swearing: allowed? Light swears only? Never?
   - Controversy: how spicy can takes get before founder approval is needed?
   - Self-deprecation: encouraged? allowed? never?

## Output Format

```markdown
# [Brand Name] Voice Guide v[date]

## Voice Traits
1. **[Trait]** — [Definition]. Example: "[real quote]" (not: "[counterexample]")
2. ...

## Do This
- [specific language pattern]
- [preferred phrase or construction]
- [opening pattern that works]

## Don't Do This
- [banned phrase or pattern]
- [banned format or word]
- [tone violation to catch]

## Platform Voice Flex
- **X:** [how the voice changes]
- **LinkedIn:** [how the voice changes]
- **IG:** [how the voice changes]
- **TikTok:** [how the voice changes]

## Edge Policy
- Swearing: [Yes / Light / No]
- Controversy threshold: [Describe — what requires founder approval?]
- Humor boundary: [Self-deprecating / Absurdist / None / Depends on topic]

## Voice Test
1. [Passing sentence] → [Why it passes]
2. [Failing sentence] → [Which voice dimension it violates]
3-5. ...
```

## Platform Notes

| Platform | Voice Characteristic |
|----------|---------------------|
| X | Fastest pace. Shortest sentences. Most direct. First 3 words carry the hook. |
| LinkedIn | Slightly longer sentences. More structure. Still human — "corporate you" is banned. |
| Instagram | Visual-first; voice supports the image. Captions are warmer, more personal, emoji-tolerant. |
| TikTok | Most casual. Caption is secondary to video script. Voice must feel like a friend talking. |

## Done Criteria

The skill is complete when:
1. The voice guide document exists with all sections filled in, not placeholder text
2. At least 3 real examples exist per voice trait
3. At least 5 items exist in the Do guide and 5 in the Don't guide
4. Platform flex is documented for all 4 platforms
5. The edge/swear policy is explicitly stated (even if the answer is "no edge at all")
6. 3 high-performing existing posts pass the voice test, and 1 post that felt "off" fails specific rules

## Pitfalls

- Over-codifying: if the guide is 50 pages, nobody (and no agent) will use it. Keep it to 1-2 pages.
- Founder-voice-only: the founder's speaking voice isn't the same as a social-media-optimized brand voice. Optimize without losing their essence.
- Generic rules: "be authentic" is not a rule. Be specific: "use contractions, avoid passive voice, open with data not questions."
- Stale guide: voice evolves. Set a quarterly review reminder.

## Verification

Run 3 high-performing posts through the guide. They should match every rule. Run 1 post that felt wrong — it should flag specific violations. Show the guide to someone who knows the brand but didn't write the guide. Ask: "Does this sound like them?" If they hesitate, the extraction missed something.

## Example

*Input:* 12 recent X posts, 5 founder podcast transcripts, and a "voice is feeling off" complaint from a team member.

*Process:* The agent reads all source material, identifies that the founder writes long, thoughtful sentences on X that get truncated and lose momentum. The guide captures: "X voice = 1 thought, 1-2 sentences max. Save the nuance for LinkedIn." It also catches that the brand uses "honestly" as a crutch word (3+ times per post) — banned.

*Output:* A voice guide with 4 traits (Direct, Warm, Unpolished, Opinionated), a Do guide with 7 rules, a Don't guide with 7 entries, platform flex for all 4 platforms, and a voice test with 5 sample checks.
