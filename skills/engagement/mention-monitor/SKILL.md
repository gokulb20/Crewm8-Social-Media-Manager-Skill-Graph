---
name: mention-monitor
description: Monitor brand mentions across all platforms, reply within 2-4 hours, categorize by sentiment and priority, and log unanswered mentions for follow-up.
version: 1.0.0
author: Gokul
license: MIT
metadata:
  hermes:
    tags: [Social, Engagement, Mentions, Monitoring, Brand-Awareness]
    related_skills: [comment-reply, dm-respond, crisis-respond]
---

# Mention Monitor

Track every time the brand is mentioned across platforms and ensure nothing goes unanswered. Mentions are social proof in public — a thanked mention builds community; an ignored mention signals that the brand doesn't care.

## When to Use

- Daily monitoring routine (check mentions across all platforms)
- After a high-performing post goes out (mention volume spikes)
- Post-launch or campaign period (elevated mention activity)
- Founder says "I keep seeing people talk about us and nobody is responding"
- Weekly mention audit — which mentions were missed?

## Quick Reference

| Mention Type | Priority | Response Time | Action |
|-------------|---------|--------------|--------|
| Direct tag/shoutout | High | Within 2 hours | Thank + add value (reply or quote tweet) |
| Question about product | Critical | Within 1 hour | Answer directly; escalate if technical |
| Complaint / negative | Critical | Within 1 hour | Acknowledge, route to `crisis-respond` if needed |
| Share/repost of content | Medium | Within 4 hours | Thank them individually |
| Casual reference (untagged) | Low | Within 24 hours | Engage if natural; don't force it |
| Competitor comparison | Medium | Within 4 hours | Monitor; engage only if factual correction needed |

## Procedure

1. Set up mention detection:
   - X: monitor @handle tags + brand name keyword searches
   - LinkedIn: @company mentions + post tags
   - Instagram: @handle tags in captions, comments, and stories
   - TikTok: @handle tags + brand name in video text/captions

2. Conduct a daily sweep (morning + afternoon minimum):
   - Check all direct @mention mentions first
   - Search for untagged brand name references
   - Check quote tweets of recent brand posts
   - Review any story mentions (IG/TikTok)

3. Categorize each mention using the Quick Reference table.

4. Draft responses:
   - Shoutout: "Appreciate you sharing this [name/context]" + add a follow-up thought
   - Question: answer thoroughly, link to resource if available
   - Complaint: acknowledge, express willingness to help, route to appropriate channel
   - Share: "Thanks for spreading the word" + reference something specific about their share

5. Track mention metrics:
   - Total mentions per day
   - Positive/neutral/negative ratio
   - Response rate (replied within target time)
   - Unanswered mentions (and why — was it intentional?)

6. Weekly mention report:
   - Volume trend (going up or down?)
   - Top mentioners (who's consistently talking about the brand?)
   - Missed opportunities: mentions that should have been replied to but slipped through
   - Sentiment shift: any change in the tone of mentions this week?

## Output Format

```markdown
# Mention Monitor: [Date]

## Mentions Today
| Time | Platform | User | Type | Content (truncated) | Priority | Response | Status |
|------|----------|------|------|--------------------|----------|----------|--------|
| 9:15 | X | @user | Shoutout | "[Mention text]" | High | "[Drafted reply]" | Replied |
| 10:30 | LinkedIn | Name | Question | "[Mention text]" | Critical | "[Drafted reply]" | Replied |
| 2:00 | IG | @user | Share | "[Mention text]" | Medium | "[Drafted reply]" | Pending |
...

## Unanswered (Flagged)
[Any mentions that couldn't be resolved — why? Next step?]

## Weekly Summary
- **Total mentions:** [N]
- **Response rate:** [N]%
- **Avg response time:** [N] hours
- **Sentiment breakdown:** Positive [N]% / Neutral [N]% / Negative [N]%
- **Top mentioners:** @handle1, @handle2, ...
```

## Pitfalls

- Only monitoring @tags and missing untagged brand references (biggest blind spot)
- Generic "thanks!" replies to every mention (looks automated after the third one)
- Engaging with competitors' negative comparisons (escalating a flame war)
- Not noticing a complaint mention until it's gone viral (2 hour windows matter)
- Responding to a mention from 3 days ago (looks like you're catching up, not listening)

## Verification

Check: are there any mentions from the last 24 hours that went unanswered? Is there a mention that received a reply but the reply was templated/generic? Is the response rate above 90% for high-priority mentions? If not, adjust the monitoring frequency or response templates.
