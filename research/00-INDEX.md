# Research & Inventory Dump — Index

## Research Files

| # | File | Topic | Key Findings |
|---|------|-------|-------------|
| 01 | agent-skills-drupal-repos.md | Agent Skills / SKILL.md repos | 12+ repos found, agentskills.io spec, Composer-installable pattern |
| 02 | drupal-ai-initiative-and-community.md | Drupal AI Initiative & community | $1.5M funding, 28 orgs, 50+ contributors, leadership team |
| 03 | agentic-architecture-drupal.md | Agentic patterns & frameworks | AI Agents module, FlowDrop, LLPhant PHP, code review, CI/CD |
| 04 | ddev-ai-plugins.md | DDEV AI plugins & addons | 15+ plugins found, MCP bridges, Ollama, Claude Code integrations |
| 05 | mcp-servers-drupal.md | MCP servers for Drupal | 10+ servers, DrupalMCP.io, Drush MCP bridge, PHP SDK |
| 06 | drupal-ai-modules-comprehensive.md | All drupal.org AI modules | 60+ modules cataloged across all categories |
| 07 | drupal-ai-roadmap-2026-canvas.md | 2026 roadmap & Canvas AI | 8 core capabilities, Canvas 3-agent architecture, Drupal CMS 2.0 |
| 08 | top-skills-repos-deep-dive.md | Detailed repo analysis | Sub-agent collective, Composer skills, Shopware patterns |
| 09 | practical-workflows-blog-posts.md | Developer workflow deep dives | Tag1, Rockowitz, te Brake, Droptica, DDEV patterns |
| 10 | events-podcasts-training.md | Events, podcasts & training | Talking Drupal episodes, hackathons, learning resources, key people |
| 11 | alternative-ai-tools-starterkit.md | Cursor, Copilot, Kiro, Nebula, llms.txt | Cursor rules, Copilot guides, Kiro format, Nebula=Canvas template, AI Starterkit proposal |
| 12 | eca-providers-governance.md | ECA+AI, providers, governance | 48+ providers, Langfuse observability, vector DBs, security advisory, Claude SDK |
| 13 | drupal-recipes-and-ai.md | Drupal Recipes as AI distribution | CMS AI recipe, AI Chatbot recipe, llms.txt recipe, ddev-drupal-ai recipe proposal |
| 14 | cross-cms-ai-patterns.md | Cross-CMS AI tool comparison | Laravel Boost, Shopware, WordPress, Symfony — patterns to learn from |
| 16 | php-analysis-testing-ai.md | PHP analysis + testing + AI | PHPStan MCP, Rector, PHPCS, AI testing, code review, debugging, upgrades |
| 17 | detailed-skills-inventory.md | Every skill in top repos | grasmash (5), madsnorgaard (5+1+5), scottfalconer (4 modes), gxleano (20!), gkastanis (16+4+10), canvas (7), oscarnovasf (3-plugin) |
| 18 | claude-code-plugin-ecosystem.md | Plugin architecture | Skills vs plugins, official plugins, hooks, distribution methods, "standard" implications |
| 19 | assessment-and-classification.md | **SYNTHESIS** | Maturity ratings for all tools, "Standard" list, Comprehensive inventory |
| 20 | final-niche-findings.md | Usage stats, core issue, DMU | 13,293 installs, Dries' core issue #3570498, DMU revived in 24h, no CLAUDE.md in core |
| 21 | context-files-platform-compatibility.md | Context files + tool compat | AGENTS.md in core issue #3568936, CCC module, platform compatibility matrix, 4 new repos |
| 22 | drupalcon-chicago-2026-surge-aiskills.md | DrupalCon Chicago + Surge + ai_skills | 21+ AI sessions THIS WEEK, Surge module, ai_skills module, Bloomidea drush-mcp, Context7 Drupal data |
| 23 | drupalorg-issue-deep-dives.md | Issue queue DISCUSSIONS | Full comment threads from #3541110, #3565489, #3568936, #3570498, #3574093 |
| 24 | general-ai-tools-symfony-ai.md | General AI tools + Symfony AI | 2026 agent landscape, Symfony AI components, best practices, MCP patterns, drupalorg-cli |
| 25 | final-niche-gaps-filled.md | Commerce, moderation, image gen | AI Commerce module, adaptable modules, amazee.ai details, completeness assessment |
| 26 | video-content-demos-new-modules.md | Videos, demos, figma_canvas_ai | Official demos, DrupalForge templates, figma_canvas_ai module, research completion status |

