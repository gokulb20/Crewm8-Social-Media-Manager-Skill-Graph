# Install for Claude Code

```bash
# Clone the repository
git clone https://github.com/gokulb20/Crewm8-Social-Media-Manager-Skill-Graph.git ~/.crew-skills

# Claude Code looks for skills in .claude/skills/ within the project
# Symlink the skills directory into your project
ln -s ~/.crew-skills/skills /path/to/your/project/.claude/skills/

# Or copy directly
cp -r ~/.crew-skills/skills/* /path/to/your/project/.claude/skills/
```

Claude Code reads SKILL.md files with YAML frontmatter (specifically `name` and `description` fields) to make skills discoverable. The `description` field is used by Claude to match skills to user requests.
