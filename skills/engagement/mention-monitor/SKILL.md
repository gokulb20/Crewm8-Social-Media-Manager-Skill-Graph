---
name: mention-monitor
description: Monitor brand mentions across all platforms, reply within 2-4 hours, categorize by sentiment and priority, and log unanswered mentions for follow-up.
version: 2.0.0
author: Crewm8
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, engagement, mentions, monitoring, brand-awareness, sentiment]
related_skills: [comment-reply, dm-respond, crisis-respond, performance-report]
inputs_required: [brand-handles-and-keywords-to-monitor, platform-access-per-platform]
deliverables: [mention-report-with-reply-status-and-sentiment]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: ["X_API_KEY"]
required_env_vars: ["X_API_KEY"]
---

# Mention Monitor

Track every time the brand is mentioned across platforms and ensure nothing goes unanswered. A thanked mention builds community. An ignored mention signals the brand doesn't care.

## Purpose

Brand mentions are free attention. Ignoring them is leaving social capital on the table. This skill ensures every mention is seen, categorized, and responded to within the appropriate timeframe.

## When to Use

- Daily monitoring routine
- After a high-performing post goes out (mention volume spikes)
- Post-launch or campaign period
- Weekly mention audit

## Inputs Required

- Brand handle(s) and keywords to monitor
- Access to each platform's notification/mention feed
- Response time targets

## Quick Reference

| Mention Type | Priority | Response Time | Action |
|-------------|---------|--------------|--------|
| Direct tag/shoutout | High | Within 2 hours | Thank + add value |
| Question about product | Critical | Within 1 hour | Answer directly |
| Complaint / negative | Critical | Within 1 hour | Acknowledge, route if needed |
| Share / repost | Medium | Within 4 hours | Thank individually |
| Casual reference (untagged) | Low | Within 24 hours | Engage if natural |
| Competitor comparison | Medium | Within 4 hours | Monitor; engage only if factual correction needed |

## Procedure

1. **Set up mention detection:**
   - X: @handle tags + brand name keyword searches
   - LinkedIn: @company mentions + post tags
   - Instagram: @handle tags in captions, comments, stories
   - TikTok: @handle tags + brand name in video text/captions

2. **Daily sweep** (morning + afternoon):
   - Check all direct @mentions
   - Search for untagged brand name references
   - Check quote tweets
   - Review story mentions (IG/TikTok)

3. **Categorize each mention** using the Quick Reference table.

4. **Draft responses:**
   - Shoutout: "Appreciate you sharing this [name/context]" + follow-up thought
   - Question: answer thoroughly, link to resource if available
   - Complaint: acknowledge, express willingness to help, route to appropriate channel
   - Share: "Thanks for spreading the word" + reference something specific about their share

5. **Track mention metrics:**
   - Total mentions per day
   - Positive/neutral/negative ratio
   - Response rate (within target time)
   - Unanswered mentions

## Output Format

```markdown
# Mention Monitor: [Date]

## Mentions Today
| Time | Platform | User | Type | Content (truncated) | Priority | Response | Status |
|------|----------|------|------|--------------------|----------|----------|--------|
| 9:15 | X | @user | Shoutout | "[text]" | High | "[reply]" | Replied |
...

## Unanswered (Flagged)
[Any that couldn't be resolved — why?]

## Weekly Summary
- Total mentions: [N] | Response rate: [N]%
- Avg response time: [N] hours
- Sentiment: Positive [N]% / Neutral [N]% / Negative [N]%
- Top mentioners: @handle1, @handle2...
```

## Done Criteria

The skill is complete when:
1. All direct @mentions are categorized and replied to
2. Untagged references are noted (engagement decision made)
3. High-priority mentions responded within target time
4. Unanswered mentions flagged with reason
5. Weekly summary compiled (if end of week)

## Pitfalls

- Only monitoring @tags and missing untagged references
- Generic "thanks!" replies to every mention
- Engaging with competitor negative comparisons
- Not noticing a complaint until it's viral
- Responding to a 3-day-old mention (looks like catching up)

## Verification

Are there mentions from the last 24 hours that went unanswered? Is the response rate above 90% for high-priority? If not, adjust monitoring frequency or templates.
