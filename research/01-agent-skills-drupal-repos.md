# Agent Skills & SKILL.md Repositories for Drupal Development

## agentskills.io Specification

**URL:** https://agentskills.io/specification
**Standard supported by:** 30+ tools including Claude Code, Kiro CLI, Cursor, VS Code Copilot, Gemini CLI, OpenHands, Roo Code, Junie

### Format
- A skill is a directory with a `SKILL.md` file (required) + optional `scripts/`, `references/`, `assets/` dirs
- SKILL.md has YAML frontmatter: `name` (required, max 64 chars, lowercase+hyphens), `description` (required, max 1024 chars), optional `license`, `compatibility`, `metadata`, `allowed-tools`
- Body content is markdown with step-by-step instructions, examples, edge cases
- Progressive disclosure: metadata (~100 tokens) loaded at startup; full SKILL.md loaded on activation; reference files loaded on demand
- Keep SKILL.md under 500 lines; move detailed reference material to separate files
- Validation tool: `skills-ref validate ./my-skill` from https://github.com/agentskills/agentskills

### Anthropic Official Skills Repo
**URL:** https://github.com/anthropics/skills
**Stars:** 95.5k | **Forks:** 10.3k
Categories: Creative & Design, Development & Technical, Enterprise & Communication, Document Skills (pdf, docx, pptx, xlsx)
Install via: `/plugin marketplace add anthropics/skills`

---

## Drupal-Specific Skills Repositories on GitHub

### 1. madsnorgaard/drupal-agent-resources
- **URL:** https://github.com/madsnorgaard/drupal-agent-resources
- **Description:** Reusable Claude Code resources for Drupal development - skills, agents, and commands
- **Stars:** 32 | **Updated:** ~March 2026
- **Relevance:** HIGH — comprehensive collection of reusable Drupal AI resources

### 2. grasmash/drupal-claude-skills
- **URL:** https://github.com/grasmash/drupal-claude-skills
- **Description:** Drupal Claude skills collection
- **Language:** Shell
- **Stars:** 24 | **Updated:** Nov 5, 2025
- **Relevance:** HIGH — from Matthew Grasmick (well-known Drupal contributor, creator of BLT/Acquia CLI)

### 3. scottfalconer/drupal-contribute-fix
- **URL:** https://github.com/scottfalconer/drupal-contribute-fix
- **Description:** Agentic skill for converting local Drupal fixes into maintainer-friendly contributions
- **Language:** Python
- **Stars:** 15 | **Updated:** ~March 2026
- **Relevance:** HIGH — directly addresses contributing to drupal.org using AI

### 4. jamieaa64/Drupal-DDEV-Setup-Claude-Skill
- **URL:** https://github.com/jamieaa64/Drupal-DDEV-Setup-Claude-Skill
- **Description:** Automates setup for new or existing Drupal projects using DDEV
- **Language:** Shell
- **Stars:** 9 | **Updated:** Nov 12, 2025
- **Relevance:** HIGH — FreelyGive, DDEV + Drupal setup automation

### 5. ronaldtebrake/drupal-coding-standards-skill
- **URL:** https://github.com/ronaldtebrake/drupal-coding-standards-skill
- **Description:** An Agentic Skill for working with coding standards
- **Stars:** 6 | **Updated:** Jan 8, 2026
- **Relevance:** HIGH — enforces Drupal coding standards via AI

### 6. ablerz/claude-skill-drupal-module
- **URL:** https://github.com/ablerz/claude-skill-drupal-module
- **Description:** Claude Code skill for Drupal 11 module development. Bundles 13 API reference docs
- **Language:** Shell
- **Relevance:** HIGH — comprehensive module development skill with reference material

### 7. gxleano/drupal-agentic-workflow
- **URL:** https://github.com/gxleano/drupal-agentic-workflow
- **Description:** Claude Code template featuring 11 AI skills, post-generation linting, and coding standards setup
- **Language:** Shell
- **Updated:** ~March 2026
- **Relevance:** HIGH — full agentic workflow with multiple skills

### 8. gkastanis/drupal-workflow
- **URL:** https://github.com/gkastanis/drupal-workflow
- **Description:** Claude Code plugin with 16 skills, 4 agents, 10 commands, and quality-gate hooks
- **Language:** Shell
- **Updated:** ~March 2026
- **Relevance:** HIGH — most comprehensive single plugin found (16 skills!)

### 9. zivtech/drupal-critic
- **URL:** https://github.com/zivtech/drupal-critic
- **Description:** Drupal-specific code review skill and agent with external skill references
- **Language:** Python
- **Stars:** 3 | **Updated:** ~March 2026
- **Relevance:** MEDIUM-HIGH — specialized code review for Drupal from Zivtech agency

### 10. drupal-canvas/skills
- **URL:** https://github.com/drupal-canvas/skills
- **Description:** Collection of agent skills for developing Drupal Canvas Code Components
- **Stars:** 1 | **Updated:** ~March 2026
- **Relevance:** MEDIUM — specifically for Canvas/Experience Builder components

### 11. oscarnovasf/claude-drupal-plugin
- **URL:** https://github.com/oscarnovasf/claude-drupal-plugin
- **Description:** Spanish-language plugin featuring agents, commands, and skills for Drupal projects
- **Language:** TypeScript
- **Updated:** ~March 2026
- **Relevance:** MEDIUM — Spanish-language, shows international adoption

### 12. aldunchev/ai-fe-skills
- **URL:** https://github.com/aldunchev/ai-fe-skills
- **Description:** Agent skills for frontend development — Drupal, AEM, performance optimization. Cross-compatible SKILL.md format
- **Language:** Shell
- **Topics:** ai, skills, ai-skills
- **Updated:** ~March 2026
- **Relevance:** MEDIUM — frontend-focused, covers Drupal and AEM

---

## Other AI Tool Configuration Files for Drupal

### .cursorrules for Drupal
- GitHub code search for ".cursorrules drupal" requires authentication — limited public results
- Blog post reference: ronaldtebrake.nl mentions AI coding starter kit inspired by Laravel Boost

### CLAUDE.md for Drupal
- GitHub code search for "CLAUDE.md drupal" requires authentication
- Known to exist in various Drupal projects but not easily searchable publicly
- Referenced in jrockowitz.com blog about using .claude folder in repo

### GitHub Copilot Instructions for Drupal
- No significant public copilot-instructions files found for Drupal specifically
- Gap in the ecosystem

### AGENTS.md for Drupal
- Droptica blog post: "AGENTS.md tool: How AI speeds up Drupal development"
- URL: https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/
- Works with Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin

---

## Assessment

The Drupal agent skills ecosystem is **actively growing** with 12+ dedicated repositories found. Key observations:
- Most are Claude Code focused (SKILL.md format)
- Several comprehensive workflow packages exist (gkastanis: 16 skills, gxleano: 11 skills)
- Notable gap: fewer Cursor/.cursorrules and Copilot-specific configurations
- Contributing to drupal.org via AI is specifically addressed (scottfalconer/drupal-contribute-fix)
- International adoption (Spanish-language plugin)
- Canvas/Experience Builder skills emerging
