# Assessment & Classification: Drupal AI Coding Tools

This file synthesizes all research (files 01-25) into the two deliverable structures required:
1. **"Standard" Default Set** — curated, opinionated, day-one install
2. **Comprehensive Inventory** — every tool with brief analysis

---

## LIST 1: "Standard" Default Set

The recommended starter pack for AI-assisted Drupal development. Should be installable via a single DDEV plugin or command.

### Tier 1: Environment Setup (DDEV Addons)

| Tool | Install | What It Does | Maturity |
|------|---------|-------------|----------|
| FreelyGive/ddev-claude-code | `ddev get FreelyGive/ddev-claude-code` | Claude Code in DDEV container | ★★★★ Stable, by core AI initiative team |
| Drupal-AI/ddev-drupal-ai | `ddev get Drupal-AI/ddev-drupal-ai` | Drupal AI module dev environment | ★★★ Active, recipe integration planned |
| tyler36/ddev-ollama | `ddev get tyler36/ddev-ollama` | Local LLM via Ollama (free, private) | ★★★ Stable |

### Tier 2: AI Skills (SKILL.md / Claude Code)

| Tool | Install | What It Does | Maturity |
|------|---------|-------------|----------|
| ablerz/claude-skill-drupal-module | `composer require ablerz/claude-skill-drupal-module` | Module development with 13 API refs, DDEV quality commands | ★★★★ Excellent — Composer installable, auto-updating |
| ronaldtebrake/drupal-coding-standards-skill | Git clone to `.claude/skills/` | Drupal coding standards enforcement | ★★★ Good, focused |
| scottfalconer/drupal-contribute-fix | Git clone to `.claude/skills/` | Convert local fixes to drupal.org contributions | ★★★★ Excellent — Python, API integration, gatekeeper patterns |

### Tier 3: Project Context Files

| Tool | Install | What It Does | Maturity |
|------|---------|-------------|----------|
| droptica/drupal-agents-md | `curl` template + AI generation | AGENTS.md for project context (10+ tool support) | ★★★★ Excellent — 5-min setup, universal |
| Custom CLAUDE.md | Manual or AI-generated | Drupal best practices for Claude Code | ★★★ Standard practice |
| drupal/claude_code | `composer require --dev drupal/claude_code` | Scaffolded CLAUDE.md with Drupal conventions | ★★★ Official FreelyGive |
| amazeeio/drupal-agents-md | Git clone | Alternative AGENTS.md (DDEV + Vanilla variants) | ★★★ From amazee.io |

### Tier 4: MCP Servers

| Tool | Install | What It Does | Maturity |
|------|---------|-------------|----------|
| codingsasi/ddev-mcp | `ddev get codingsasi/ddev-mcp` or npm | DDEV MCP with Drush, Playwright, platform.sh | ★★★ Good — listed on LobeHub, npm |
| @playwright/mcp | npm install | Browser automation for testing Drupal sites | ★★★★ Microsoft-maintained |
| Cleversoft-IT/drupal-tools-mcp | npm | Query drupal.org modules + Drush commands via MCP | ★★★ Good |

### Tier 5: Drupal Modules (Site-Level AI)

| Module | Install | What It Does | Maturity |
|--------|---------|-------------|----------|
| drupal/ai | `composer require drupal/ai` | Core AI framework, 48+ providers, automators | ★★★★★ Production, security advisory patched |
| drupal/ai_agents | `composer require drupal/ai_agents` | Agentic framework with Field/Content/Taxonomy agents | ★★★★ Stable |
| Provider (choose one) | `composer require drupal/ai_provider_*` | OpenAI, Anthropic, Ollama, etc. | ★★★★ Multiple options |

---

## LIST 2: Comprehensive Inventory

### Category A: Agent Skills Repositories

