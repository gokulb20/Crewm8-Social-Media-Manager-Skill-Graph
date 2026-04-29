# Install for OpenAI Agents (Operator / Custom GPTs)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gokulb20/Crewm8-Social-Media-Manager-Skill-Graph.git ~/.crew-skills
   ```

2. **For Custom GPTs:** Upload individual SKILL.md files as knowledge base documents. Agents read the YAML frontmatter + markdown body directly.

3. **For OpenAI Operator or API-based agents:** Point the agent at the skills directory with flat YAML format. The agent reads `name:`, `description:`, and the body procedure to determine when and how to use each skill.

4. **No special configuration needed.** OpenAI agent skills follow the same universal SKILL.md format.
