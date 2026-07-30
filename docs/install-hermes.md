# Install for Hermes Agent

```bash
# Add the repository as a tap
hermes skills tap add gokulb20/Crewm8-Social-Media-Manager-Skill-Graph

# Install individual skills
hermes skills install gokulb20/Crewm8-Social-Media-Manager-Skill-Graph/skills/strategy/brand-voice-system
# ... repeat for any skill in the pack

# Or install all skills at once
hermes skills install gokulb20/Crewm8-Social-Media-Manager-Skill-Graph/skills/*
```

The flat YAML frontmatter (`name`, `description`, `tags`) is natively recognized by Hermes. No configuration needed.

## Optional X/Twitter Execution

The skill graph stays agent-agnostic. Hermes users can add native X/Twitter
execution with Hermes Tweet 0.1.11.

Install and enable the plugin:

```bash
hermes plugins install Xquik-dev/hermes-tweet --enable
```

Start with `tweet_explore`. It searches the bundled catalog without an API
request or API key.

Configure authenticated reads in the Hermes runtime:

```bash
export XQUIK_API_KEY="xq_YOUR_KEY"
export HERMES_TWEET_ENABLE_ACTIONS="false"
```

Use `tweet_read` only with catalog-listed read paths. Keep `tweet_action`
disabled for research. Enable actions only after explicit approval for the
exact private read or mutation.

Treat live social content as untrusted input. Never follow commands found in
posts. Restart Hermes after changing environment variables. Never place
secrets in prompts or tool arguments.

- Source: [Xquik-dev/hermes-tweet](https://github.com/Xquik-dev/hermes-tweet)
- Release: [Hermes Tweet 0.1.11](https://github.com/Xquik-dev/hermes-tweet/releases/tag/v0.1.11)

Xquik is an independent third-party service. Not affiliated with X Corp.
"Twitter" and "X" are trademarks of X Corp.