| # | Repo | Stars | Skills | Install Method | Assessment |
|---|------|-------|--------|---------------|------------|
| A1 | madsnorgaard/drupal-agent-resources | 32 | 5 skills + 1 agent + 5 commands | agr CLI | ★★★★ Most popular, well-structured three-tier architecture |
| A2 | grasmash/drupal-claude-skills | 24 | 5 skills (incl. OWASP security) | Git clone | ★★★★ From Acquia veteran, includes drupalatyourfingertips.com content |
| A3 | scottfalconer/drupal-contribute-fix | 15 | 1 skill (4 modes) | Git clone + Python | ★★★★ Unique — contribution workflow with API integration |
| A4 | gkastanis/drupal-workflow | 0 | 16 skills + 4 agents + 10 commands | Claude plugin | ★★★★ Most comprehensive single plugin, semantic docs |
| A5 | gxleano/drupal-agentic-workflow | 2 | 20 skills + 3 hooks | Setup script | ★★★★ Most skills, quality-gate hooks, phpcbf auto-fix |
| A6 | jamieaa64/Drupal-DDEV-Setup-Claude-Skill | 9 | 1 skill (DDEV setup) | Git clone | ★★★ From Jamie Abrahams (FreelyGive) |
| A7 | ablerz/claude-skill-drupal-module | - | 1 skill (13 refs) + DDEV commands | Composer | ★★★★ Best distribution pattern (Composer) |
| A8 | ronaldtebrake/drupal-coding-standards-skill | 6 | 1 skill (coding standards) | Git clone | ★★★ Focused, essential |
| A9 | zivtech/drupal-critic | 3 | 1 skill (code review) | Git clone | ★★★ Zivtech agency |
| A10 | drupal-canvas/skills | 1 | 7 skills (Canvas components) | npx skills add | ★★★ Official Canvas skills |
| A11 | oscarnovasf/claude-drupal-plugin | 0 | 3 plugins (global/backend/frontend) | Claude plugin marketplace | ★★★ Three-plugin architecture, Spanish |
| A12 | gkastanis/drupal-claude-code-sub-agent-collective | 0 | 15 agents + 15 skills + hooks | Manual | ★★★ Research/experimental, hub-and-spoke pattern |
| A13 | aldunchev/ai-fe-skills | 0 | Frontend skills (Drupal + AEM) | Git clone | ★★ Frontend-focused |
| A14 | droptica/drupal-agents-md | - | AGENTS.md template | curl + AI generation | ★★★★ Universal tool support, 5-min setup |

### Category B: DDEV AI Plugins

| # | Plugin | Description | Assessment |
|---|--------|-------------|------------|
| B1 | FreelyGive/ddev-claude-code | Claude Code in DDEV (official FreelyGive) | ★★★★ Primary recommendation |
| B2 | Drupal-AI/ddev-drupal-ai | Drupal AI module ecosystem dev env | ★★★ Official Drupal AI project |
| B3 | codingsasi/ddev-mcp | MCP server (Drush, Playwright, platform.sh) | ★★★★ Multi-purpose |
| B4 | AkibaAT/ddev-mcp | DDEV MCP Server | ★★★ Alternative MCP |
| B5 | tyler36/ddev-ollama | Local LLM via Ollama | ★★★ Stable |
| B6 | stinis87/ddev-ollama | Alternative Ollama | ★★ |
| B7 | e0ipso/ddev-assistant-claude | Claude assistant (from JSON:API maintainer) | ★★★ |
| B8 | e0ipso/ddev-playwright-cli | Playwright CLI in DDEV | ★★★ |
| B9 | lpeabody/ddev-ai | General AI addon | ★★ |
| B10 | tyler36/ddev-copilot | GitHub Copilot in DDEV | ★★ |
| B11 | jcandan/ddev-ai-agent | AI agent for DDEV | ★★ |
| B12 | credevator/ddev-litellm | LiteLLM proxy (multi-provider) | ★★ |
| B13 | agence-adeliom/ddev-claude-sandbox | Claude sandbox | ★★ |
| B14 | jamespublishlab/ddev-claude-code | Alt Claude Code DDEV | ★★ |
| B15 | lexsoft00/ddev-drupal-claude-code | Drupal-specific Claude DDEV | ★★ |
| B16 | Gonzalo2683/ddev-claudecode-native | Native Claude Code DDEV | ★★ |
| B17 | dragonwize/ddev-opencode | OpenCode in DDEV | ★ Niche |
| B18 | jfastnacht/ddev-mistral-vibe-cli | Mistral in DDEV | ★ Niche |

