# Install for Any Markdown-Aware Agent

1. Clone the repository:
   ```bash
   git clone https://github.com/gokulb20/Crewm8-Social-Media-Manager-Skill-Graph.git
   ```

2. Point your agent at the `skills/` directory.

3. Each SKILL.md follows the universal format:
   ```yaml
   ---
   name: skill-name
   description: Action-oriented one-liner
   tags: [keywords]
   ---
   ```

4. The agent reads the description to determine when to load the skill, then follows the numbered procedure in the body.

5. No agent-specific metadata is required. All skills declare `compatible_agents: [generic]`.
