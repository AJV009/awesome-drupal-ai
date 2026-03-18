# Drupal AI Roadmap 2026 & Canvas AI

## Drupal AI Roadmap 2026

**Published:** February 11, 2026 by Dries Buytaert
**URL:** https://dri.es/drupal-ai-roadmap-for-2026
**Full Plan PDF:** https://dri.es/files/drupal-ai-roadmap-2026.pdf
**Drupal.org:** https://www.drupal.org/blog/drupals-ai-roadmap-for-2026

### Eight Core Capabilities

1. **Page Generation** — "Describe what you need and get a usable page, built from your actual design system components"
2. **Context Management** — Centralized definitions for brand voice, style guides, audience profiles, and governance rules
3. **Background Agents** — AI functioning autonomously based on triggers and schedules while respecting editorial workflows
4. **Design System Integration** — AI building with existing components and proposing new ones when needed
5. **Content Creation and Discovery** — Enhanced search, optimization capabilities, and drafting assistance
6. **Advanced Governance** — Batch approvals, branch-based versioning, comprehensive audit trails
7. **Intelligent Website Improvements** — Performance-based learning with concrete change proposals
8. **Multi-Channel Campaigns** — Single campaign goal producing content for websites, social media, email, and automation

### Strategic Philosophy
AI embedded "into the content and page creation process itself, guided by the structure, governance, and brand rules" — NOT bolting on separate tools. Builds on Drupal's strengths: structured content, workflows, permissions, revisions, moderation.

### Resources
- 28 organizations, 50+ individual contributors
- $1.5 million in combined cash and in-kind contributions
- Two dedicated delivery teams: QED42 (innovation) + 1xINTERNET (productization)

---

## Execution Strategy (2026)

**URL:** https://www.drupal.org/about/starshot/initiatives/ai/blog/from-strategy-to-execution-how-the-drupal-ai-initiative-is-scaling-delivery-for-2026

### Delivery Model
- RFP process launched October 2025 for delivery partners
- Initial 6-month engagement starting January 2026
- Two-week sprint cycles established
- QED42: Innovation workstream (forward-looking capabilities)
- 1xINTERNET: Product Development workstream (stable, production-ready features)

### Governance
- Pre-proposal briefings, clarification periods, structured review
- Evaluation: governance, roadmap management, delivery approach, QA, financial oversight, Drupal/AI experience
- Independent reviews + leadership comparison sessions

### Coverage
- https://www.thedroptimes.com/66376/drupal-ai-initiative-selects-qed42-and-1xinternet-lead-2026-delivery-workstreams

---

## Four Weeks of High Velocity Development

**URL:** https://www.drupal.org/about/starshot/initiatives/ai/blog/four-weeks-of-high-velocity-development-for-drupal-ai
**Coverage:** https://www.thedroptimes.com/66491/drupal-ai-initiative-reports-four-weeks-high-velocity-development

### Sprint Performance
- **143 issues resolved in first two weeks**
- Largest regular patch release in AI module history

### Major Deliverables

| Feature | Description |
|---------|-------------|
| AI Dashboard | Central hub for managing AI features and providers, shipped with Drupal CMS 2.0 |
| Advanced Automation | New JSON and Audio field automators for complex data types |
| Context Control Center | Evolved from config to content entities, revision management, targeting |
| Markdown Editor | New editor for prompt fields with type-ahead autocomplete for variables/tokens (AI module 1.3) |
| Agents Debugger | Developer module tracing AI agent interactions in real-time |
| Symfony AI Integration | Ongoing advancement |
| MCP Implementation | Model Context Protocol integration |
| Reranking Models | Enhanced search quality |

---

## Drupal CMS 2.0

**URL:** https://www.drupal.org/blog/drupal-cms-20-is-here-visual-building-ai-and-site-templates-transform-drupal
- Visual building + AI + site templates
- AI Dashboard included

---

## Canvas AI Assistant

**URL:** https://project.pages.drupalcode.org/canvas/ai-assistant/
**Coverage:** https://www.thedroptimes.com/55636/drupal-canvas-ai-assistant-enables-prompt-based-page-building-with-sdcs

### Three Specialized Agents
1. **Page Builder Agent** — Constructs pages using existing components (trigger: "place", "use")
2. **Component Agent** — Creates new code components (trigger: "create", "add")
3. **Template Builder Agent** — Generates complete page templates, headers, footers

### Architecture
- **Canvas AI Orchestrator** — Intelligent router analyzing user intent, directing to appropriate agent
- Retrieves all enabled components as contextual information
- Users control placement via directional vocabulary ("top", "bottom", "below", "above")
- Nesting via "into" or "inside" terms

### Setup
- Enable `canvas_ai` submodule (or `xb_ai_assistant`)
- Configure AI provider supporting function calling (OpenAI recommended)
- Set provider for all Chat operation types
- ✨ icon appears in Canvas interface

### Cost & Performance
- Context often exceeds 30,000 tokens due to component metadata
- Mitigation: disable unused components, refine descriptions, filter component types
- Select models with low per-token input costs

### Known Limitations
- Non-deterministic: variable results from identical prompts
- Occasional generation of nonexistent enum values or component IDs
- Vague wording yields inconsistent outputs

### Related Resources
- QED42 deep dive: https://www.qed42.com/insights/inside-drupal-canvas-ai-how-agents-turn-prompts-into-pages
- DrupalForge template: https://www.drupalforge.org/template/drupal-canvas-ai
- Canvas builder recap: https://www.rollin.ca/resources/canvas-builder-for-drupal-official-recap-of-its-release-candidate-launch-and-ai-powered-capabilities/
- Lovable AI + Canvas workflow demo at DrupalCamp Delhi: https://www.thedroptimes.com/66977/lovable-ai-and-drupal-canvas-workflow-be-demonstrated-at-drupal-camp-delhi

---

## Drupal Digests for AI Development Tracking
**URL:** https://www.thedroptimes.com/66530/drupal-digests-ai-development-tracking
- Dries Buytaert launched Drupal Digests for tracking AI development progress

---

## Acquia Nebula as Canvas Template
- **Issue:** https://www.drupal.org/project/canvas/issues/3571591
- Set acquia/nebula as recommended template in @drupal-canvas/create
- **GitHub:** https://github.com/acquia/nebula

---

## ngxtm/devkit — Cross-Platform Skills System

**URL:** https://github.com/ngxtm/devkit
**NPM:** @ngxtm/devkit

### Stats
- 414+ skills, 38 agents, 57 commands
- MIT license
- 4 stars, 107 commits, 35 releases (latest v3.21.0, Feb 2026)

### Installation Modes
| Mode | Command | Size |
|------|---------|------|
| Index-only | `devkit install` | ~30KB (recommended) |
| Minimal | `devkit install --minimal` | ~2MB |
| Category | `devkit install -c=react,ts` | varies |
| Full | `devkit install --full` | ~59MB |

### Features
- Smart tech detection (auto-detects project stack)
- 99.95% context reduction in index-only mode
- Auto-sync via GitHub Actions
- Per-project installation
- Coding level 0-5 (ELI5 to God mode)
- Multi-tool: Claude Code, Cursor, Copilot, Gemini

### Skill Categories
React (9), TypeScript (4), Node (6), Security (5), Mobile (5), Backend (6), Database (5), DevOps (7), Testing (6), AI (6), Frontend (6), Tools (6)

### Relevance to Drupal
- No Drupal-specific skills found in the catalog
- Architecture pattern is applicable: could host Drupal skills as a category
- Listed on LobeHub Skills Marketplace