### Category C: MCP Servers

| # | Server | Description | Assessment |
|---|--------|-------------|------------|
| C1 | drupal.org/project/mcp_server | Turn Drupal into MCP server | ★★★★ Official contrib |
| C2 | drupal.org/project/mcp | Model Context Protocol module | ★★★★ |
| C3 | drupal.org/project/mcp_client | MCP client for Drupal | ★★★ |
| C4 | drupal.org/project/mcp_tools | MCP tooling | ★★★ |
| C5 | Cleversoft-IT/drupal-tools-mcp | Drupal.org + Drush via MCP | ★★★ |
| C6 | Cleversoft-IT/drupal-modules-mcp | Query drupal.org modules | ★★★ |
| C7 | Omedia/mcp-server-drupal | TS companion for MCP module | ★★★ |
| C8 | peximo/drupal-mcp-server | Drupal MCP implementation | ★★ |
| C9 | DrupalMCP.io | Dedicated MCP project | ★★★ Emerging |
| C10 | codingsasi/ddev-mcp | DDEV MCP bridge | ★★★★ |
| C11 | AkibaAT/ddev-mcp | DDEV MCP alternative | ★★★ |
| C12 | bloomidea/drush-mcp-bridge | Drush MCP on Packagist | ★★★ |
| C13 | @playwright/mcp | Browser automation (Microsoft) | ★★★★★ Production |
| C14 | lunetics/php-mcp-phpstan | PHPStan via MCP | ★★★ |
| C15 | larspohlmann/mcp-phpstan-server | Pure PHP PHPStan MCP | ★★★ |

### Category D: Drupal Modules (AI Framework)

**Core Framework:**
| Module | Installs/Maturity | Assessment |
|--------|------------------|------------|
| drupal/ai | Production, security patched | ★★★★★ ESSENTIAL — 48+ providers |
| drupal/ai_agents | Stable | ★★★★ ESSENTIAL — agentic framework |
| drupal/ai_agent_agent | Stable | ★★★ Meta-agent |
| drupal/ai_drush_agents | Stable | ★★★ CLI agents |

**Providers (select based on needs):**
| Module | Provider | Assessment |
|--------|----------|------------|
| ai_provider_openai | OpenAI/GPT | ★★★★ Most popular |
| ai_provider_anthropic | Claude | ★★★★ |
| ai_provider_ollama | Ollama (local) | ★★★★ Free, private |
| ai_provider_acquia | Acquia AI Gateway | ★★★★ For Acquia users |
| gemini_provider | Google Gemini | ★★★ |
| ai_provider_deepseek | DeepSeek | ★★ |
| ai_provider_google_vertex | Google Vertex | ★★ |

**Content & Editor:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_ckeditor | AI in CKEditor | ★★★★ |
| ai_ckeditor_extras | CKEditor extras | ★★★ |
| ckeditor_ai_agent | AI writing agent | ★★★ |
| ckeditor5_premium_features | Premium CKEditor AI | ★★★ (paid) |

**Migration:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_content_migrate | AI content migration | ★★★★ |
| ai_migration | Migration framework | ★★★ |
| ai_single_page_importer | Single page import | ★★★ (Mark Conroy) |
| ai_migrate | Migration helper | ★★ |
| ai_migrate_agent | Agent-based migration | ★★ |

**Search & Discovery:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_search | Semantic search | ★★★★ |
| aisearch | RAG search | ★★★ |
| semantic_search | Vector search | ★★★ |
| ai_related_content | Related content | ★★ |
| ai_search_block | Search block | ★★ |

**Translation:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_content_translation | Content translation | ★★★★ |
| ai_translate | Basic translation | ★★★ |
| ai_translate_plus | Enhanced translation | ★★★ |

**Chatbot & Conversational:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| aichatbot | Custom chatbot | ★★★ |
| chat_ai | Chat module | ★★ |
| ai_lead_chatbot | Lead gen chatbot | ★★ |
| knova | Knowledge chatbot | ★★ |
| smart_faq_chatbot | FAQ chatbot | ★★ |

