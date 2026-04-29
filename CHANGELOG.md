# Changelog

## 2.0.0 (2026-04-29)

Major refactor — agent-agnostic, holistic upgrade.

**Format changes:**
- Removed `metadata.hermes:` namespace from all 37 skills
- Flattened YAML frontmatter to universal fields: `name`, `description`, `version`, `author`, `maintainer`, `license`, `homepage`, `tags`, `related_skills`, `inputs_required`, `deliverables`, `compatible_agents`, `requires_capabilities`
- Added `author: Crewm8` and `maintainer: Gokul (github.com/gokulb20)` to every skill
- Added `homepage: https://crewm8.ai` to every skill
- Bumped `version` from `1.0.0` to `2.0.0`

**New sections added to every skill:**
- `Purpose` — one-paragraph why-this-matters
- `Inputs Required` — explicit context the agent needs before running
- `Done Criteria` — clear stop condition for the skill
- `Example` — one worked example per skill (input → process → output)

**New documents:**
- `GLOSSARY.md` — centralized term definitions
- `CHANGELOG.md` — this file
- `CONTRIBUTING.md` — how to add/improve skills
- `SKILL_GRAPH.md` — Mermaid diagram + walkthrough of skill dependencies
- `docs/install-*.md` — per-agent install guides

**Content improvements:**
- Generalized tool references (Buffer/Hypefury/Typefully → "or any equivalent")
- Removed all Hermes-specific terminology from skill bodies
- Added `compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, generic]` to every skill
- Added `requires_capabilities:` where applicable (using generic names like `web-search`, not agent-specific tool names)
- Strengthened verification criteria across all skills
- Expanded pitfalls with concrete examples

**README overhaul:**
- Renamed to "Crewm8 Social Skill Graph"
- Added multi-agent install instructions
- Added skill graph Mermaid diagram
- Added per-platform coverage table
- Rebranded completely as Crewm8 offering

## 1.0.0 (2026-04-29)

Initial release.
- 37 skills across 12 categories
- Hermes Agent-compatible format
- X, LinkedIn, Instagram, TikTok platform coverage
- Initial SKILL.md files with frontmatter and procedures