## Preliminary "Standard" Recommendations

Based on research, the recommended starter pack for AI-assisted Drupal development:

### DDEV Plugins
1. `FreelyGive/ddev-claude-code` — Claude Code in DDEV container
2. `Drupal-AI/ddev-drupal-ai` — Drupal AI module dev environment
3. `codingsasi/ddev-mcp` — MCP server for DDEV (Drush, Playwright)
4. `tyler36/ddev-ollama` — Local LLM via Ollama

### Agent Skills (SKILL.md)
1. `ablerz/claude-skill-drupal-module` — Module development (Composer-installable)
2. `ronaldtebrake/drupal-coding-standards-skill` — Coding standards enforcement
3. `scottfalconer/drupal-contribute-fix` — Contributing to drupal.org

### Context Files
1. `droptica/drupal-agents-md` — AGENTS.md template (5-min setup, 10+ tool support)
2. Custom CLAUDE.md with Drupal best practices

### MCP Servers
1. `drupal.org/project/mcp_server` — Turn Drupal into MCP server
2. `Cleversoft-IT/drupal-tools-mcp` — Query drupal.org + Drush via MCP
3. `@playwright/mcp` — Browser testing

### Drupal Modules (AI Framework)
1. `drupal/ai` — Core AI framework
2. `drupal/ai_agents` — Agentic framework
3. Provider module for chosen LLM (OpenAI, Anthropic, Ollama, etc.)

## Statistics (Final)

- **Total research:** 5,013 lines across 27 files (260KB)
- **Total unique URLs referenced:** 400+
- **GitHub repos cataloged:** 40+
- **drupal.org modules cataloged:** 70+
- **Individual AI skills inventoried:** 80+
- **Blog posts analyzed in depth:** 25+
- **Events/podcasts documented:** 15+
- **Key people identified:** 25+
- **Organizations involved:** 28+
- **drupal.org issues analyzed comment-by-comment:** 5
- **AI tool platforms covered:** Claude Code, Cursor, Copilot, Kiro, Gemini CLI, Aider, OpenCode, Cline, Roo Code, Codex, Windsurf, Zed, Devin, Junie

## Research Methodology

22+ parallel research agents dispatched across 8 waves over 10+ Ralph loop iterations:
1. **Wave 1 (6 agents):** DDEV plugins, Drupal modules, MCP servers, Agent Skills, Community efforts, Agentic architecture
2. **Wave 2 (4 agents):** Roadmap 2026 & Canvas, Top repos deep-dive, Blog post workflows, Events & training
3. **Wave 3 (2 agents):** Alternative AI tools & Starterkit proposal, ECA + Providers + Governance
4. **Wave 4 (3 agents):** Drupal Recipes + AI, Cross-CMS patterns, PHP analysis + testing
5. **Wave 5 (3 agents):** Top repo content deep-dive, Claude Code plugin ecosystem, Developer experience
6. **Wave 6 (1 agent):** Latest March 2026 developments, DrupalCon Chicago schedule
7. **Wave 7 (3 agents):** drupal.org issue comment threads, general AI tools + Symfony AI, developer blog deep-dives
8. **Wave 8 (2 agents):** Final niche gaps (Commerce, moderation, image gen), video content

Each agent performed multiple web searches and page fetches, covering 90+ distinct search queries. Diminishing returns confirmed after wave 7.

## Key Gaps Identified

1. **No unified one-command setup** exists yet (AI Coding Starterkit proposal #3541110 is active but unassigned)
2. **Drupal core lacks AGENTS.md** — active issue #3568936 proposes adding one
3. **First-class agent-skills support** proposed for AI module (#3565489)
4. **Context Control Center (CCC)** is the Drupal-native context management approach — active sprint planning
5. **CI/CD AI integration** is emerging but not standardized
7. **AGENTS.md** is the most portable context file (10+ tool support) — should be the default recommendation
8. **SKILL.md** (agentskills.io) has 30+ tool support — the standard skill format