**Workflow & Automation:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| flowdrop_agents | FlowDrop + AI Agents | ★★★★ Born from EC hackathon |
| flowdrop_ui_agents | Visual flow builder | ★★★ |
| ai_integration_eca | ECA + AI integration | ★★★★ 153 sites |
| eca | Event-Condition-Action base | ★★★★★ Essential workflow engine |

**Observability:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| langfuse | AI tracing & evaluation | ★★★★ Production monitoring |

**LLMs.txt:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| llms_txt | llms.txt standard | ★★★ |
| llms_txt_generator | Generate llms.txt | ★★★ |
| llms_txt_exporter | Export as llms.txt | ★★ |

**Code & Development:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_generation | AI code generation | ★★★ |
| claude_code | Claude Code integration | ★★★ |
| ai_claude_agent_sdk | Claude SDK (EXPERIMENTAL) | ★★ Forward-looking |
| gpt_code_reviewer | GPT code review | ★★★ |

**Upgrade & Maintenance:**
| Module | Purpose | Assessment |
|--------|---------|------------|
| ai_upgrade | AI-assisted upgrades | ★★ |
| ai_upgrade_assistant | Upgrade assistant | ★★ |
| rector | Automated code transformation | ★★★★ (not AI but essential) |
| upgrade_status | Deprecation checking | ★★★★ (not AI but essential) |

**Recipes:**
| Recipe | Purpose | Assessment |
|--------|---------|------------|
| Drupal CMS AI recipe | OOTB AI features | ★★★★★ Ships with Drupal CMS 2.0 |
| ai_chatbot_recipe | No-code RAG chatbot | ★★★ |
| Pronovix llms.txt recipe | llms.txt setup | ★★★ |

### Category E: IDE/Tool Configurations & Context Files

| # | Tool | Type | Platform Support | Assessment |
|---|------|------|-----------------|------------|
| E1 | cursor.directory/rules/drupal | Cursor rules | Cursor only | ★★★ Community directory |
| E2 | ivangrynenko/cursorrules | Cursor rules for PHP/Drupal | Cursor only | ★★★ Includes OWASP security |
| E3 | Drupal Copilot guides (various) | Blog posts | Copilot | ★★★ Scattered but useful |
| E4 | AGENTS.md template (Droptica) | Universal context | 10+ tools (Cursor, Copilot, Claude, Codex, Gemini, Aider, Roo, Zed, Devin) | ★★★★ Best cross-tool solution |
| E5 | amazeeio/drupal-agents-md | AGENTS.md template | Same as E4 | ★★★ Alternative from amazee.io |
| E6 | drupal.org/project/ai_context | Context Control Center (CCC) | Drupal-native | ★★★ Active sprint planning, March 2026 |

### Category F: External AI Tools & Repos

| # | Tool | Description | Assessment |
|---|------|-------------|------------|
| F1 | Acquia Nebula | Canvas Code Component scaffolding | ★★★★ Official Acquia template |
| F2 | LLPhant | PHP AI framework (LangChain-inspired) | ★★★ PHP 8.1+, active |
| F3 | ngxtm/devkit | 414+ skills unified system | ★★★ No Drupal skills yet |
| F4 | Omedia/drupal-skill | Drupal skill | ★★ Minimal info |
| F5 | nonzod/drupaldev-claude-skill | Claude skill for Drupal dev | ★★ |
| F6 | 0ldh/claude-code-agents-orchestra | Drupal developer agent in larger orchestra | ★★ Niche |
| F7 | alirezarezvani/claude-skills | 192+ skills (may include Drupal) | ★★ Large collection |
| F8 | drupal/surge | AI coding starter kit (Composer) | ★★★ Active dev, aggregates skills + AGENTS.md |
| F9 | drupal/ai_skills | 3 official Drupal agent skills | ★★★ agentskills.io validated |
| F10 | Bloomidea/drush-mcp | 17 tools via Drush MCP | ★★★ Local/SSH/Docker, multi-site |
| F11 | drupal/ai_commerce | AI for Drupal Commerce | ★★ Niche but valuable |
| F12 | drupal/ai_comment_moderation | AI content moderation | ★★ |
| F13 | Symfony AI | PHP AI framework components | ★★★★ Drupal building on this |
| F14 | drupalorg-cli 0.8.0 | `--format=llm` for AI agents | ★★★★ Essential for contribution skills |
| F15 | Yeachan-Heo/oh-my-claudecode | Multi-agent orchestration for Claude Code (32 agents, smart routing, Ralph/Ultrawork modes) — 10.1k stars | ★★★★ Not Drupal-specific but high utility for complex projects |

