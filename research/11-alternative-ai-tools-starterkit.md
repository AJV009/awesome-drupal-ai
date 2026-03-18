# Alternative AI Tools, Cursor Rules, Copilot, Kiro, Nebula & Starterkit Proposal

## Cursor IDE Rules for Drupal

### Drupal Rules on Cursor Directory
- **URL:** https://cursor.directory/rules/drupal
- **Description:** Community-maintained Drupal rules for Cursor IDE
- **Relevance:** HIGH — direct Cursor configuration for Drupal

### Drupal 11 Cursor Rules Guide
- **URL:** https://cursorrules.org/article/drupal-11-cursorrules-prompt-file
- **Description:** Drupal 11 development rules for Cursor
- **Relevance:** HIGH

### ivangrynenko/cursorrules (GitHub)
- **URL:** https://github.com/ivangrynenko/cursorrules
- **Description:** Set of cursor rules for Cursor AI IDE supporting PHP, Python, JavaScript, and Drupal-specific rules
- **Relevance:** HIGH — Drupal-specific Cursor configuration from Ivan Grynenko

### awesome-cursorrules Collection
- **URL:** https://github.com/PatrickJS/awesome-cursorrules
- **Description:** Curated collection of .cursorrules configurations
- **Relevance:** MEDIUM — general collection, may contain Drupal examples

### Drupal.org Issue: "Create docs for Cursor and Claude code quality for CCC"
- **URL:** https://www.drupal.org/project/ai_context/issues/3572891
- **Description:** Active issue to create documentation for Cursor and Claude integration
- **Relevance:** HIGH — official effort

### Drupal.org Issue: "Plan to create ai-rules for Drupal"
- **URL:** https://www.drupal.org/project/surge/issues/3544054
- **Description:** Planning centralized AI rules for Drupal development
- **Relevance:** HIGH — standardization effort

---

## GitHub Copilot for Drupal

### Custom Instructions for Copilot
- **GitHub Docs:** https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions
- **Copilot Code Review:** https://docs.github.com/en/copilot/tutorials/use-custom-instructions
- **Instructions spec:** https://copilot-instructions.md/
- **Awesome Copilot:** https://github.com/github/awesome-copilot

### Drupal-Specific Copilot Guides
- **"Maximizing GitHub Copilot for Drupal Development":** https://www.thedroptimes.com/38853/maximizing-github-copilot-drupal-development
- **"Do's and Don'ts of GitHub Copilot (For Drupal Developers)":** https://www.thirdandgrove.com/insights/dos-and-donts-github-copilot-drupal-developers/
- **"Getting started with AI assisted development - GitHub Copilot | Drupal":** https://www.ramsalt.com/en/blog/getting-started-ai-assisted-development-github-copilot
- **"Accelerated Drupal Contribution using GitHub Copilot":** https://medium.com/@arpitrastogi_62655/accelerated-drupal-contribution-using-github-copilot-abed4c50d37f
- **"Using GitHub Copilot with Drupal Development":** https://drupal.com.ua/index.php/38/using-github-copilot-drupal-development

---

## Kiro IDE (Amazon) for Drupal

### Kiro Overview
- **URL:** https://kiro.dev/docs/
- **Skills Docs:** https://kiro.dev/docs/skills/
- **Changelog:** https://kiro.dev/changelog/ide/
- **Custom Subagents:** https://kiro.dev/changelog/ide/0-9/ and https://kiro.dev/blog/custom-subagents-skills-and-enterprise-controls/
- **Powers (skills system):** https://kiro.dev/blog/introducing-powers/

### Kiro Skill Format
- Reads from `.kiro/skills/` directory
- Same SKILL.md format as Claude Code (agentskills.io standard)
- Supports custom subagents, agent skills, hooks, code review

### Drupal-Specific Kiro Content
- No Drupal-specific Kiro skills found publicly yet
- Skills format is identical to Claude Code — any Drupal SKILL.md works in both
- **Gap:** No `.kiro/` Drupal configurations exist yet

---

## Gemini CLI for Drupal

### Gemini CLI
- **URL:** https://developers.google.com/gemini-code-assist/docs/gemini-cli
- **GitHub:** https://github.com/google-gemini/gemini-cli
- **Docs:** https://docs.cloud.google.com/gemini/docs/codeassist/gemini-cli
- **Conductor extension:** https://github.com/gemini-cli-extensions/conductor
- **Hooks guide:** https://developers.googleblog.com/tailor-gemini-cli-to-your-workflow-with-hooks/

