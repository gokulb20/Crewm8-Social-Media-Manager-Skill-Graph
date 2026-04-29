---
name: positioning-statement
description: Craft an elevator pitch, niche positioning, and contrarian take that every social post ladders up to — ensuring all content reinforces a single clear message about who the brand serves and why it matters.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, strategy, positioning, messaging, brand-foundation]
related_skills: [brand-voice-system, content-pillars, hook-write]
inputs_required: [existing-brand-materials, customer-interviews-or-testimonials, competitor-landscape]
deliverables: [positioning-statement-document]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Positioning Statement

Define the core positioning that every piece of content ladders up to. This is the answer to "what do you do?" that lives in the background of every post, thread, reply, and caption. Content without positioning is noise.

## Purpose

A brand that tries to talk to everyone ends up interesting to nobody. This skill distills the brand's audience, problem, solution, and differentiator into a single positioning that makes content decisions obvious: "Does this post reinforce our positioning?" If no, don't post it.

## When to Use

- Before building any content calendar
- Founder's messaging is scattered across platforms
- After a pivot, rebrand, or new product launch
- Quarterly positioning refresh
- New team member needs the one-sentence north star
- Content feels "correct" but boring (positioning is too safe)

## Inputs Required

- Website, pitch deck, investor updates
- Customer testimonials, support tickets, sales call transcripts
- Founder's personal bio and speaking materials
- Top 3 competitor positioning for comparison
- Any previous positioning docs (to identify what changed)

## Quick Reference

| Element | Purpose | Example |
|---------|---------|---------|
| Target audience | Who exactly (not "everyone") | "Seed-stage SaaS founders who are technical but hate marketing" |
| Problem | Specific pain in their words | "You can build the product but nobody signs up" |
| Solution | One plain sentence, no jargon | "We handle your entire GTM so you can focus on shipping" |
| Differentiator | Sharpest edge vs alternatives | "Outcome-based pricing — we only win when you grow" |
| Proof | Evidence it works | "150+ customers, average 3x pipeline in 90 days" |

## Procedure

1. **Review existing materials.** Read website, pitch decks, investor updates, customer testimonials. Note which messages get the strongest reactions.

2. **Define the target audience with precision:**
   - Role, company stage, specific pain, aspiration
   - Not "startup founders" — "pre-seed B2B SaaS founders raising their first round"
   - Use language customers actually use (verbatim quotes from support tickets, sales calls, reviews)

3. **Articulate the problem in their words:**
   - No marketing speak. Use their vocabulary.
   - Find the specific frustration that keeps them up at night — not the category problem, the personal one.

4. **Write the solution in one plain sentence:**
   - If your mom wouldn't understand it, rewrite it.
   - No jargon, no weasel words ("leverage," "synergize," "next-gen").

5. **Identify the sharpest differentiator:**
   - Speed? Price? Approach? Specific use case? Philosophy?
   - "We're the X for Y" is valid IF it's accurate.
   - Run the test: "If a competitor copied our entire product tomorrow, what would still make us different?"

6. **Write 3 positioning statement variants:**
   - **Elevator pitch:** 1 sentence, works in any context
   - **Social bio version:** 150 characters, platform-ready (X bio, IG bio, LinkedIn headline)
   - **Contrarian take:** What belief does the brand hold that competitors don't? (This is often your highest-engaging content on X.)

7. **Stress-test:** Can every piece of planned content for the next month ladder up to this positioning? If any post feels disconnected, the positioning is either wrong or too narrow.

## Output Format

```markdown
# [Brand] Positioning — [Date]

## Elevator Pitch
[One sentence: who you help, what you do, why it matters]

## Social Bio Version
[150 characters max — ready for X/LinkedIn/IG bio fields]

## Contrarian Take
[The belief that sets you apart — e.g., "Most B2B pricing is wrong. Here's what actually works."]

## Target Audience
- Primary: [specific persona with role, stage, pain, aspiration]
- Secondary: [adjacent persona, if any]

## Problem They Feel
[In their words — include a verbatim quote if possible]

## How We Solve It
[One plain sentence]

## Why Us
[Sharpest differentiator — the thing competitors can't easily copy]

## Proof Points
- [Metric or logo or testimonial — 3-5 items]

## Content Litmus Test
Can every post this month trace back to this positioning?
```

## Done Criteria

The skill is complete when:
1. The elevator pitch passes the "mom test" (anyone can understand it)
2. The social bio version fits within 150 characters
3. A contrarian take exists that's specific enough to generate engagement
4. The positioning is narrow enough that it explicitly excludes someone
5. Every content pillar planned for the next month can trace back to this positioning

## Pitfalls

- Positioning that's true but boring ("we help businesses grow" — everyone says this)
- Positioning that's so narrow nobody cares (too niche is fixable; too generic is fatal)
- Copying a competitor's positioning because it sounds good on their website
- Positioning that shifts every month (your content needs a consistent anchor)
- Forgetting the "why" — people don't buy what you do, they buy why you do it

## Verification

Show the 3 variants to 5 people who fit the target audience. Ask: "What do you think this company does?" If 3+ people can't explain it back in their own words, the positioning isn't clear enough. Post the contrarian take on X as a standalone statement — if it gets 0 engagement, the positioning doesn't resonate.

## Example

*Input:* Website says "AI-powered growth platform for startups." Customer call transcript says "We were spending $5K/month on ads getting zero pipeline. Crewm8 automated our outreach and we closed 3 deals in week one."

*Process:* The agent identifies the real problem isn't "growth" — it's "wasted spend with no pipeline." The positioning shifts from features (AI-powered) to outcome (pipeline without the burn).

*Output:*
- Elevator pitch: "We automate B2B outreach so early-stage founders can build pipeline without a sales team."
- Bio version: "B2B outreach automation for seed-stage founders. Pipeline without the burn."
- Contrarian take: "Most 'growth' advice is written by people selling growth advice. Real pipeline comes from consistent, personal outreach — and we automated that."
