# Detailed Skills Inventory: Contents of Top Drupal AI Repos

## 1. grasmash/drupal-claude-skills (24 stars)

**Author:** Matthew Grasmick (Acquia, creator of BLT/Acquia CLI)

### 5 Skills Included

| Skill | Source | Coverage |
|-------|--------|----------|
| drupal-at-your-fingertips | drupalatyourfingertips.com by Selwyn Polit | 50+ topics: core APIs, content mgmt, forms, routing, theming, caching, testing |
| drupal-contrib-mgmt | Original | Composer workflows, compatibility checking, patch management, dependency troubleshooting |
| drupal-config-mgmt | Original | Safe inspection techniques, environment synchronization workflows |
| drupal-ddev | Original | Environment configuration, database operations, debugging, performance optimization |
| ivangrynenko-cursorrules-drupal | Ivan Grynenko's Cursor Rules | OWASP Top 10 security: auth, access control, injection prevention, cryptography |

### Installation
- **Project-specific:** Copy `.claude` directory to project root
- **Global:** Copy to `~/.config/claude/skills` or symlink
- Skills activate **contextually** — module updates trigger contrib mgmt, security reviews invoke OWASP

### Roadmap
Planned: performance optimization, advanced theming with SDC, headless Drupal, commerce, migration, hosting-specific skills

---

## 2. madsnorgaard/drupal-agent-resources (32 stars)

**Author:** Mads Norgaard
**Package Manager:** `agr` CLI tool (agent-resources)

### 5 Skills
| Skill | Purpose |
|-------|---------|
| drupal-expert | Drupal 10/11 development, modules, themes, services, hooks |
| drupal-security | Security expertise: XSS, SQL injection, access bypass warnings |
| drupal-migration | D7-to-D10 migrations, CSV imports, custom plugins |
| ddev-expert | DDEV local dev, Xdebug, custom services |
| docker-local | Custom Docker Compose patterns for non-DDEV projects |

### 1 Agent
| Agent | Purpose |
|-------|---------|
| drupal-reviewer | Code review: security, standards, performance, DI compliance |

### 5 Commands
| Command | Purpose |
|---------|---------|
| /drush-check | Health checks on Drupal sites |
| /module-scaffold [name] | Generate new modules with best-practice structure |
| /config-export | Export config with review workflow |
| /security-audit [path] | Audit for security vulnerabilities |
| /performance-check [path] | Analyze caching, queries, optimization |

### Install
```bash
agr add madsnorgaard/drupal-agent-resources/drupal-expert
agr add madsnorgaard/drupal-agent-resources/drupal-reviewer
```

### Architecture
Three-tier: Skills (contextual expertise), Commands (user-triggered), Agents (task delegation)

---

## 3. scottfalconer/drupal-contribute-fix (15 stars)

**Purpose:** Convert local Drupal fixes into maintainer-friendly drupal.org contributions

### Three Rules
1. **Targeted:** Searches Drupal.org first. If fix exists, stops and recommends it
2. **High-Quality:** PHP lint by default; PHPCS if available; flags hack patterns
3. **Maintainer-First:** Never auto-posts. Generates clean artifacts for review

### Workflow Modes
| Mode | Purpose |
|------|---------|
| preflight | Search-only verification |
| package | Generate MR artifacts and local diffs |
| test | Generate RTBC comments for existing fixes |
| reroll | Handle legacy patch adaptation |

### Python Modules
- `drupalorg_api.py` — Drupal.org API client
- `issue_matcher.py` — Issue search/scoring
- `baseline_repo.py` — Git baseline resolution
- `patch_packager.py` — Local diff generation
- `report_writer.py` — Output file generation
- `security_detector.py` — Security flagging
- `validator.py` — Code validation

### Exit Codes (Gatekeeper)
| Code | Meaning |
|------|---------|
| 0 | Proceed with local artifact generation |
| 10 | Redirect to existing upstream solution |
| 30 | Review required (complex/hacky fix) |
| 40 | Error encountered |
| 50 | Security issue flagged |

### Companion Tool
**drupal-issue-queue** — deeper triage with status/priority/category filtering

---

## 4. gxleano/drupal-agentic-workflow (20 skills!)

**Note:** Originally reported as 11 skills, actually contains **20 skills**

### All 20 Skills
| Skill | Type | Purpose |
|-------|------|---------|
| drupal-expert | Inline | Knowledge base and references |
| scaffold | Inline | Generate modules, services, plugins, forms, hooks |
| code-review | Agent | Architectural reviews with reports |
| generate-tests | Agent | PHPUnit test generation |
| debug | Inline | Code-level troubleshooting |
| ddev | Inline | Environment management |
| migrate | Inline | Migration management |
| solr-setup | Inline | DDEV Solr configuration |
| drupal-frontend-expert | Inline | Twig, SDC, theming, CSS/JS, accessibility |
| drupal-site-builder-expert | Inline | Views, content types, Layout Builder, config |
| drupal-security | Inline | Proactive security practices |
| update-module | Inline | Safe contrib module updates |
| config-management | Inline | Config export/import, Config Split, Recipes |
| performance | Inline | Caching, queries, BigPipe, profiling |
| drush | Inline | CLI reference and deprecated commands |
| refactor | Inline | Code smell detection and guidance |
| doctor | Inline | Workflow health checks |
| accessibility | Inline | WCAG 2.2 compliance and ARIA patterns |
| api | Inline | REST, JSON:API, GraphQL support |
| entity | Inline | Custom content/config entity types |

