# Install for Factory Droid

**Project-level** (shared with the team):

```bash
# Clone into project
git clone https://github.com/gokulb20/Crewm8-Social-Media-Manager-Skill-Graph.git /tmp/crew-skills
cp -r /tmp/crew-skills/skills/* .factory/skills/
```

**Personal-level** (available across all your projects):

```bash
cp -r /tmp/crew-skills/skills/* ~/.factory/skills/
```

Droid reads `.factory/skills/[category]/[skill-name]/SKILL.md` files. The flat YAML format with `name`, `description`, `tags` is natively supported.
