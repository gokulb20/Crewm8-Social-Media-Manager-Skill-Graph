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
