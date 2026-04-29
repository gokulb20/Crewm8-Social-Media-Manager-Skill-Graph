---
name: comment-reply
description: Draft replies to comments on the brand's own posts and value-add comments on other accounts' posts — non-promotional, brand-voice consistent, and engagement-driving.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, engagement, comments, replies, community, daily-routine]
related_skills: [brand-voice-system, mention-monitor, dm-respond, crisis-respond]
inputs_required: [new-comments-on-brand-posts, target-accounts-for-outbound-engagement]
deliverables: [reply-drafts-for-inbound-and-outbound-engagement]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]
---

# Comment Reply

Draft replies that make people feel heard on your own posts and make the brand visible in other people's feeds. The comment section is where community is built — one thoughtful reply is worth more than a generic "thanks!"

## Purpose

Commenting on other accounts is the highest-leverage growth tactic for small teams. It's free, it's visible, and it builds relationships. On your own posts, every reply is a signal to the algorithm that people are talking about your content.

## When to Use

- Daily engagement routine
- High-value accounts posted something worth engaging with
- Trending post in the space where brand comment adds visibility
- Founder building in public and peers are engaging
- Someone shared or reposted the brand's content

## Inputs Required

- Comments on brand's own posts (since last check)
- Target accounts for outbound engagement (10-15 per session)
- Brand voice guide
- Platform

## Quick Reference

| Reply Type | Goal | Tone | Max Length |
|-----------|------|------|-----------|
| Reply to own post comment | Acknowledge, add value, continue conversation | Warm, conversational | 1-3 sentences |
| Value-add on others' posts | Show expertise, be visible, be helpful | Insightful, non-promotional | 2-4 sentences |
| Thank-you for share/shoutout | Express genuine gratitude | Warm, specific | 1-2 sentences |
| Disagreement / debate | Disagree respectfully, add perspective | Professional, curious | 2-4 sentences |

## Procedure

### Part A: Replying to comments on brand posts

1. **Review all new comments.** Every 2-4 hours during active posting windows.

2. **Categorize:**
   - Positive/affirming: reply with warmth + follow-up thought
   - Question: answer directly and thoroughly
   - Disagreement: acknowledge their point, add perspective, no defensiveness
   - Spam/troll: do not engage (escalate to `crisis-respond`)
   - Low-effort ("nice! "great post"): short reply + question to extend conversation

3. **Draft replies:**
   - Acknowledge their specific point (not generic "thanks!")
   - Add a follow-up question, additional context, or validation
   - Match energy of their comment

### Part B: Engaging on other accounts' posts

4. **Identify 10-15 target accounts** for the session: high-value accounts in niche, other founders building in public, potential customers, trending posts.

5. **Draft value-add comments:**
   - NEVER promotional in someone else's replies
   - Add insight, ask a thoughtful question, share a relevant experience
   - Be specific: reference something they actually said
   - 2-4 sentences. Long enough to add value, short enough to be read.

6. **Quality check:**
   - Would this comment make someone curious about who wrote it?
   - Does it add to the conversation or just take up space?
   - If the brand had no product, would this still be a good comment?

## Output Format

```markdown
# Comment Replies: [Date]

## Replies on Brand Posts

### Post: [Title truncated]
**Commenter:** @handle
**Comment:** "[Their text]"
**Reply:** "[Drafted reply]"
**Type:** [Acknowledgment / Question answer / Debate]

---

## Comments on Other Accounts

### Account: @handle
**Their post:** [Topic]
**Our comment:** "[Drafted comment]"
**Strategy:** [Building authority / Engaging peer / Supporting community]

---

## Daily Summary
- Brand comments replied: [N]
- Other accounts engaged: [N] of [N] target
- Unreplied (flagged): [N]
```

## Done Criteria

The skill is complete when:
1. All new comments on brand posts have replies
2. 10-15 target accounts have been identified for engagement
3. Value-add comments are drafted (non-promotional)
4. No troll/spam comments have been engaged

## Pitfalls

- Generic replies: "Thanks!" "Great point!" — looks automated
- Self-promotional comments on other accounts (quickest way to get blocked)
- Arguing with trolls
- Over-commenting on one account (looks like a fan account)

## Verification

Read drafted replies. If you replaced the brand name with a random person, would these still be good comments? Comments should be valuable as COMMENTS, not as brand positioning.
