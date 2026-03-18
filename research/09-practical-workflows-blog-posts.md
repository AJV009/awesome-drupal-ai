# Practical AI Development Workflows for Drupal (Blog Post Deep Dives)

## 1. Tag1: Using AI to Move a 10-Year-Old Drupal Core Issue Forward

**URL:** https://www.tag1.com/blog/moving-10-year-old-drupal-issue-forward-with-ai/
**Issue:** Allow multiple field widgets to not use tabledrag (#2264739) — open for 10 years

### Setup
- Installed `ddev-claude-code`: `ddev add-on get FreelyGive/ddev-claude-code`
- Claude runs inside DDEV container with GitLab CLI access
- Created `.claude` directory for plans, snippets, docs (cross-session continuity)

### Workflow Strategy
1. **Plan-Driven Development:** Request AI write implementation plan first, execute step-by-step with review pauses
2. **Dedicated Context Folder:** `.claude/` directory stores plans, snippets, Drupal config schema guides
3. **Voice Prompts:** Terminal dictation for repetitive questions
4. **Deep Reasoning:** Keywords like "ultrathink" for thorough reasoning before code
5. **Screenshot Uploads:** Paste screenshots for CSS adjustments

### Results
- Configuration schema designed and implemented
- Broad widget coverage achieved
- Extensive tests and documentation added
- Remaining work: theming and documentation polish

### Key Learnings
- **Generate test coverage first** across all widgets to surface edge cases early
- **Plan mode flow:** approve each step before implementation
- **Independently verify tests** rather than trusting automated reports
- **Keep prompts short and focused** for test generation
- **Expert oversight is essential** — "non-negotiable"
- AI acts as "powerful accelerator" for drafts, refactoring, suggestions while human stays accountable

---

## 2. Jacob Rockowitz: Coding Drupal with AI / AI Mentoring

**URL:** https://www.jrockowitz.com/blog/coding-drupal-with-ai

### Key Insights
- AI value is in **enhancing comprehension and documentation** not just faster code
- Community should create **AGENTS.md files** in Drupal core for better AI context
- AI as **mentoring tool** for new Drupal contributors
- "The argument that AI writes 'bad code' seems ridiculous because developers are letting it write bad code and not giving it 'good code' examples"
- Senior devs should share their agentic workflows

### Workflow
- Iterative: Markdown requirements → AI → review output → refine
- Created personalized cheatsheet comparing language paradigms
- Used AI for documentation and explanatory comments

### Recommendation for Community
"Senior developers in the Drupal community should share their agentic Drupal coding workflows so we can learn from one another."

---

## 3. Ronald te Brake: AI Coding Starter Kit for Drupal

**URL:** https://www.ronaldtebrake.nl/blog/embracing-ai-coding-starter-kit-drupal/
**Inspired by:** Laravel Boost

### Vision: Unified AI Framework for Drupal
- Single-command installation (module or Composer package)
- AI tool configs auto-populated with Drupal standards
- Real-time Drupal documentation and API references
- Sandboxed Drush commands, scaffolding, log checking
- Version-aware suggestions from official sources

### Components Mentioned
- **CLAUDE.md** — Drupal-specific best practices
- **MCP servers** — specialized tools for Drupal
- **Context7** — version-specific documentation
- **Drupal MCP Module** — site content exposure to AI
- **Claude Code Module** — Claude integration

### Key Assessment
Current Drupal AI solutions are "fragmented and experimental" across multiple tools. Duplicated effort and inconsistent guidance undermines productivity. **Unified approach needed.**

### Proposal
Active at drupal.org: **"AI coding starterkit proposal"** at drupal.org/project/ai_initiative/issues/3541110

---

## 4. Droptica: AGENTS.md for Drupal

**URL:** https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/
**GitHub:** github.com/droptica/drupal-agents-md

### Setup (5 minutes)
1. `curl` download AGENTS-TEMPLATE.md
2. Copy prompt from README into AI tool
3. AI scans project, generates customized AGENTS.md

### Coverage
Infrastructure, customization, architecture, workflow, frontend, security, testing

### Results
- Onboarding "several times faster"
- Reduced AI hallucinations
- Works with: Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin

---

## 5. DDEV Blog: Claude Code for DDEV Contributions

**URL:** https://ddev.com/blog/claude-code-ai-pr-for-ddev-contributor-training/
**Coverage:** https://www.thedroptimes.com/54452/using-claude-code-ai-contribute-ddev-contributor-training-recap

### Key Takeaway
Official DDEV contributor training now uses Claude Code. Demonstrates the pattern for AI-assisted open source contributions applicable to drupal.org.

---

## 6. Bálint Pekker: AI Code Review for Drupal

**URL:** https://bpekker.dev/ai-code-review/
**Also:** https://cheppers.com/post/drupal-ai-code-review

### Approach
- Claude AI for automated Drupal code reviews
- Goes beyond static analysis (phpstan, drupal-check) with contextual understanding
- Reviews: .php, .module, .install, .theme, .twig, YAML files
- Skips: core, contrib, vendor, non-critical directories
- Interprets code structure, flags logic flaws, suggests architectural improvements

### CI/CD Integration (Bounteous)
**URL:** https://www.bounteous.com/insights/2025/07/07/automating-drupal-code-refactoring-and-reviews-llms/
- LLM-based review in CI/CD pipeline as "first pass" reviewer
- Catches deprecations, enforces standards, suggests improvements
- **Hybrid approach:** LLM reviews + static analysis + human review

---

## 7. FreelyGive: Intro to Drupal AI Module

**URL:** https://freelygive.io/blog/detail-intro-new-drupal-ai-module
- Detailed introduction to the Drupal AI module from the core team
- Marcus Johansson's perspective as technical lead

---

## 8. Freelock: Unit Testing with Drupal Flake and AI

**URL:** https://www.freelock.com/blog/john-locke/2025-09/easy-unit-testing-drupal-flake-and-ai-group-purl-case-study

### Approach
- AI as test-writing partner
- Rarely perfect tests, but faster starting point
- **Key pattern:** Capture lessons in reusable ruleset → AI becomes consistent testing assistant

---

## 9. Four Kitchens: AI-Driven Testing in Drupal

**URL:** https://www.fourkitchens.com/blog/development/ai-drupal-testing-development-efficiency/
- AI-driven testing for faster development without sacrificing quality
- (Full content not extractable from page)

---

## Common Workflow Patterns Across All Posts

### The Standard Setup
1. **DDEV + Claude Code:** `ddev add-on get FreelyGive/ddev-claude-code`
2. **Context directory:** `.claude/` with plans, reference docs, snippets
3. **AGENTS.md or CLAUDE.md:** Project context file for AI
4. **Quality gates:** phpcs, phpstan, phpunit via DDEV commands
5. **Plan-first approach:** AI writes plan, human reviews, then executes

### Key Principles (Consensus)
- AI accelerates, humans accountable
- Context is king — provide good docs, examples, standards
- Test-first or test-early with AI assistance
- Expert oversight is essential — always review AI output
- Share workflows with the community

### The Gap
No unified, one-command setup exists yet. The "AI Coding Starter Kit" proposal at drupal.org is the closest attempt to standardize.

---

## 10. Dries Buytaert Blog Posts on AI (dri.es)

Dries uses Claude Code personally with a custom CLAUDE.md for his Drupal workflow.

### "Self-improving AI Skills" (Jan 30, 2026)
- **URL:** https://dri.es/self-improving-ai-skills
- Explores Moltbook (platform for AI agents sharing learned techniques via skill file URLs)
- Warns about supply chain attack risks: "One bad skill poisons everything that trusts it"
- Recommends building robust containment mechanisms before adopting skill-sharing

### "AI Creates Asymmetric Pressure on Open Source" (Jan 29, 2026)
- **URL:** https://dri.es/ai-creates-asymmetric-pressure-on-open-source
- AI lowers contribution barrier but evaluation burden stays on maintainers
- Case study: curl's maintainer ended bug bounty — fewer than 1 in 20 submissions were real bugs
- Proposes: experiment on your own work first, demonstrate results, share findings

### "AI Flattens Interfaces and Deepens Foundations" (Dec 23, 2025)
- **URL:** https://dri.es/ai-flattens-interfaces-and-deepens-foundations
- CMS is ~30% visible (page builders) and ~70% invisible (content models, APIs)
- AI accelerates the visible layer; foundation becomes increasingly critical
- Drupal responding with Canvas 1.0 and AI-driven page generation

### "The Control Layers of AI" (Dec 30, 2025)
- **URL:** https://dri.es/the-control-layers-of-ai
- Three-layer model: outer (deterministic workflow), middle (AI decisions), inner (precise tools)
- "Outside In" (workflow platforms control AI) vs "Inside Out" (AI controls tools)
- References Drupal's ECA module as hybrid model example

### "AI is a Business Model Stress Test" (Jan 9, 2026)
- **URL:** https://dri.es/ai-is-a-business-model-stress-test
- AI commoditizes anything fully specifiable: docs, components, CSS libs, plugins
- Tailwind Labs case study: 75% engineering layoff after docs traffic dropped 40%
- Open source was never the product; operational services around it are

### "Markdown, llms.txt and AI Crawlers" (Mar 5, 2026)
- **URL:** https://dri.es/markdown-llms-txt-and-ai-crawlers
- Cloudflare logs: for every citation AI sent, crawlers fetched **1,241 pages**
- Offering Markdown didn't reduce bot traffic; crawler traffic increased 7%
- llms.txt received 52 requests — all from SEO audit tools, none from AI engines
- llms.txt = 0.001% of traffic across Acquia's hosting fleet

### "The Software Sovereignty Scale" (Feb 10, 2026)
- **URL:** https://dri.es/the-software-sovereignty-scale
- Five-grade scale (A-E); Drupal is Grade A (structurally sovereign)
- Governments should evaluate AI-integrated systems' sovereignty grade for procurement
- Relevant for EC/Europa Web Platform context

---

## 11. Goran Nikolovski (gorannikolovski.com) — 7 AI Posts

Most prolific individual Drupal developer blogging about AI coding.

### "Automating Drupal Dependency Management with Custom Claude Code Commands" (Nov 21, 2025)
- **URL:** https://gorannikolovski.com/blog/automating-drupal-dependency-management-with-custom-claude-code-commands
- Created `/check-unused-modules` command in `.claude/commands/`
- Pattern applies to security audits, code quality analysis, config drift detection

### "Building a Claude Code Subagent to Automate Drupal Core Updates" (Aug 16, 2025)
- **URL:** https://gorannikolovski.com/blog/building-a-claude-code-subagent-to-automate-drupal-core-updates
- Subagent for Drupal core update workflows; all commands within Docker container
- Claude Code autonomously recognized update request matched subagent's expertise

### "Building a Custom MCP Server: Making AI Assistants Understand Your Projects" (Sep 28, 2025)
- **URL:** https://gorannikolovski.com/blog/building-a-custom-mcp-server-making-ai-assistants-understand-your-projects
- Centralized MCP server distributing project knowledge as markdown files
- Intentionally "primitive" — basic filename matching, not RAG

### "From Vibe to Structure: How Backlog.md Transforms Your Development Workflow" (Oct 4, 2025)
- **URL:** https://gorannikolovski.com/blog/from-vibe-to-structure-how-backlogmd-transforms-your-development-workflow
- Backlog.md (github.com/MrLesk/Backlog.md) — markdown-native task manager in git repos
- Claude Code reads task specs and generates implementation plans

### "Automated AI Code Reviews for GitLab with n8n" (May 31, 2025)
- **URL:** https://gorannikolovski.com/blog/automated-ai-code-reviews-for-gitlab-with-n8n
- Self-hosted: ~$0.008 per MR review using Claude 3-Haiku
- Seven-node n8n workflow: GitLab trigger → diff → LLM review → comment → Slack

### "From Zero to Chatbot" series (Dec 2024 — Feb 2025)
- Part 1: Text-to-vectors with Qdrant + OpenAI embeddings (3,072 vectors/article)
- Part 2: Deep Chat JS + Qdrant semantic search + OpenAI RAG

---

## 12. Lullabot — AI Articles & Podcast

### "AI Will Supercharge Your CMS (Not Replace It)" (Oct 1, 2025)
- **URL:** https://www.lullabot.com/articles/artificial-intelligence-will-supercharge-your-cms-not-replace-it
- 290+ AI modules, 21 major providers in Drupal ecosystem
- AI handles repetitive work; CMS manages governance

### "How Automated Code Review Tools Reduce PR Bottlenecks" (Sep 3, 2025)
- **URL:** https://www.lullabot.com/articles/how-automated-code-review-tools-reduce-pull-request-bottlenecks
- Tested: CodeRabbit.ai, Codacy, GitHub Copilot, Google Gemini Code Assist
- **Winner:** Gemini Code Assist — superior accuracy, minimal false positives, free on GitHub

### "Building an AI-Powered Project Management System" (Sep 17, 2025)
- **URL:** https://www.lullabot.com/articles/building-ai-powered-project-management-system
- Cursor Memory Bank: 6 foundational files, `npx cursor-bank init`

### "Smart AI Integration: Beyond Chatbots" (Sep 10, 2025)
- **URL:** https://www.lullabot.com/articles/smart-ai-integration-moving-beyond-chatbots-and-quick-fixes
- "Context engineering" — deliberately designing what information AI gets

---

## 13. undpaul — "Drupal and AI: Real Success Stories" (Jan 19, 2026)

- **URL:** https://www.undpaul.de/en/blog/2026/01/19/drupal-ai-success-stories
- **Author:** Anja Schirwinski (CEO)
- **Metrics from real projects:**
  - 1xINTERNET & World Cancer Day: AI content moderation with human oversight
  - annertech & French Telecom: Reverse image search — 99% reliability
  - Southwark Council: AI PDF accessibility — 240x faster than manual
  - DB Schenker: Email categorization — weeks reduced to minutes
  - FreelyGive & ESP Group: Railway compensation — 90% auto-verified, 80% time reduction
  - Dropsolid & pidpa: Customer service bot — 15% efficiency increase
  - Liip & Canton Basel-Landschaft: Government chatbot — 50,000 inquiries in year 1
  - Factorial & Boehringer Ingelheim: Semantic page matching across 45 country sites

---

## 14. Morpht — AI Views Agent (Feb 3, 2026)

- **URL:** https://www.morpht.com/blog/introducing-drupal-ai-views-agent
- **Author:** Jibran Ijaz
- AI agent for creating/updating Views through natural language
- Configuration schema API validates all changes before saving
- Status: Experimental, not production-ready

---

## 15. QED42 — Custom Canvas AI Agents + HAAT

### "Create Your Own AI Agents for Drupal Canvas" (Feb 18, 2026)
- **URL:** https://www.qed42.com/insights/create-your-own-ai-agents-for-drupal-canvas
- Step-by-step: create sub-agent → integrate with orchestrator → test

### "HAAT Deep Dive: Human-As-A-Tool" (Mar 17, 2026)
- **URL:** https://www.qed42.com/insights/haat-deep-dive-turning-human-intervention-into-a-scalable-primitive
- Repositions humans as "a dependency reachable inside the execution graph"
- One human can support 1,000+ agents through async interaction

---

## 16. Acquia — "Vibes on Rails" (Mar 2, 2026)

- **URL:** https://www.acquia.com/blog/vibes-rails
- **Author:** Scott Falconer
- "System-in-the-loop governance" for scaling AI agents in enterprise
- Agent actions ("vibes") vs immutable enforcements ("rails"): schema validation, RBAC, workflow gates, audit trails
- Drupal's built-in guardrails: typed content, native permissions, content moderation, revision history, config-as-code

---

## 17. Axelerant — AI Engineering Workflows

### "How AI Is Transforming Engineering Workflows" (Mar 12, 2026)
- **URL:** https://www.axelerant.com/blog/how-ai-is-transforming-engineering-workflows
- "Structured AI Iteration Loop": Plan → Generate → Run → Diagnose → Refine → Validate
- "AI-assisted workflow reduced hands-on debugging effort by at least half"

### "How AI Is Quietly Rewriting Axelerant's Engineering Playbook" (Nov 20, 2025)
- **URL:** https://www.axelerant.com/blog/ai-rewriting-axelerants-engineering-playbook
- Three shifts: AI as strategic thought partner, infrastructure toolchain replacement, cognitive time recovery

---

## 18. 1xINTERNET — AI Summit at FOST (Dec 12, 2025)

- **URL:** https://www.1xinternet.com/en/highlights/drupal-ai-summit-fost-insights
- 120+ participants at Drupal AI Summit in Paris
- S1x SIGNALS Framework: AIO (AI Optimization) + GEO (Generative Engine Optimization)
- Christoph Breidert: "Website traffic is dropping dramatically as AI search replaces traditional clicks"

---

## 19. Robert Menetray — "OpenCode + DDEV: How I Built a Drupal Development Environment with 16 AI Agents"

- **URL:** https://menetray.com/en/blog/opencode-ddev-how-i-built-drupal-development-environment-16-ai-agents
- **Author:** Robert Menetray
- **Relevance:** HIGH — Most comprehensive documented multi-agent Drupal dev setup using OpenCode (not Claude Code)

### What Was Built
A containerized AI development environment: OpenCode (open-source, provider-agnostic AI CLI) + DDEV + 16 specialized agents across 3 Docker containers. 7,000+ lines of config. Includes autonomous overnight execution via Ralph Loop (~500-line bash script).

### Three-Container Architecture
1. **OpenCode Container** — AI agents, code reading/execution, Drush/Composer commands
2. **Web Container** — Standard DDEV: Drupal, Drush, quality tools (PHPCS, PHPStan, PHPUnit)
3. **Playwright Container** — Headless browser for visual testing

### The 16 Agents

**Development (6):**
| Agent | Role |
|-------|------|
| drupal-dev | Backend development, Drupal API work |
| drupal-theme | Frontend, Twig template development |
| drupal-test | PHPUnit testing |
| drupal-perf | Performance optimization, caching |
| drupal-update | Composer updates, database migrations |
| twig-audit | Template auditing |

**Quality (2):**
| Agent | Role |
|-------|------|
| three-judges | Three-person quality gate (architecture, security, performance) |
| output-verifier | Validates accuracy of generated outputs |

**Content (3):**
| Agent | Role |
|-------|------|
| blog-writer | Technical articles |
| sales-copy | Landing page content |
| email-responder | Professional email composition |

**Utility (5):**
| Agent | Role |
|-------|------|
| applier | Mechanically applies code changes via SEARCH/REPLACE (separation of concerns) |
| code-explorer | Quick codebase navigation |
| deep-research | In-depth investigation tasks |
| ralph-planner | Generates requirements and task lists |
| visual-test | Playwright-based browser testing |

### Key Patterns
- **Applier pattern** — Analysis agents are read-only, generate SEARCH/REPLACE proposals. A separate `applier` agent mechanically applies changes. Prevents over-modification.
- **Three-judges gate** — Quality review before human sees proposals (architecture + security + performance)
- **LiteLLM proxy** — Routes tasks to appropriate models: Claude Opus for reasoning, cheaper open-source models for mechanical tasks. 2-3x cost savings vs all-Anthropic.
- **Ralph Loop** — Autonomous execution: converts requirements.md into prioritized tasks (P0-P3) via Beads (git-based task tracking), loops through pending tasks. No git commit/push/destructive ops allowed (safety boundary).
- **60/20/20 split** — "Sixty percent AI execution, twenty percent human planning, twenty percent final review"

### Skills (12 total, key ones)
- drupal-audit, run-quality-checks, drupal-module-scaffold, playwright-browser-testing, drush-commands

### Custom DDEV Commands
```
ddev opencode          # Interactive mode
ddev opencode ralph    # Autonomous mode
ddev phpunit           # Quality tools
ddev phpstan
```

### Results
- "Hours needed to reach same solution dropped significantly"
- Tasks previously taking "entire afternoon" now solved in "fraction of that time"
- Config not publicly shared yet (personal credentials, client context embedded)