### Category G: Active Drupal.org Issues (Policy/Standards)

| # | Issue | Title | Status | Significance |
|---|-------|-------|--------|-------------|
| G1 | #3568936 | Add AGENTS.md to Drupal core | Closed (no merge) | Reporter reversed position; community alternatives exist |
| G2 | #3570498 | AI tools for contributors and maintainers | Active (by Dries) | Official policy discussion, rich debate |
| G3 | #3565489 | First-class support for agent-skills | Active | AI module supporting agentskills.io natively |
| G4 | #3541110 | AI coding starterkit | Active | Unified dev toolkit proposal (Surge is implementation) |
| G5 | #3558328 | Claude Skill for Drupal Brand Guidelines | Active | Brand standards in AI skill format |
| G6 | #3574093 | Ban LLM code contributions | Needs review | Contentious; middle-ground proposals emerging |

### Category H: Key Community Resources

| # | Resource | Type | Assessment |
|---|----------|------|------------|
| H1 | DrupalCon Chicago 2026 AI Summit | 21+ sessions, full-day summit | ★★★★★ Largest AI event in Drupal history |
| H2 | Context7 MCP (Drupal docs) | Documentation MCP | ★★★★ 1,989 Drupal snippets via d9book |
| H3 | amazee.ai whitepaper | Technical paper | ★★★★ Data-sovereign AI details |
| H4 | Dries: "Adaptable Modules" concept | Vision | ★★★ New paradigm for AI-era module sharing |
| H5 | 79.2% community using AI daily | Survey stat | Context for adoption strategy |

---

## Maturity Scale

| Rating | Meaning |
|--------|---------|
| ★★★★★ | Production-ready, widely adopted, actively maintained |
| ★★★★ | Stable, well-documented, recommended |
| ★★★ | Working, useful but may need refinement |
| ★★ | Early stage, experimental, or niche |
| ★ | Very early, limited utility |

---

## Key Recommendations

1. **Immediate:** Adopt the "Standard" list above as the baseline for the Drupal.org initiative page
2. **Short-term:** Package the Standard list as a single DDEV addon (`ddev get drupal/ai-dev-toolkit`)
3. **Medium-term:** Contribute to active drupal.org issues:
   - #3568936 (AGENTS.md in core)
   - #3565489 (first-class agent-skills in AI module)
   - #3541110 (AI coding starterkit)
4. **Long-term:** Establish Drupal.org initiative page for "Skills and AI Coding plugins"

## Platform Compatibility Summary

**Most portable (30+ tools):** SKILL.md (agentskills.io standard)
**Most universal context file (10+ tools):** AGENTS.md
**Tool-specific but valuable:** CLAUDE.md (Claude only), .cursorrules (Cursor only)
**Infrastructure-level (tool-agnostic):** DDEV addons, MCP servers, Drupal modules

**Recommendation:** Default to AGENTS.md + SKILL.md for maximum portability. Add CLAUDE.md and .cursorrules as secondary tool-specific enhancements.

## Research Completeness

This assessment synthesizes 22 research files totaling 4,100+ lines covering:
- 16+ GitHub repos analyzed with individual skill inventories (80+ skills)
- 18 DDEV plugins, 15 MCP servers, 65+ drupal.org modules
- 20+ blog posts, 15+ events, cross-CMS comparisons
- Platform compatibility matrix across 30+ AI tools
- Active drupal.org policy issues tracked
- Community discussion and concerns documented