### 3 Automated Hooks
- **pre-bash-guard.sh** — Blocks destructive Bash commands
- **post-generation-lint.sh** — Auto-runs phpcbf, phpcs, prettier, eslint, security scanning
- **prompt-context.sh** — Optional git status injection

### Setup
```bash
git clone <repo> ~/drupal-agentic-workflow
cd /path/to/drupal-project && claude /init
~/drupal-agentic-workflow/bin/setup.sh .
```

---

## 5. gkastanis/drupal-workflow (16 skills, 4 agents, 10 commands)

### 16 Skills
| Skill | Purpose |
|-------|---------|
| drupal-rules | Core dev patterns: code quality, security, services, testing |
| drupal-testing | Practical verification: curl, drush eval, test scripts |
| drupal-service-di | Service definitions, DI patterns, interfaces |
| drupal-entity-api | Field types, entity CRUD, view modes, access |
| drupal-caching | Cache bins, tags, contexts, CacheableMetadata |
| drupal-hook-patterns | OOP hooks (D11), form alters, entity hooks |
| drupal-security-patterns | OWASP, access control, input sanitization |
| drupal-coding-standards | PHPCs, PHPStan, naming, style enforcement |
| drupal-conventions | Translations, CSS, error handling |
| drupal-config-management | Config split, ignore, readonly, environments |
| twig-templating | Template patterns, filters, theme suggestions, SDC |
| verification-before-completion | Gate preventing untested claims |
| semantic-docs | Business logic-to-code mappings via Logic IDs |
| discover | Docs-first codebase discovery (service:, hook:, deps:) |
| structural-index | Auto-generated awareness parsing *.services.yml, *.routing.yml |
| writing-plans | Implementation plans for sub-agents |

### 4 Agents
| Agent | Purpose |
|-------|---------|
| drupal-builder | Full-stack: modules, themes, config, migrations, performance |
| drupal-reviewer | Architecture, security audit, standards, test writing |
| drupal-verifier | Verification via ddev drush eval, curl smoke tests |
| semantic-architect | Semantic docs: business index, tech specs, Logic IDs |

### 10 Commands
| Command | Purpose |
|---------|---------|
| /drupal-test [type] | Run verification tests |
| /drupal-verify | Verify via smoke tests and drush checks |
| /implement | Implement changes with validation |
| /verify-changes | Verify completeness and consistency |
| /drupal-bootstrap | Auto-detect state, run 3-step pipeline |
| /drupal-prime | Load project overview (~2500 tokens) |
| /drupal-refresh | Regenerate structural index |
| /drupal-status | Check docs, index, staleness |
| /drupal-blast-radius [FEATURE] | Analyze dependencies |
| /drupal-semantic [cmd] | Manage semantic documentation |

### Quality-Gate Hooks
| Event | Action |
|-------|--------|
| SessionStart | Display activation, auto-regen structural index if stale |
| PreToolUse | Block access to settings.php, .env, credentials |
| PostToolUse | PHP lint on modified files, staleness warnings |
| SubagentStart | Inject Drupal context, version detection |
| TaskCompleted | Quality gate checks |

---

## 6. drupal-canvas/skills (1 star)

### 7 Skills for Canvas Code Components
1. canvas-component-composability
2. canvas-component-definition
3. canvas-component-metadata
4. canvas-component-upload
5. canvas-component-utils
6. canvas-data-fetching
7. canvas-styling-conventions

**Install:** `npx skills add drupal-canvas/skills`

---

## 7. oscarnovasf/claude-drupal-plugin (Spanish, TypeScript)

### Three-Plugin Architecture
| Plugin | Scope | Requires |
|--------|-------|----------|
| drupal-global | Base: shared MCPs, agents, commands, skills | None |
| drupal-backend | Backend: modules, APIs, services, migrations | drupal-global |
| drupal-frontend | Frontend: theming, Twig, CSS/JS, a11y | drupal-global |

### MCPs Included
- **Context7** — Updated library documentation
- **Obsidian** — Vault integration
- **Playwright** — Browser automation

### Agents
- context7, drupal-backend, drupal-frontend

### Commands & Skills (drupal-global)
- /drupal-setup, /update-changelog
- drupal-setup skill, change-name skill, config-ia skill, drupal-reference skill

### Frontend-Specific
- /component — Generate SDC with Twig templates and schema

### Security Hooks
Protected paths: node_modules, vendor, .git, core/, settings.php, dist/, build/

### Install
```bash
claude plugin marketplace add https://github.com/oscarnovasf/claude-drupal-plugin.git
claude plugin install drupal-global@drupal-tools
claude plugin install drupal-backend@drupal-tools
claude plugin install drupal-frontend@drupal-tools
```
