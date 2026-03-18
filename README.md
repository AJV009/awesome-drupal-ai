<div align="center">

<img src="https://raw.githubusercontent.com/sindresorhus/awesome/main/media/logo.svg" alt="Awesome" width="400">

<br>
<br>

# Awesome Drupal AI

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

*A curated list of AI tools, skills, plugins, modules, and resources for Drupal development and site building.*

**65+ modules · 15+ skill repos · 18+ DDEV plugins · 15+ MCP servers · 80+ skills**

</div>

<br>

## Contents

- [The Starter Pack](#the-starter-pack) - Recommended defaults to get started fast.
- [Agent Skills & Repos](#agent-skills--repos) - SKILL.md repos for AI coding tools.
- [DDEV Plugins](#ddev-plugins) - AI addons for DDEV local development.
- [MCP Servers](#mcp-servers) - Model Context Protocol servers for Drupal.
- [Drupal.org AI Modules](#drupalorg-ai-modules) - Contributed modules on drupal.org.
- [IDE & Editor Configurations](#ide--editor-configurations) - Cursor, Copilot, Kiro, CLAUDE.md configs.
- [CLI Tools & Frameworks](#cli-tools--frameworks) - Command-line tools and PHP AI frameworks.
- [Drupal Recipes for AI](#drupal-recipes-for-ai) - One-step AI setup via Drupal Recipes.
- [Community Resources](#community-resources) - Events, podcasts, training, blogs, key people.
- [Specifications & Standards](#specifications--standards) - agentskills.io, AGENTS.md, llms.txt.
- [Cross-CMS Patterns](#cross-cms-patterns) - How Laravel, Shopware, WordPress compare.

## The Starter Pack

The fastest path to AI-assisted Drupal development. All tested, all recommended. Install in order.

### Step 1: Environment (DDEV Addons)

```bash
# Claude Code inside your DDEV container
ddev get FreelyGive/ddev-claude-code

# Drupal AI module development environment
ddev get Drupal-AI/ddev-drupal-ai

# Local LLM via Ollama (free, private)
ddev get tyler36/ddev-ollama
```

### Step 2: Agent Skills

```bash
# Module development skill with 13 Drupal API reference docs (Composer)
composer require ablerz/claude-skill-drupal-module:dev-11.x

# Coding standards enforcement skill
git clone https://github.com/ronaldtebrake/drupal-coding-standards-skill \
  .claude/skills/drupal-coding-standards

# drupal.org contribution workflow skill
git clone https://github.com/scottfalconer/drupal-contribute-fix \
  .claude/skills/drupal-contribute-fix
```

### Step 3: Project Context File

```bash
# 5-minute setup: download template, paste prompt into AI, get customized AGENTS.md
curl -O https://raw.githubusercontent.com/droptica/drupal-agents-md/main/AGENTS-TEMPLATE.md
# Then copy the prompt from the README into your AI tool
```

Works with: Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin.

### Step 4: MCP Servers

```bash
# DDEV MCP bridge (Drush, Playwright, platform.sh)
ddev get codingsasi/ddev-mcp

# Browser automation for testing Drupal sites
npm install -g @playwright/mcp

# Query drupal.org modules + Drush commands via MCP
npm install -g drupal-tools-mcp  # Cleversoft-IT
```

### Step 5: Drupal Modules (Core AI Framework)

```bash
composer require drupal/ai           # Core framework, 48+ providers ★★★★★
composer require drupal/ai_agents    # Agentic framework ★★★★
composer require drupal/ai_provider_openai   # or anthropic, ollama, etc.
```

### Maturity Scale

| Rating | Meaning |
|--------|---------|
| ★★★★★ | Production-ready, widely adopted, actively maintained |
| ★★★★ | Stable, well-documented, recommended |
| ★★★ | Working, useful but may need refinement |
| ★★ | Early stage, experimental, or niche |
| ★ | Very early, limited utility |

---

## Agent Skills & Repos

Skills in [SKILL.md format](https://agentskills.io/specification) work across 30+ tools including Claude Code, Kiro, Cursor, VS Code Copilot, Gemini CLI, OpenHands, Roo Code, Aider, Junie, and Cline.

### Drupal-Specific Skill Repositories

- [madsnorgaard/drupal-agent-resources](https://github.com/madsnorgaard/drupal-agent-resources) (★ 32) — 5 skills, 1 agent, 5 commands; three-tier architecture; `agr` CLI install ★★★★
- [grasmash/drupal-claude-skills](https://github.com/grasmash/drupal-claude-skills) (★ 24) — 5 skills including OWASP security and drupalatyourfingertips.com content ★★★★
- [scottfalconer/drupal-contribute-fix](https://github.com/scottfalconer/drupal-contribute-fix) (★ 15) — Convert local fixes to drupal.org MR-ready contributions; 4 modes ★★★★
- [gkastanis/drupal-workflow](https://github.com/gkastanis/drupal-workflow) — 16 skills, 4 agents, 10 commands, quality-gate hooks; most comprehensive single plugin ★★★★
- [gxleano/drupal-agentic-workflow](https://github.com/gxleano/drupal-agentic-workflow) — 20 skills, 3 quality-gate hooks, post-generation auto-linting ★★★★
- [ablerz/claude-skill-drupal-module](https://github.com/ablerz/claude-skill-drupal-module) — Module dev skill bundling 13 API reference docs; Composer-installable ★★★★
- [jamieaa64/Drupal-DDEV-Setup-Claude-Skill](https://github.com/jamieaa64/Drupal-DDEV-Setup-Claude-Skill) (★ 9) — Automates new/existing Drupal project setup via DDEV ★★★
- [ronaldtebrake/drupal-coding-standards-skill](https://github.com/ronaldtebrake/drupal-coding-standards-skill) (★ 6) — Coding standards enforcement via AI ★★★
- [zivtech/drupal-critic](https://github.com/zivtech/drupal-critic) (★ 3) — Drupal-specific code review skill from Zivtech agency ★★★
- [drupal-canvas/skills](https://github.com/drupal-canvas/skills) (★ 1) — 7 skills for developing Drupal Canvas Code Components; `npx skills add drupal-canvas/skills` ★★★
- [oscarnovasf/claude-drupal-plugin](https://github.com/oscarnovasf/claude-drupal-plugin) — Three-plugin system (global/backend/frontend); Spanish-language; TypeScript ★★★
- [gkastanis/drupal-claude-code-sub-agent-collective](https://github.com/gkastanis/drupal-claude-code-sub-agent-collective) — 15 specialized agents, hub-and-spoke research architecture ★★★
- [aldunchev/ai-fe-skills](https://github.com/aldunchev/ai-fe-skills) — Frontend skills for Drupal and AEM; cross-compatible SKILL.md format ★★
- [Omedia/drupal-skill](https://github.com/Omedia/drupal-skill) — 3 skills (frontend, backend, tooling) with references and assets ★★
- [nonzod/drupaldev-claude-skill](https://github.com/nonzod/drupaldev-claude-skill) — Coding standards organized by language (PHP, Twig, CSS, JS, YAML, SQL) ★★
- [droptica/drupal-agents-md](https://github.com/droptica/drupal-agents-md) — AGENTS.md template for Drupal projects; 10+ tool support; 5-min setup ★★★★

### Context Files

- [amazeeio/drupal-agents-md](https://github.com/amazeeio/drupal-agents-md) — AGENTS.md template from amazee.io; DDEV and vanilla variants ★★★

### Drupal.org Skill Modules

- [drupal/ai_skills](https://www.drupal.org/project/ai_skills) — 3 official agentskills.io-validated skills: coding-standards, issue-queue, contribute-fix ★★★
- [drupal/surge](https://www.drupal.org/project/surge) — Aggregates agent skills; generates AGENTS.md; multi-tool coding standards (`composer surge-standards`) ★★★
- [drupal/claude_skill_drupal_ddev_site_setup](https://www.drupal.org/project/claude_skill_drupal_ddev_site_setup) — Drupal and DDEV site setup skill on drupal.org ★★★

### Skill Installation Methods Summary

| Method | Command example |
|--------|----------------|
| Composer | `composer require ablerz/claude-skill-drupal-module` |
| `agr` CLI | `agr add madsnorgaard/drupal-agent-resources/drupal-expert` |
| `npx skills add` | `npx skills add drupal-canvas/skills` |
| Claude plugin marketplace | `claude plugin marketplace add https://github.com/user/repo.git` |
| Git clone | `git clone <repo> .claude/skills/<name>` |
| Setup script | `~/drupal-agentic-workflow/bin/setup.sh .` |

---

## DDEV Plugins

### Recommended (Official Registry — addons.ddev.com)

- [FreelyGive/ddev-claude-code](https://github.com/FreelyGive/ddev-claude-code) — Claude Code inside DDEV web container; `ddev get FreelyGive/ddev-claude-code` ★★★★
- [tyler36/ddev-ollama](https://github.com/tyler36/ddev-ollama) — Local LLM via Ollama; `ddev get tyler36/ddev-ollama` ★★★
- [lpeabody/ddev-ai](https://addons.ddev.com/addons/lpeabody/ddev-ai) — General AI addon for DDEV ★★

### Drupal AI Module Development

- [Drupal-AI/ddev-drupal-ai](https://github.com/Drupal-AI/ddev-drupal-ai) — Official Drupal AI module development environment; recipe integration planned ★★★

### MCP Bridges for DDEV

- [codingsasi/ddev-mcp](https://github.com/codingsasi/ddev-mcp) — MCP server with Drush, Playwright, platform.sh tools; also on npm ★★★★
- [AkibaAT/ddev-mcp](https://github.com/AkibaAT/ddev-mcp) — DDEV MCP server; listed on LobeHub, mcpservers.org, playbooks.com ★★★

### Claude Code Variants

- [e0ipso/ddev-assistant-claude](https://github.com/e0ipso/ddev-assistant-claude) — Claude assistant from JSON:API maintainer Mateu Aguiló Bosch ★★★
- [jamespublishlab/ddev-claude-code](https://github.com/jamespublishlab/ddev-claude-code) — Alternative Claude Code DDEV integration ★★
- [lexsoft00/ddev-drupal-claude-code](https://github.com/lexsoft00/ddev-drupal-claude-code) — Drupal-specific Claude Code DDEV integration ★★
- [Gonzalo2683/ddev-claudecode-native](https://github.com/Gonzalo2683/ddev-claudecode-native) — Native Claude Code DDEV integration ★★
- [agence-adeliom/ddev-claude-sandbox](https://github.com/agence-adeliom/ddev-claude-sandbox) — Sandboxed Claude environment for DDEV ★★

### Other AI Tools in DDEV

- [tyler36/ddev-copilot](https://github.com/tyler36/ddev-copilot) — GitHub Copilot integration for DDEV ★★
- [e0ipso/ddev-playwright-cli](https://github.com/e0ipso/ddev-playwright-cli) — Playwright CLI for browser automation in DDEV ★★★
- [credevator/ddev-litellm](https://github.com/credevator/ddev-litellm) — LiteLLM proxy for multi-provider LLM access in DDEV ★★
- [jcandan/ddev-ai-agent](https://github.com/jcandan/ddev-ai-agent) — AI agent for DDEV ★★
- [dragonwize/ddev-opencode](https://github.com/dragonwize/ddev-opencode) — OpenCode (open-source AI CLI) in DDEV ★
- [jfastnacht/ddev-mistral-vibe-cli](https://github.com/jfastnacht/ddev-mistral-vibe-cli) — Mistral vibe CLI for DDEV ★
- [stinis87/ddev-ollama](https://addons.ddev.com/addons/stinis87/ddev-ollama) — Alternative Ollama DDEV integration ★★

---

## MCP Servers

### Drupal-Native MCP (drupal.org)

- [drupal/mcp_server](https://www.drupal.org/project/mcp_server) — Turns your Drupal site into an MCP server for Claude, Cursor, and other tools ★★★★
- [drupal/mcp](https://www.drupal.org/project/mcp) — Model Context Protocol module; STDIO transport ★★★★
- [drupal/mcp_client](https://www.drupal.org/project/mcp_client) — MCP client; allows Drupal to consume external MCP servers ★★★
- [drupal/mcp_tools](https://www.drupal.org/project/mcp_tools) — Additional MCP tooling for Drupal ★★★

### External MCP Servers for Drupal

- [DrupalMCP.io](https://drupalmcp.io/) — Dedicated MCP implementation project for Drupal; setup guides and roadmap ★★★
- [Omedia/mcp-server-drupal](https://github.com/Omedia/mcp-server-drupal) — TypeScript companion MCP server for the Drupal MCP module; STDIO transport ★★★
- [Cleversoft-IT/drupal-tools-mcp](https://github.com/Cleversoft-IT/drupal-tools-mcp) — Query drupal.org modules AND run Drush commands via MCP; works with Cline ★★★
- [Cleversoft-IT/drupal-modules-mcp](https://github.com/Cleversoft-IT/drupal-modules-mcp) — Query drupal.org module information from AI tools ★★★
- [bloomidea/drush-mcp-bridge](https://packagist.org/packages/bloomidea/drush-mcp-bridge) — 17 Drush tools via MCP; local/SSH/Docker transports; multi-site support ★★★
- [peximo/drupal-mcp-server](https://github.com/peximo/drupal-mcp-server) — Drupal MCP server implementation ★★

### DDEV MCP Servers

- [codingsasi/ddev-mcp](https://github.com/codingsasi/ddev-mcp) — MCP server with platform.sh, Playwright, Drush, wp-cli; also on npm ★★★★
- [AkibaAT/ddev-mcp](https://github.com/AkibaAT/ddev-mcp) — DDEV MCP Server; listed across MCP directories ★★★

### Browser Automation

- [@playwright/mcp](https://github.com/microsoft/playwright-mcp) — Microsoft-maintained browser automation MCP; essential for testing Drupal sites ★★★★★

### PHP Code Quality MCPs

- [lunetics/php-mcp-phpstan](https://github.com/lunetics/php-mcp-phpstan) — PHPStan static analysis via MCP for AI tools ★★★
- [larspohlmann/mcp-phpstan-server](https://github.com/larspohlmann/mcp-phpstan-server) — Minimal pure-PHP PHPStan MCP; zero dependencies ★★★

### Documentation MCPs

- [Context7 MCP](https://context7.com/) — Version-specific Drupal API docs; 1,989 Drupal snippets via d9book (`/selwynpolit/d9book`); used by multiple Drupal skill repos ★★★★

### General Utility MCPs

- [bytebase/dbhub](https://github.com/bytebase/dbhub) — Database MCP hub for MySQL, PostgreSQL; useful for Drupal DB interactions ★★★
- [AWS OpenAPI MCP Server](https://awslabs.github.io/mcp/servers/openapi-mcp-server) — OpenAPI spec MCP; useful for API-first Drupal development ★★

### PHP MCP SDK

- [Official PHP MCP SDK](http://blog.modelcontextprotocol.io/posts/2025-09-05-php-sdk/) — Build native MCP servers in PHP; directly applicable to Drupal ★★★★

---

## Drupal.org AI Modules

### Core Framework

- [drupal/ai](https://www.drupal.org/project/ai) (13,293 installs) — Core AI framework; abstraction layer for 48+ providers; AI Automators, CKEditor, ECA submodules included ★★★★★
- [drupal/ai_agents](https://www.drupal.org/project/ai_agents) — Agentic framework; Field Type, Content Type, and Taxonomy agents built-in; no-code agent creation ★★★★
- [drupal/ai_agent_agent](https://www.drupal.org/project/ai_agent_agent) — Meta-agent that orchestrates other agents ★★★
- [drupal/ai_drush_agents](https://www.drupal.org/project/ai_drush_agents) — AI agents accessible via Drush CLI ★★★
- [drupal/ai_agent_migration](https://www.drupal.org/project/ai_agent_migration) — AI-powered migration agent ★★★
- [drupal/ai_context](https://www.drupal.org/project/ai_context) — Context Control Center (CCC); centralized AI context management; active sprint development ★★★

### Providers

Full list of 48+ providers: [new.drupal.org/ai/about-drupal-ai/providers](https://new.drupal.org/ai/about-drupal-ai/providers)

- [drupal/ai_provider_openai](https://www.drupal.org/project/ai_provider_openai) — OpenAI / GPT integration ★★★★
- [drupal/ai_provider_anthropic](https://www.drupal.org/project/ai_provider_anthropic) — Anthropic / Claude integration ★★★★
- [drupal/ai_provider_ollama](https://www.drupal.org/project/ai_provider_ollama) — Local LLM via Ollama; free, private ★★★★
- [drupal/ai_provider_acquia](https://www.drupal.org/project/ai_provider_acquia) — Acquia secure AI gateway; pre-configured ★★★★
- [drupal/gemini_provider](https://www.drupal.org/project/gemini_provider) — Google Gemini integration ★★★
- [drupal/ai_provider_google_vertex](https://www.drupal.org/project/ai_provider_google_vertex) — Google Vertex AI ★★★
- [drupal/ai_provider_deepseek](https://www.drupal.org/project/ai_provider_deepseek) — DeepSeek integration ★★

Additional providers available via the AI module: AWS Bedrock, Azure OpenAI, Hugging Face, Mistral, amazee.ai, LiteLLM, OpenRouter, Groq, and 35+ more.

### Content & Editor

- [drupal/ai_ckeditor](https://www.drupal.org/project/ai_ckeditor) — AI-powered content assistance in CKEditor ★★★★
- [drupal/ai_ckeditor_extras](https://www.drupal.org/project/ai_ckeditor_extras) — Additional AI features for CKEditor ★★★
- [drupal/ckeditor_ai_agent](https://www.drupal.org/project/ckeditor_ai_agent) — AI writing agent for CKEditor ★★★
- [drupal/ckeditor5_premium_features](https://www.drupal.org/project/ckeditor5_premium_features) (13,180 installs) — Premium CKEditor including AI assistant (paid CKSource features) ★★★
- [drupal/ai_generation](https://www.drupal.org/project/ai_generation) — AI-powered Drupal code generation ★★★

### Migration & Import

- [drupal/ai_content_migrate](https://www.drupal.org/project/ai_content_migrate) — AI-assisted large-scale content migration ★★★★
- [drupal/ai_migration](https://www.drupal.org/project/ai_migration) — Full AI migration framework with docs ★★★
- [drupal/ai_single_page_importer](https://www.drupal.org/project/ai_single_page_importer) — Fast, flexible single-page content imports by Mark Conroy ★★★
- [drupal/ai_migrate](https://www.drupal.org/project/ai_migrate) — AI content migration helper ★★
- [drupal/ai_migrate_agent](https://www.drupal.org/project/ai_migrate_agent) — Agent-based content migration ★★

### Search & RAG

- [drupal/ai_search](https://www.drupal.org/project/ai_search) (51 installs) — Semantic search with AI; vector embeddings via Search API ★★★★
- [drupal/aisearch](https://www.drupal.org/project/aisearch) — RAG-based AI search ★★★
- [drupal/semantic_search](https://www.drupal.org/project/semantic_search) — AI-vectored semantic search ★★★
- [drupal/ai_related_content](https://www.drupal.org/project/ai_related_content) — AI-powered related content suggestions ★★
- [drupal/ai_search_block](https://www.drupal.org/project/ai_search_block) — AI-powered search block ★★
- [drupal/openai_search](https://www.drupal.org/project/openai_search) — OpenAI-powered search ★★
- [drupal/ai_vdb_provider_milvus](https://www.drupal.org/project/ai_vdb_provider_milvus) — Milvus vector database provider ★★

### Translation

- [drupal/ai_content_translation](https://www.drupal.org/project/ai_content_translation) — AI-powered content translation ★★★★
- [drupal/ai_translate](https://www.drupal.org/project/ai_translate) (237 installs) — AI translation module ★★★
- [drupal/ai_translate_plus](https://www.drupal.org/project/ai_translate_plus) — Enhanced AI translation ★★★

### Chatbots & Assistants

- [drupal/aichatbot](https://www.drupal.org/project/aichatbot) — Custom AI chatbot with RAG for Drupal 9/10/11 ★★★
- [drupal/chat_ai](https://www.drupal.org/project/chat_ai) — Chat AI module ★★
- [drupal/ai_lead_chatbot](https://www.drupal.org/project/ai_lead_chatbot) — AI-powered lead generation chatbot ★★
- [drupal/knova](https://www.drupal.org/project/knova) — Knowledge-based AI chatbot ★★
- [drupal/smart_faq_chatbot](https://www.drupal.org/project/smart_faq_chatbot) — FAQ-oriented AI chatbot ★★

### Automation & Workflow (ECA, Agents)

- [drupal/eca](https://www.drupal.org/project/eca) — Event-Condition-Action framework; foundation for AI automation; BPMN.iO visual modeller ★★★★★
- [drupal/flowdrop_agents](https://www.drupal.org/project/flowdrop_agents) — Bridges AI Agents with FlowDrop workflows; born at EC Play to Impact hackathon 2026 ★★★★
- [drupal/flowdrop_ui_agents](https://www.drupal.org/project/flowdrop_ui_agents) — Visual flow builder for AI agents ★★★
- [drupal/ai_integration_eca](https://www.drupal.org/project/ai_integration_eca) (153 installs) — AI capabilities as actions within ECA models ★★★★
- [drupal/ai_commerce](https://www.drupal.org/project/ai_commerce) — AI for Drupal Commerce ★★
- [drupal/ai_comment_moderation](https://www.drupal.org/project/ai_comment_moderation) — AI-powered comment moderation ★★

### MCP Modules

- [drupal/mcp_server](https://www.drupal.org/project/mcp_server) — Turn Drupal into MCP server for Claude, Cursor, and other AI tools ★★★★
- [drupal/mcp](https://www.drupal.org/project/mcp) — Model Context Protocol module; STDIO transport ★★★★
- [drupal/mcp_client](https://www.drupal.org/project/mcp_client) — MCP client for consuming external MCP servers ★★★
- [drupal/mcp_tools](https://www.drupal.org/project/mcp_tools) — Additional MCP tooling ★★★
- [drupal/figma_canvas_ai](https://www.drupal.org/project/figma_canvas_ai) — Convert Figma designs to Drupal Canvas components via MCP ★★★

### LLMs.txt & AI Discoverability

- [drupal/llms_txt](https://www.drupal.org/project/llms_txt) — Provides `/llms.txt` endpoint for AI discoverability ★★★
- [drupal/llms_txt_generator](https://www.drupal.org/project/llms_txt_generator) — Generate llms.txt files for your Drupal site ★★★
- [drupal/llms_txt_exporter](https://www.drupal.org/project/llms_txt_exporter) — Export content as llms.txt ★★
- [drupal/llms_txt_ai](https://www.drupal.org/project/llms_txt_ai) — AI-generated llms.txt files ★★

### Testing & Code Quality

- [drupal/ai_testing](https://www.drupal.org/project/ai_testing) — AI-assisted testing module for Drupal ★★★
- [drupal/ai_agents_test](https://www.drupal.org/project/ai_agents_test) — QA testing framework for AI agents; runs known prompts for consistency ★★★
- [drupal/gpt_code_reviewer](https://www.drupal.org/project/gpt_code_reviewer) — OpenAI-powered automated code review ★★★
- [drupal/reviewer](https://www.drupal.org/project/reviewer) — Code review module for Drupal ★★
- [drupal/automated_testing_kit](https://www.drupal.org/project/automated_testing_kit) — Comprehensive testing kit ★★★

### Observability

- [drupal/langfuse](https://www.drupal.org/project/langfuse) — AI agent observability, tracing, cost tracking, and evaluation for production ★★★★

### Upgrade & Maintenance

- [drupal/ai_upgrade](https://www.drupal.org/project/ai_upgrade) — AI-assisted Drupal version upgrades ★★
- [drupal/ai_upgrade_assistant](https://www.drupal.org/project/ai_upgrade_assistant) — AI upgrade assistant ★★
- [drupal/rector](https://www.drupal.org/project/rector) — Automated code transformation (not AI but essential for upgrade workflows) ★★★★
- [drupal/upgrade_status](https://www.drupal.org/project/upgrade_status) — Deprecation checking (not AI but essential) ★★★★

### Accessibility

- [editoria11y](https://www.drupal.org/project/editoria11y) (21,155 installs) — Real-time a11y checker with "Fix with AI" button ★★★★★
- [drupal/ai_image_alt_text](https://www.drupal.org/project/ai) (7,231 installs) — AI-generated alt text via vision models (submodule of drupal/ai) ★★★★
- [drupal/ai_accessibility](https://www.drupal.org/project/ai_accessibility) — axe-core scanning with AI suggestions (MVP) ★★

### Other & Experimental

- [drupal/claude_code](https://www.drupal.org/project/claude_code) — Claude Code integration; provides scaffolded CLAUDE.md with Drupal best practices ★★★
- [drupal/ai_claude_agent_sdk](https://www.drupal.org/project/ai_claude_agent_sdk) — EXPERIMENTAL: Claude Code runtime integration with Drupal ★★
- [drupal/augmentor](https://www.drupal.org/project/augmentor) — AI augmentation pipeline module ★★
- [drupal/aia](https://www.drupal.org/project/aia) — AI Architect; generates content types and fields from natural language ★★
- [drupal/aidev](https://www.drupal.org/project/aidev) — AI developer assistant module ★★
- [drupal/openai](https://www.drupal.org/project/openai) — Original OpenAI integration (predates the AI framework; largely superseded) ★★
- [drupal/saplings_ai_agents](https://www.drupal.org/project/saplings_ai_agents) — AI agents by Saplings ★★
- [drupal/skills](https://www.drupal.org/project/skills) — Skills module on drupal.org ★★
- [drupal/skilling](https://www.drupal.org/project/skilling) — Skilling module on drupal.org ★★

---

## IDE & Editor Configurations

### Cursor Rules for Drupal

- [cursor.directory/rules/drupal](https://cursor.directory/rules/drupal) — Community-maintained Drupal rules directory for Cursor IDE ★★★
- [ivangrynenko/cursorrules](https://github.com/ivangrynenko/cursorrules) — Drupal-specific Cursor rules including OWASP Top 10 security patterns ★★★
- [cursorrules.org Drupal 11 guide](https://cursorrules.org/article/drupal-11-cursorrules-prompt-file) — Drupal 11 development rules for Cursor ★★★
- [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules) — Curated collection of .cursorrules files; may contain Drupal examples ★★

### CLAUDE.md Templates

- [drupal/claude_code](https://www.drupal.org/project/claude_code) — Drupal module providing scaffolded CLAUDE.md with Drupal coding conventions ★★★
- `CLAUDE.md` in your project root — standard practice; see [Tag1 workflow](https://www.tag1.com/blog/moving-10-year-old-drupal-issue-forward-with-ai/) for what to include ★★★

### AGENTS.md Templates (Universal — 10+ tool support)

- [droptica/drupal-agents-md](https://github.com/droptica/drupal-agents-md) — AGENTS.md template with Drupal sections: infrastructure, architecture, workflow, security ★★★★
- [amazeeio/drupal-agents-md](https://github.com/amazeeio/drupal-agents-md) — Alternative AGENTS.md template from amazee.io; DDEV and vanilla variants ★★★

### GitHub Copilot for Drupal

- [copilot-instructions.md spec](https://copilot-instructions.md/) — Official spec for Copilot custom instructions files ★★★
- [github/awesome-copilot](https://github.com/github/awesome-copilot) — Curated Copilot resources ★★

### Kiro IDE (Amazon)

- [kiro.dev/docs/skills/](https://kiro.dev/docs/skills/) — Kiro uses identical SKILL.md format as Claude Code; all Drupal SKILL.md files work in Kiro ★★★

### Acquia Nebula (Canvas Scaffolding)

- [acquia/nebula](https://github.com/acquia/nebula) — Template for scaffolding Drupal Canvas Code Components; `npx @drupal-canvas/create@latest`; includes agent skills in `.agents/skills/` ★★★★

### Context Control Center (Drupal-Native Context)

- [drupal/ai_context](https://www.drupal.org/project/ai_context) — Centralized context management within Drupal itself; active sprint development March 2026 ★★★

---

## CLI Tools & Frameworks

### Drupal-Specific CLI Tools

- [drupalorg-cli 0.8.0](https://mglaman.dev) — `--format=llm` flag formats issue/MR output for AI agent consumption; essential for contribution skills ★★★★
- [drupal/surge](https://www.drupal.org/project/surge) — Aggregates agent skills; compiles AGENTS.md; `composer surge-standards` and `composer surge-scan` ★★★

### Claude Code Configuration & Orchestration

- [bguidolim/managed-claude-stack (MCS)](https://github.com/bguidolim/mcs) (★ 65) — Config engine for Claude Code; shareable "tech packs" bundle MCP servers, plugins, hooks, skills, commands; convergence sync, drift detection, lockfiles; `brew install bguidolim/tap/managed-claude-stack` ★★★★
- [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) (★ 10,100+) — Multi-agent orchestration for Claude Code; 32 agents; Ralph/Autopilot/Ultrawork modes; smart model routing; 30-50% token savings ★★★★
- [ngxtm/devkit](https://github.com/ngxtm/devkit) — 414+ skills, 38 agents, 57 commands; multi-tool (Claude, Cursor, Copilot, Gemini); smart tech detection; no Drupal skills yet ★★★

### PHP AI Frameworks

- [LLPhant](https://github.com/LLPhant/LLPhant) — Comprehensive PHP AI framework inspired by LangChain; PHP 8.1+; works with Symfony/Drupal ★★★
- [Symfony AI](https://symfony.com/doc/current/ai.html) — AI components built on Symfony (Platform, Agent, Chat, Store, Mate, MCP Bundle); Drupal is building on this ★★★★
- [Neuron AI](https://www.neuron-ai.dev/) — Production-ready PHP agent framework; RAG, multi-agent, human-in-the-loop; no official Drupal module yet ★★★

### Acquia Platform Tools

- [Acquia Nebula](https://github.com/acquia/nebula) — Canvas Code Component scaffolding template; `npx @drupal-canvas/create@latest` ★★★★
- [Acquia Source](https://www.acquia.com/products/acquia-source) — Drupal SaaS with three AI agents: Site Builder Agent, AI Writing Assistant, Web Governance Agent ★★★

### Code Review & CI/CD Tools

- [drupal-rector](https://github.com/palantirnet/drupal-rector) — Automated upgrade of deprecated Drupal code via Rector ★★★★
- [mglaman/drupal-check](https://github.com/mglaman/drupal-check) — Check Drupal code for deprecations and bugs via static analysis ★★★★
- [hussainweb/drupal-code-quality](https://github.com/hussainweb/drupal-code-quality) — Docker image with all Drupal QA tools (PHPCS, PHPStan, PHPUnit) ★★★
- [Lullabot/drupal9ci](https://github.com/Lullabot/drupal9ci) — GitHub Actions CI for Drupal ★★★

### AI Pair Coding Best Practices

See [Dries' Claude Code meets Drupal](https://dri.es/claude-code-meets-drupal) — 30-min demo; no IDE touch; custom Drush command, refactoring, annotation-to-attribute conversion.

---

## Drupal Recipes for AI

Drupal Recipes distribute modules + configuration + permissions in one step. See the [Recipes docs](https://www.drupal.org/docs/extending-drupal/drupal-recipes) and [browse all recipes](https://new.drupal.org/browse/recipes).

- **Drupal CMS AI Recipe** — Ships with Drupal CMS 2.0; installs AI Core, AI Agents, AI Dashboard, AI Image Alt Text, Anthropic Provider, OpenAI Provider, Canvas; requires OpenAI or Anthropic API key ★★★★★
- [drupal/ai_chatbot_recipe](https://www.drupal.org/project/ai_chatbot_recipe) — No-code RAG chatbot with Key module; `drush recipe ../recipes/ai-chatbot-recipe`; requires OpenAI + Pinecone ★★★
- [drupal/ai_recipe_llm_optimized_content](https://packagist.org/packages/drupal/ai_recipe_llm_optimized_content) — LLM-optimized content structure recipe ★★
- [Pronovix llms.txt Recipe](https://www.thedroptimes.com/49424/pronovix-releases-drupal-recipe-llmstxt-support-ai-ready-content) — Recipe for implementing llms.txt; makes developer portals AI-agent-ready ★★★

---

## Community Resources

### Events & Conferences

- [DrupalCon Chicago 2026](https://events.drupal.org/chicago2026) — Mar 23-26; 21+ AI sessions; full-day AI Summit Monday; largest AI focus in DrupalCon history ★★★★★
- [Drupal AI Summit NYC 2026](https://new.drupal.org/ai/events/Drupal-AI-Summit-New-York-City) — May 14, 360 Madison Ave; early bird $150 ★★★★
- [Drupal Developer Days Athens 2026](https://devdays2026.drupal.org.gr/) — Apr 22-25; AI in programme ★★★
- [DrupalCon Rotterdam 2026](https://events.drupal.org/rotterdam2026) — Sep 28-Oct 1 ★★★
- [DrupalCon Vienna 2025](https://events.drupal.org/vienna2025) — 20+ AI sessions; standing room only; Canvas AI Assistant featured; recordings available ★★★★
- [DrupalCon Atlanta 2025](https://events.drupal.org/atlanta2025) — AI Automators powering Drupal CMS 1.0 launch ★★★★
- [DrupalCamp NJ 2026](https://www.drupalcampnj.org/) — Mar 12-13; two full-day AI trainings; 20 sessions ★★★
- [Play to Impact Hackathon 2026](https://www.drupal.org/about/starshot/initiatives/ai) — EC-organized; Jan 27-28, Brussels; 70+ participants; FlowDrop Agents module born here ★★★★
- [Drupal Dev Days 2026](https://www.thedroptimes.com/66857/drupal-dev-days-2026-programme-trends) — AI, Drupal CMS Evolution, Developer Tooling ★★★
- [Drupaladas #11 — AI Translation](https://www.drupal.org/community/events) — Mar 27 online (Spain); AI automation for Drupal translation workflows ★★★
- [MidCamp 2026 Hackathon](https://www.drupal.org/community) — Active planning ★★★
- [Drupal Switzerland AI Hackathon](https://www.drupal.org/community) — Organizing ★★

### Podcasts

- [Talking Drupal #542](https://talkingdrupal.com/542) — "Another AI Show"; Scott Falconer; good/bad of AI, Field Widget Actions
- [Talking Drupal #540](https://talkingdrupal.com/540) — Acquia Source; Matthew Grasmick; AI Single Page Importer
- [Talking Drupal #538](https://talkingdrupal.com/538) — "Agentic Development Workflows"; Andy Giles & Matt Glaman; Canvas CLI
- [Talking Drupal #537](https://talkingdrupal.com/537) — Orchestration; Jürgen Haas; automation and orchestration
- [Talking Drupal #530](https://talkingdrupal.com/530) — Community Working Group; Matthew Saunders; AI accessibility
- [Talking Drupal #515](https://talkingdrupal.com/515) — amazee.ai; Michael Schmid; privacy-focused AI, vector DBs, MCP, ECA
- [Talking Drupal #485](https://talkingdrupal.com/485) — AI Autonomy; Jay Callicott; future of AI in Drupal
- [Talking Drupal #455](https://talkingdrupal.com/455) — Top 5 Uses of AI for Drupal; Mike Miles
- [TD Cafe #015](https://talkingdrupal.com/td-cafe-015) — Non-Profit Summit at DrupalCon; AI for nonprofits

### Training & Courses

- [EC Webinar Series — "Bringing Drupal AI into your DNA"](https://www.drupal.org/about/starshot/initiatives/ai/webinars) — 5-part series by FreelyGive, EC, Dropsolid; **free**; YouTube recordings available
- [Dropsolid Drupal AI Academy](https://dropsolid.ai/drupal-ai-training) — 4 courses EUR 299-499; Certified Drupal AI Practitioner (DDAP) certification ★★★★
- [DrupalEasy "Responsible Drupal AI Basics"](https://www.drupaleasy.com/) — Full-day workshop by Mike Anello; covers AI Automators, Field Widget Actions, AI Agents ★★★
- [Drupalize.Me Drupal AI Guide](https://drupalize.me/blog/drupal-ai-how-set-it-and-try-it-out) — "How to Set It Up and Try It Out" ★★★
- [DrupalForge AI Templates](https://www.drupalforge.org/blog/learn-drupal-ai-free-templates-guide) — Free, no-install environments for Canvas AI, CMS AI, Automators, Testing ★★★★
- [DrupalForge Live Demos](https://www.drupalforge.org/blog/try-drupal-cms-ai-online-2026-ultimate-guide-no-install-live-demos) — Try Drupal CMS AI in 2026; no install required ★★★
- [amazee.ai Interactive Demos](https://new.drupal.org/ai/demos) — 7-day free trial; Content Categorization, CKEditor AI, AI Search, Advanced Skills ★★★
- [Anthropic MCP Advanced Topics](https://anthropic.skilljar.com/model-context-protocol-advanced-topics) — MCP course from Anthropic; directly applicable to Drupal MCP implementations ★★★
- [Opensense Labs 6-Part AI Series](https://opensenselabs.com/blog/drupal-ai-series/ai-module-setup-and-ckeditor) — AI module setup through ECA integration ★★★
- [QED42 Drupal AI Guides](https://www.qed42.com/insights/ai-in-drupal-a-focused-guide-to-practical-implementation) — Practical guides for agents, CKEditor, search, Canvas AI ★★★

### Blog Posts & Articles

**Workflows & Setup**
- [Tag1: AI on a 10-Year-Old Drupal Core Issue](https://www.tag1.com/blog/moving-10-year-old-drupal-issue-forward-with-ai/) — Plan-driven development; DDEV + Claude Code; core contribution workflow
- [Ronald te Brake: AI Coding Starter Kit for Drupal](https://www.ronaldtebrake.nl/blog/embracing-ai-coding-starter-kit-drupal/) — Inspired by Laravel Boost; proposes unified approach; drupal.org issue #3541110
- [Droptica: AGENTS.md for Drupal](https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/) — 5-min setup; 10+ tool support; onboarding "several times faster"
- [Jacob Rockowitz: Coding Drupal with AI](https://www.jrockowitz.com/blog/coding-drupal-with-ai) — AI as mentoring tool; plan-first approach; iterative Markdown requirements
- [Robert Menetray: OpenCode + DDEV 16-Agent Setup](https://menetray.com/en/blog/opencode-ddev-how-i-built-drupal-development-environment-16-ai-agents) — Most comprehensive multi-agent Drupal dev setup; three-container architecture; Ralph Loop automation

**Code Review & Quality**
- [Bálint Pekker: AI Code Review for Drupal](https://bpekker.dev/ai-code-review/) — Claude for automated Drupal code review; beyond static analysis
- [Bounteous: Automating Drupal Code Review with LLMs](https://www.bounteous.com/insights/2025/07/07/automating-drupal-code-refactoring-and-reviews-llms/) — LLM review in CI/CD pipelines; hybrid human + AI approach
- [Lullabot: Automated Code Review Tools](https://www.lullabot.com/articles/how-automated-code-review-tools-reduce-pull-request-bottlenecks) — Tested CodeRabbit, Codacy, Copilot, Gemini; Gemini Code Assist won

**Agentic Architecture**
- [QED42: Inside Drupal Canvas AI](https://www.qed42.com/insights/inside-drupal-canvas-ai-how-agents-turn-prompts-into-pages) — Deep dive into Canvas AI three-agent architecture
- [QED42: HAAT — Human-As-A-Tool](https://www.qed42.com/insights/haat-deep-dive-turning-human-intervention-into-a-scalable-primitive) — Repositioning humans as async dependencies in agent execution graphs
- [Acquia: Vibes on Rails](https://www.acquia.com/blog/vibes-rails) — System-in-the-loop governance; agent vibes vs immutable rails; Drupal's built-in guardrails
- [Axelerant: AI Transforming Engineering Workflows](https://www.axelerant.com/blog/how-ai-is-transforming-engineering-workflows) — Structured AI Iteration Loop; 50% debugging effort reduction

**Goran Nikolovski Series (Most Prolific Individual Blogger)**
- [Automating Drupal Dependency Management](https://gorannikolovski.com/blog/automating-drupal-dependency-management-with-custom-claude-code-commands) — Custom Claude Code commands in `.claude/commands/`
- [Claude Code Subagent for Drupal Core Updates](https://gorannikolovski.com/blog/building-a-claude-code-subagent-to-automate-drupal-core-updates) — Autonomous core update workflow in Docker
- [Automated AI Code Reviews for GitLab with n8n](https://gorannikolovski.com/blog/automated-ai-code-reviews-for-gitlab-with-n8n) — Self-hosted; ~$0.008/MR; seven-node n8n workflow

**Dries Buytaert (Strategic Vision)**
- [Claude Code meets Drupal](https://dri.es/claude-code-meets-drupal) — 30-min live demo; Drupal founder endorsement of Claude Code
- [Drupal AI Roadmap for 2026](https://dri.es/drupal-ai-roadmap-for-2026) — Eight core capabilities; page generation, context mgmt, background agents, multi-channel
- [Self-Improving AI Skills](https://dri.es/self-improving-ai-skills) — Supply chain attack risks in shared skill ecosystems
- [Adaptable Drupal Modules](https://dri.es/adaptable-drupal-modules-code-meant-to-be-adapted-not-installed) — New paradigm: AI-adapted modules vs install-and-configure
- [AI Flattens Interfaces and Deepens Foundations](https://dri.es/ai-flattens-interfaces-and-deepens-foundations) — CMS = 30% visible, 70% invisible; AI accelerates Canvas, foundation becomes critical
- [The Software Sovereignty Scale](https://dri.es/the-software-sovereignty-scale) — Drupal is Grade A (structurally sovereign); procurement guidance

**Revival & Contribution**
- [Gábor Hojtsy: DMU Revival in 24 Hours](https://www.hojtsy.hu/blog/2026-mar-07/my-experiment-bringing-drupal-module-upgrader-back-dead-less-24-hours) — AI revived abandoned Drupal Module Upgrader; full test suite passing in hours
- [undpaul: Drupal AI Real Success Stories](https://www.undpaul.de/en/blog/2026/01/19/drupal-ai-success-stories) — 8 real projects; 90-240x speed improvements; 15,000-50,000 user deployments

**Testing & Tooling**
- [Freelock: Unit Testing with Drupal Flake and AI](https://www.freelock.com/blog/john-locke/2025-09/easy-unit-testing-drupal-flake-and-ai-group-purl-case-study) — Reusable ruleset → consistent AI testing assistant
- [Four Kitchens: AI-Driven Testing in Drupal](https://www.fourkitchens.com/blog/development/ai-drupal-testing-development-efficiency/) — Faster development without sacrificing quality
- [PrometSource: AI-Powered Drupal Module Development](https://www.prometsource.com/blog/exploring-ai-drupal-development-1) — Step-by-step tutorial

**Overviews & Aggregators**
- [TheDropTimes: 30 Drupal AI Modules](https://www.thedroptimes.com/50956/30-drupal-ai-framework-and-integration-modules-you-should-know) — Broad module overview
- [DrupalForge: 30 AI Frameworks and Integration Modules](https://www.drupalforge.org/blog/drupal-ai-landscape-30-frameworks-integration-modules-you-should-know) — Landscape overview with demos
- [Drupalize.Me: Drupal AI Setup Guide](https://drupalize.me/blog/drupal-ai-how-set-it-and-try-it-out) — Getting started guide

### Key People

| Person | Organization | Known For |
|--------|-------------|-----------|
| Dries Buytaert | Acquia / Drupal | Strategic oversight; 2026 roadmap; ai.drupal.org |
| Marcus Johansson | FreelyGive | Technical leadership; AI Automators; AI module 1.3 |
| Matthew Grasmick | Acquia | drupal-claude-skills (★ 24); Acquia CLI / BLT creator |
| Scott Falconer | — | drupal-contribute-fix skill; Talking Drupal; DrupalCon Chicago AI Summit |
| Matt Glaman | — | drupalorg-cli; agentic workflows; Talking Drupal |
| Andy Giles | — | Agentic workflows; Canvas CLI; Talking Drupal #538 |
| Jürgen Haas | — | ECA module; orchestration; Talking Drupal #537 |
| Baddý Breidert | 1xINTERNET | Governance; funding; product direction |
| Christoph Breidert | 1xINTERNET | Product roadmap; DrupalCon workshops |
| Jacob Rockowitz | — | Webform module; AI mentoring blog; plan-first advocacy |
| Ronald te Brake | — | AI Coding Starter Kit proposal; Surge module; coding standards skill |
| Mark Conroy | — | AI Single Page Importer module |
| Goran Nikolovski | — | Most prolific AI workflow blogger (7+ posts) |
| Bálint Pekker | Cheppers | AI code review integration |
| Albert Skibinski | — | MCP + Drupal exploration; blog series |
| Mateu Aguiló Bosch | — | ddev-assistant-claude; JSON:API maintainer |
| Michael Schmid | amazee.io / amazee.ai | Privacy AI infrastructure; Talking Drupal #515 |
| Vincenzo Gambino | QED42 | AI Agents development; DrupalCon workshops |
| Gábor Hojtsy | — | Drupal Module Upgrader revival; Drupal 11 readiness |
| Dominique De Cooman | Dropsolid | Fundraising; Drupal AI Academy |
| Frederik Wouters | Dropsolid | Head of Innovation; training; DrupalCon workshops |
| Kristen Pol | Salsa Digital | Cross-team alignment; DrupalCon Chicago keynote |
| Lenny Moskalyk | AI Makers | Community builder; AI Makers meetup |
| Mike Anello | DrupalEasy | Training; "Responsible Drupal AI Basics" workshops |
| Kevin Quillen | Velir | AI module maintainer; semantic search |

---

## Specifications & Standards

### Agent Skills Standard

- [agentskills.io specification](https://agentskills.io/specification) — SKILL.md format; supported by 30+ tools; YAML frontmatter + markdown body; progressive disclosure
- [agentskills/agentskills](https://github.com/agentskills/agentskills) — Validation tool: `skills-ref validate ./my-skill`; `npx skills add` installer
- [anthropics/skills](https://github.com/anthropics/skills) (★ 95,500) — Official Anthropic skills repo; `/plugin marketplace add anthropics/skills`; Creative, Development, Enterprise, Document categories
- [skillmatic-ai/awesome-agent-skills](https://github.com/skillmatic-ai/awesome-agent-skills) — Curated list of all agent skills across ecosystems

### Context File Standards

- [AGENTS.md specification](https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/) — Universal AI context file; supported by Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin
- [CLAUDE.md convention](https://dri.es/claude-code-meets-drupal) — Claude Code-only; project-specific instructions; used by Dries Buytaert for his own Drupal workflow
- [.cursorrules convention](https://cursor.directory/rules/drupal) — Cursor-only; project-level Cursor rules
- [.github/copilot-instructions.md](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions) — GitHub Copilot custom instructions

### Platform Compatibility Matrix

| Format | Claude Code | Cursor | Copilot | Kiro | Gemini | Others |
|--------|:-----------:|:------:|:-------:|:----:|:------:|:------:|
| SKILL.md (agentskills.io) | ✅ | ✅ | ✅ | ✅ | ✅ | 25+ more |
| AGENTS.md | ✅ | ✅ | ✅ | — | ✅ | Aider, Roo, Zed, Devin |
| CLAUDE.md | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| .cursorrules | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| MCP servers | ✅ | ✅ | ✅ | ✅ | ✅ | Most modern tools |
| DDEV addons | Tool-agnostic (environment level) |||||| |

### llms.txt Standard

- [llmstxt.org specification](https://llmstxt.org/) — Standard for helping LLMs use your site content; [GitHub](https://github.com/AnswerDotAI/llms-txt)
- [1xINTERNET guide to llms.txt](https://www.1xinternet.com/en/highlights/llms-txt-website-visibility-ai-search) — Website visibility in AI search era
- [Dries: Markdown, llms.txt and AI Crawlers](https://dri.es/markdown-llms-txt-and-ai-crawlers) — Data-driven analysis; llms.txt = 0.001% of traffic; AI crawlers fetched 1,241 pages per citation

### Active Drupal.org Standards Issues

- [#3565489 — First-class agent-skills support in AI module](https://www.drupal.org/project/ai/issues/3565489) — Modules include `skills/` folder; native agentskills.io support in Drupal AI module ★★★★
- [#3541110 — AI coding starterkit](https://www.drupal.org/project/ai_initiative/issues/3541110) — Unified tool-agnostic starter kit; Surge is the implementation ★★★
- [#3570498 — AI tools for contributors and maintainers](https://www.drupal.org/project/drupal/issues/3570498) — Official Drupal core policy discussion started by Dries; rich debate ★★★★
- [#3574093 — Ban LLM code contributions](https://www.drupal.org/project/drupal/issues/3574093) — Contentious; community leaning toward quality gates over blanket bans ★★★
- [#3558328 — Claude Skill for Drupal Brand Guidelines](https://www.drupal.org/project/ai_initiative/issues/3558328) — Brand standards in AI skill format ★★

---

## Cross-CMS Patterns

Drupal leads the CMS field in organized AI tooling. What other ecosystems have done well is worth learning from.

### Laravel Boost (Drupal's Primary Inspiration)

The explicit model for the Drupal AI Coding Starterkit proposal.

- [Laravel Boost](https://laravel.com/docs/boost) — Single-command AI coding kit; 15+ specialized MCP tools; vectorized version-specific docs; auto-configures AI tool settings
- [ronaldtebrake.nl: AI Coding Starter Kit for Drupal](https://www.ronaldtebrake.nl/blog/embracing-ai-coding-starter-kit-drupal/) — Direct application of Laravel Boost patterns to Drupal

**What Drupal needs from this pattern:** One-command setup (`ddev get drupal/ai-dev-toolkit` equivalent) that bundles everything.

### Shopware AI Coding Tools (PHP CMS — Directly Applicable)

- [shopwareLabs/ai-coding-tools](https://github.com/shopwareLabs/ai-coding-tools) — Claude Code plugin marketplace for Shopware; 6 plugins: dev-tooling (PHPStan, ECS via MCP), gh-tooling, test-writing, ADR writing, CI failure interpretation, code chunking

**Patterns worth adopting for Drupal:**
- ADR (Architecture Decision Record) writing with AI
- CI failure interpretation plugin
- LSP integration for framework-specific intelligence
- AGENTS.md included as standard

### WordPress

- [NickOrtiz/cursorrules](https://github.com/NickOrtiz/cursorrules) — WordPress/Gutenberg Cursor rules; minimal (2 commits); no community coordination

**Assessment:** WordPress AI development is significantly behind Drupal's organized community effort. Drupal's $1.5M initiative with 28 organizations is unique in the CMS space.

### Symfony AI (Drupal's Foundation)

- [Symfony AI Components](https://symfony.com/doc/current/ai.html) — Platform, Agent, Chat, Store, Mate, MCP Bundle; Drupal AI module is building on these components
- [LLPhant](https://github.com/LLPhant/LLPhant) — PHP LangChain equivalent; works with Symfony/Drupal; PHP 8.1+

**Key insight:** Drupal's AI module actively integrating Symfony AI means Drupal developers benefit from the entire PHP AI ecosystem, not just Drupal-specific tools.

### Drupal's Unique Advantages Over All Other CMS

| Capability | Laravel | Shopware | WordPress | Drupal |
|------------|---------|----------|-----------|--------|
| Funded community AI initiative | ❌ | ❌ | ❌ | ✅ $1.5M, 28 orgs |
| Comprehensive AI module (48+ providers) | ❌ | ❌ | ❌ | ✅ drupal/ai |
| Recipe-based AI distribution | ❌ | ❌ | ❌ | ✅ Drupal Recipes |
| Agent skills community (30+ repos) | ❌ | ✅ 6 plugins | ❌ | ✅ 15+ repos, 80+ skills |
| Unified AI starter kit | ✅ Boost | ❌ | ❌ | 🔄 Surge (in progress) |
| MCP integration (site + dev) | ✅ | ✅ | ❌ | ✅ Multiple |
| AGENTS.md / context files | ✅ | ✅ | ❌ | ✅ Droptica + amazee |

---

## Contributing

This list is maintained by the Drupal community. To add a tool:

1. It must be publicly available and Drupal-relevant
2. Include: name, URL, brief description (under 15 words), maturity rating if applicable
3. Place in the most appropriate category
4. Deduplicate — check if it already exists under a different name

**Key community hubs:**
- [Drupal Slack #ai channel](https://drupal.slack.com) — Primary real-time coordination
- [new.drupal.org/ai](https://new.drupal.org/ai) — Official AI initiative page
- [new.drupal.org/ai/makers](https://new.drupal.org/ai/makers) — Certified AI suppliers and makers
- [LobeHub Skills Marketplace](https://lobehub.com/skills) — Drupal skills listed on mainstream AI marketplace

---

*Last updated: March 2026. Based on research covering 300+ URLs, 65+ drupal.org modules, 15+ agent skill repos, 18+ DDEV plugins, and 15+ MCP servers.*
