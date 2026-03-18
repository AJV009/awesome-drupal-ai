# Deep Dive: Top Drupal AI Skills Repositories

## 1. gkastanis/drupal-claude-code-sub-agent-collective

**URL:** https://github.com/gkastanis/drupal-claude-code-sub-agent-collective
**Description:** Context Engineering Research — Hub-and-spoke coordination through Claude Code

### Architecture
```
.claude/
├── settings.json
├── settings.local.json
├── agents/ (15 agent definitions)
├── hooks/ (10 enforcement scripts + lib)
├── rules/ (8 behavioral rules)
├── agent-memory/ (persistent knowledge)
├── skills/ (15 skills)
└── commands/
```

### 15 Specialized Agents
1. Routing coordination
2. Drupal architecture specialist
3. Module development expert
4. Theme development specialist
5. Configuration management handler
6. Content migration specialist
7. Security/compliance validator
8. Performance and DevOps expert
9. Functional testing automation
10. Unit testing framework
11. Visual regression testing
12. Project management coordinator
13. Technical research agent
14. Workflow orchestrator
15. Semantic documentation architect

### Key Capabilities
- Drupal 10/11 best practices enforcement
- Security vulnerability scanning and remediation
- Automated quality gate validation
- Configuration export/import management
- Context-aware agent memory systems
- Semantic documentation mapping (business logic to code)

### MCP Server Configurations
- Default: Task Master (~20MB memory)
- Optional: Playwright, Context7, DDEV, Sequential Thinking
- Can combine all MCPs

### Assessment
Most comprehensive single-repo architecture found. Research-oriented — demonstrates how multiple specialized agents coordinate via hub-and-spoke pattern. Very relevant for the "agentic architecture" aspect of the inventory.

---

## 2. ablerz/claude-skill-drupal-module

**URL:** https://github.com/ablerz/claude-skill-drupal-module
**Description:** Claude Code skill for Drupal 11 module development with 13 API reference docs

### What It Does
Transforms Claude into a "senior Drupal architect" that generates production-ready, installable Drupal 11 modules:
- PHP 8 attributes (not annotations)
- Proper dependency injection (no `\Drupal::service()`)
- Drupal coding standards (2-space indent, PSR-4, PHPDoc)
- Cache metadata, access checks, translatable strings
- Runs quality tools after every change
- Security verification: XSS, SQL injection, CSRF, access control

### Installation Methods

**Composer (recommended):**
```json
"extra": {
    "installer-paths": {
        ".claude/skills/{$name}": ["type:claude-skill"]
    }
}
```
```bash
composer require ablerz/claude-skill-drupal-module:dev-11.x
```

**Git clone:**
```bash
git clone -b 11.x https://github.com/ablerz/claude-skill-drupal-module \
  .claude/skills/custom-drupal-module
```

### DDEV Integration
Requires custom DDEV commands: `ddev phpcs`, `ddev phpcbf`, `ddev phpstan`, `ddev phpunit`
Copy from repo: `cp .claude/skills/custom-drupal-module/ddev-commands/* .ddev/commands/web/`

### Usage
```
/custom-drupal-module
```

### Drupal Version Support
| Branch | Drupal | PHP |
|--------|--------|-----|
| 11.x | 11.x | 8.4+ |
| 12.x | 12.x | TBD |

### Staying Current
- Uses api.drupal.org/api/drupal/11.x
- Monthly GitHub Actions check for breaking changes
- License: GPL-2.0-or-later

### Assessment
HIGH quality — Composer-installable skill with automated breaking change detection. Good model for how Drupal skills should be packaged and distributed.

---

## 3. shopwareLabs/ai-coding-tools (Cross-CMS Pattern)

**URL:** https://github.com/shopwareLabs/ai-coding-tools
**Description:** Claude Code plugin marketplace for Shopware development

### Why It Matters
Shopware (another PHP CMS) has created a comprehensive AI coding tools framework. The architecture patterns are directly applicable to Drupal:
- MCP servers
- Skills
- Agents
- Hooks
- Commands

### Pattern to Learn From
- Plugin marketplace approach
- Integration of multiple AI tool types in one package
- Potentially a model for a "ddev get drupal/ai-dev-toolkit" package

---

## 4. Droptica's AGENTS.md Template

**URL:** https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/
**GitHub:** github.com/droptica/drupal-agents-md

### What It Is
AGENTS.md file placed in project root that AI assistants read at session start. Contains "everything AI needs to know about the project."

### Setup (5 minutes)
1. Download `AGENTS-TEMPLATE.md` via curl
2. Copy prompt from README into AI tool
3. AI scans project and generates customized `AGENTS.md`

### Drupal-Specific Sections
- **Infrastructure:** Drupal/PHP versions, directory structure
- **Customization:** Module prefixes, theme naming, coding standards
- **Architecture:** Content types, entities, Paragraphs, custom integrations
- **Workflow:** DDEV config, Git practices, Composer, cache config
- **Frontend:** SCSS, theming, caching strategies
- **Security:** Practices and audit configurations

### Compatible Tools
Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin

### Benefits
- Onboarding "several times faster"
- Reduced hallucinations through documented dependencies
- Fewer repetitive architecture explanations

### Limitations
- Large projects (50+ custom modules) create significant overhead
- Manual regeneration after structural changes
- Documentation quality depends on existing code organization

### Assessment
HIGH value — practical, 5-minute setup, broad tool compatibility. Should be in the "standard" list.

---

## 5. scottfalconer/drupal-contribute-fix

**URL:** https://github.com/scottfalconer/drupal-contribute-fix
**Stars:** 15
**Description:** Agentic skill for converting local Drupal fixes into maintainer-friendly contributions

### Assessment
Directly addresses the "how to contribute to Drupal using AI" requirement. Converts local patch work into proper drupal.org merge request format. HIGH relevance.

---

## 6. ronaldtebrake/drupal-coding-standards-skill

**URL:** https://github.com/ronaldtebrake/drupal-coding-standards-skill
**Stars:** 6
**Description:** Agentic Skill for working with Drupal coding standards

### Assessment
Enforces PHPCS/PHPStan Drupal coding standards via AI. Essential for code quality. Should be in "standard" list.

---

## Key Pattern: Composer-Installable Skills

The ablerz/claude-skill-drupal-module demonstrates a pattern where skills can be installed via Composer using `installer-paths`. This is a significant distribution mechanism for the Drupal ecosystem where Composer is the standard package manager.

```json
"extra": {
    "installer-paths": {
        ".claude/skills/{$name}": ["type:claude-skill"]
    }
}
```

This pattern should be adopted as a standard for distributing Drupal AI skills.