### Drupal-Specific Gemini Content
- Gemini Provider module: https://www.drupal.org/project/gemini_provider
- No dedicated Gemini CLI configurations for Drupal found
- GEMINI.md file convention supported for context (similar to CLAUDE.md)
- **Gap:** No `.gemini/` Drupal configurations exist yet

---

## Alternative AI Coding Tools with Drupal

### Aider
- Open-source AI coding agent
- No Drupal-specific configurations found
- Supported by AGENTS.md standard (Droptica)
- **Gap:** No dedicated Drupal aider setup

### OpenCode
- Open-source terminal-based coding agent
- dragonwize/ddev-opencode exists as DDEV addon
- **URL (DDEV):** https://github.com/dragonwize/ddev-opencode
- General comparison: https://openalternative.co/compare/aider/vs/opencode

### Cline
- VS Code extension for AI coding
- Cleversoft-IT MCP servers integrate with Cline
- Used in Drupal context through MCP compatibility

---

## Acquia Nebula

### What It Actually Is
**URL:** https://github.com/acquia/nebula
**IMPORTANT:** NOT an AI coding assistant CLI. Nebula is a **template repository for scaffolding Drupal Canvas Code Components.**

### Purpose
- Starter template used by `@drupal-canvas/create` CLI tool
- Scaffolds new codebases to work with Drupal Canvas Code Components
- Pre-configured development environment with AI-assisted development built in

### Installation
```bash
npx @drupal-canvas/create@latest
```

### Technology Stack
- Storybook for component development
- Vite with SWC compiler
- Tailwind CSS v4
- Prettier + ESLint
- Husky + lint-staged pre-commit hooks
- GitHub Actions for CI

### AI Features
- Agent skills in `.agents/skills/` directory
- Native support: Amp, Codex, Gemini CLI, GitHub Copilot, Kimi Code CLI, OpenCode
- Manual symlink for: Cursor, Claude Code
- Skills from skills.sh registry

