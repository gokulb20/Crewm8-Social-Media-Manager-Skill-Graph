# Contributing

Thanks for your interest in improving the Crewm8 Social Skill Graph. This is a community-maintained, open-source skill pack for any agent system.

## How to Add a New Skill

1. **Check if it already exists.** Review the skill index in README.md and the list in GLOSSARY.md.

2. **Choose the right category.** Skills live under `skills/[category]/[skill-name]/SKILL.md`.

3. **Use the standard format:**

```yaml
---
name: skill-name
description: One-line, action-oriented description
version: 2.0.0
author: Crewm8
maintainer: Your Name (github.com/yourhandle)
license: MIT
homepage: https://crewm8.ai
tags: [social, category, keywords]
related_skills: [other-skill-names]
inputs_required: [what-the-agent-needs-before-starting]
deliverables: [what-the-skill-produces]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
---
```

Body sections: **Purpose → When to Use → Inputs Required → Quick Reference → Procedure → Output Format → Platform Notes → Done Criteria → Pitfalls → Verification → Example**

4. **Make it agent-agnostic.** Use generic capability names (`web-search`, `text-generation`), not agent-specific tool names. Don't assume a specific scheduling tool.

5. **Add an example.** Each skill needs at least one worked example (input → process → output).

6. **Update supporting files.**
   - Add the skill to the index in README.md
   - Add any new terms to GLOSSARY.md
   - Update SKILL_GRAPH.md if your skill has dependencies

7. **Submit a pull request.**

## How to Improve an Existing Skill

- Open an issue describing the change
- Submit a PR with the updated SKILL.md
- Bump the patch version (e.g., 2.0.0 → 2.0.1) for bug fixes
- Bump the minor version (e.g., 2.0.0 → 2.1.0) for content additions

## Guidelines

- Skills must be agent-agnostic (work with any markdown-skill-aware agent)
- No external dependencies unless documented in the skill's inputs
- No tracking, analytics, or API calls hardcoded into skill instructions
- Keep skills focused — one job, done well
- Include verifiable Done Criteria (not just "it feels right")
- Write in plain English. Assume the agent reads the markdown directly.

## Code of Conduct

Be respectful. Be helpful. Don't submit skills that require paid tools or vendor lock-in.
