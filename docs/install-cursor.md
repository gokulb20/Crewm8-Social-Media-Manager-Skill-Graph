# Install for Cursor / Windsurf

1. Clone the repository:
   ```bash
   git clone https://github.com/gokulb20/Crewm8-Social-Media-Manager-Skill-Graph.git ~/.crew-skills
   ```

2. Reference the skills in your project's rules file (`.cursorrules` or `.windsurfrules`):
   ```
   You have access to social media management skills located at ~/.crew-skills/skills/.
   These are SKILL.md files with YAML frontmatter.
   When the user asks for social media tasks, read the relevant SKILL.md.
   ```

3. For direct inclusion, create a symlink:
   ```bash
   ln -s ~/.crew-skills/skills /path/to/your/project/.cursor/skills/
   ```