### Drupal.org Integration
- Issue: Set acquia/nebula as recommended template (#3571591)
- Canvas 1.2.0 release: https://www.drupal.org/project/canvas/releases/1.2.0

---

## AI Coding Starterkit Proposal (drupal.org)

### Issue Details
- **URL:** https://www.drupal.org/project/ai_initiative/issues/3541110
- **Title:** AI coding starterkit
- **Status:** Active
- **Priority:** Normal
- **Category:** Feature request
- **Reporter:** ronaldtebrake
- **Created:** August 13, 2025
- **Updated:** January 18, 2026
- **Assigned:** Unassigned

### Problem Statement
Drupal lacks unified AI-assisted development approach. Current ecosystem is "fragmented" with scattered solutions: Claude Code module, MCP servers, custom Cursor rules.

### Proposed Features
- **Tool-agnostic** AI developer starter kit
- Version-specific Drupal documentation accessible to AI tools
- Current coding standards and best practices
- Optional Drupal.org-hosted MCP server
- Lightweight, infrastructure-independent design
- Easy integration with Claude.md, Cursor Rules, etc.

### Community Response
- Multiple +1s from developers
- ronaldtebrake began development at "surge" project
- References to Linux kernel examples and GitHub's spec-kit
- Interest in documentation MCP as starting point

### Related Drupal.org Issues
- **AI tools for contributors and maintainers:** https://www.drupal.org/project/drupal/issues/3570498
- **Plan to create ai-rules for Drupal:** https://www.drupal.org/project/surge/issues/3544054

### Coverage
- **TheDropTimes:** https://www.thedroptimes.com/51292/ronald-te-brake-proposes-ai-coding-starter-kit-drupal-developers

---

## llms.txt Standard for Drupal

### The Standard
- **Spec:** https://llmstxt.org/
- **GitHub:** https://github.com/AnswerDotAI/llms-txt
- **Purpose:** Help LLMs use your website content

### Drupal Modules
1. **/llms.txt:** https://www.drupal.org/project/llms_txt
2. **LLMs.txt Generator:** https://www.drupal.org/project/llms_txt_generator
3. **llms txt exporter:** https://www.drupal.org/project/llms_txt_exporter

### Notable Implementation
- **Pronovix Drupal Recipe for llms.txt:** https://www.thedroptimes.com/49424/pronovix-releases-drupal-recipe-llmstxt-support-ai-ready-content
- Distributed as Drupal Recipe (modern approach)

### Coverage
- **Future-Proofing SEO with llms.txt:** https://www.thedroptimes.com/54703/future-proofing-seo-with-llmstxt-preparing-drupal-sites-ai-search
- **1xINTERNET guide:** https://www.1xinternet.com/en/highlights/llms-txt-website-visibility-ai-search
- **Drupal4u guide:** https://www.drupal4u.org/tips-and-tricks/best-modules-and-resources-add-llmstxt-drupal

---

## Vibe Coding with Drupal

### Key Article
- **"Coding Drupal with AI: Jacob Rockowitz on Mentoring, Vibe Coding and Developer Workflows"**
- **URL:** https://www.thedroptimes.com/66624/coding-drupal-with-ai-jacob-rockowitz-vibe-coding-workflows
- Term "vibe coding" being adopted in Drupal community

---

## AI Developer Assistant Module
- **URL:** https://www.drupal.org/project/aidev
- **Description:** AI developer assistant module on drupal.org

---

## Managed Claude Stack (MCS) — Configuration Engine for Claude Code

- **URL:** https://github.com/bguidolim/mcs
- **Stars:** 65 | **Forks:** 4 | **License:** MIT
- **Language:** Swift (macOS 13+)
- **Install:** `brew install bguidolim/tap/managed-claude-stack`
- **Description:** Configuration engine for Claude Code that packages development environments into shareable "tech packs." Tech packs are Git-based repos with `techpack.yaml` manifests bundling MCP servers, plugins, hooks, skills, commands, and settings.

### Key Features
- **Tech Pack System** — Git-based, shareable config bundles (like Homebrew casks for Claude Code)
- **Convergence Sync** — Re-running `mcs sync` adds missing artifacts, removes deselected packs, updates changed elements
- **Drift Detection** — `mcs doctor --fix` detects and repairs configuration drift
- **Safety** — Timestamped backups, `--dry-run` previews, SHA-256 verification, lockfiles for version pinning
- **Dual Scope** — Per-project and global artifact installation

### Core Workflow
```bash
mcs pack add [pack-name]   # Add a tech pack
mcs sync                    # Converge configuration
mcs doctor                  # Verify setup
```

### Example Packs
- `mcs-core-pack` — Foundational Claude Code settings
- `mcs-continuous-learning` — Persistent memory across sessions
- `mcs-ios-pack` — Xcode/Swift integration

### Drupal Relevance
- **Not Drupal-specific yet**, but a Drupal/DDEV tech pack could bundle all Drupal skills, MCP servers, and DDEV integrations into one installable pack
- The tech pack pattern maps well to the "one-command setup" goal for Drupal AI development
- Could become the distribution mechanism for a Drupal AI devkit
- **Relevance:** HIGH — potential for Drupal/DDEV tech pack distribution

---

## oh-my-claudecode — Multi-Agent Orchestration for Claude Code

- **URL:** https://github.com/Yeachan-Heo/oh-my-claudecode
- **Stars:** 10,100+ | **Forks:** 712 | **License:** MIT
- **Language:** TypeScript/JavaScript
- **npm package:** `oh-my-claude-sisyphus`
- **Description:** Multi-agent orchestration framework for Claude Code. Zero learning curve — extends Claude Code with intelligent defaults and natural language interfaces.

### Orchestration Modes
- **Team** — Canonical staged pipeline: plan → PRD → execute → verify → fix
- **Autopilot** — Autonomous end-to-end execution
- **Ralph** — Persistent mode with verify/fix loops
- **Ultrawork** — Maximum parallelism
- **Pipeline** — Sequential multi-step processing
- **omc team** — tmux CLI workers supporting Codex/Gemini/Claude simultaneously

### Key Features
- 32 specialized agents (architecture, research, design, testing, data science)
- Smart model routing (Haiku for simple tasks, Opus for complex reasoning) — 30-50% token cost savings
- Magic keywords: `ralph`, `ulw`, `ralplan`, `deep-interview`, `deepsearch`, `ultrathink`
- HUD statusline for real-time visibility
- Skill learning from sessions
- Analytics and cost tracking
- Notification integrations: Telegram, Discord, Slack webhooks

### Installation
```bash
# Claude Code plugin marketplace
/plugin marketplace add https://github.com/Yeachan-Heo/oh-my-claudecode
/plugin install oh-my-claudecode

# Or via npm
npm i -g oh-my-claude-sisyphus@latest
```

### Requirements
- Claude Code CLI + Claude Max/Pro subscription or API key
- tmux (for team features, rate-limit detection)
- Optional: Gemini CLI, Codex CLI for multi-AI orchestration

### Drupal Relevance
- **Not Drupal-specific**, but directly applicable to Drupal development workflows
- The multi-agent orchestration patterns (plan → execute → verify → fix) map well to Drupal migration and component building workflows
- Ralph mode and Ultrawork mode are useful for large-scale repetitive Drupal tasks
- Could be combined with Drupal-specific skills for enhanced development workflows
- **Relevance:** MEDIUM — general-purpose Claude Code enhancement, high utility for any complex Drupal project
