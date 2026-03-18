# DrupalCon Chicago 2026, Surge Module & AI Skills Module

## DrupalCon Chicago 2026 (March 23-25, 2026) — AI Sessions

**21+ AI-specific sessions across 3 days — largest AI focus of any DrupalCon.**

### Monday March 23: Full-Day AI Summit
- AI Strategic Initiative Panel (Jamie, Matthew, Glenn)
- "Innovation from Within: Drupal, AI, and Internal Expertise"
- "The Human Edge in AI Content"
- Scott Falconer: "A Practical Framework for AI Success in Drupal"
- Sponsor case studies from Acquia, Four Kitchens, CKSource
- Ethics/governance breakout sessions

### Tuesday March 24: Key AI Sessions
| Session | Speaker | Topic |
|---------|---------|-------|
| Agent Experience (AX) and AI-driven Drupal | scott-falconer | AGENTS.md, CLI tools, "Agent Skills" as infrastructure |
| Strategic Evolution + Orchestration | yautja_cetanu | Canvas AI, visual workflow, ECA + Tools API + MCP |
| Context is Everything | Kristen Pol, afoster | Content Control Center + Canvas AI + markdown context |
| Exposing Drupal Content to LLMs with MCP | eojthebrave | Custom MCP servers, RAG, action execution |
| Stop Building AI Features | (unnamed) | "AI as your audience" — infrastructure over features |
| Building AI-Powered Drupal Applications | breidert | Hands-on workshop: AI module through RAG |

### Wednesday March 25: Key AI Sessions
| Session | Speaker | Topic |
|---------|---------|-------|
| Beyond Chatbots: AG-UI | aaronchristian | Component-based AI in content, not popups |
| 10 Ways to Learn AI in Drupal | salimlakhani, darren oh | 13+ working templates |
| KEYNOTE: Drupal CMS Spotlights | Hojtsy, Pol, scott-falconer | Latest CMS + AI Initiative |
| Migrate Smarter: D7-to-D11 | marco | 15-year-old site AI migration |
| Drupal AI Initiative: Year in Review | pdjohnson, domidc, breidert | Critical retrospective + AMA |
| AI Agents for Site Builders | marcus_johansson | No-code agent framework, MCP |
| Beyond Chunk and Pray: Smarter RAG | vincenzo gambino | Hybrid retrieval, re-ranking |

### New Concepts Emerging at DrupalCon
- **Agent Experience (AX):** AI agents as distinct user type needing dedicated UX
- **AG-UI:** Component-based toolkit embedding AI into content (not popups)
- **"AI as Your Audience":** Open source should expose infrastructure to AI, not build features
- **Orchestration:** Combining intelligent AI agents with deterministic actions (ECA + Tools API + MCP)

---

## Drupal Surge Module (AI Coding Starter Kit)

**URL:** https://www.drupal.org/project/surge
**Status:** Development (1.0.x-dev, updated Feb 2026)
**Author:** ronaldtebrake

### What It Does
- Aggregates Agent Skills from multiple sources
- Generates coding standards compatible with: Claude Code, Cursor, Aider, Gemini CLI, PhpStorm
- Scans projects and compiles AGENTS.md as single source of truth
- Aggregates skills into `.claude/skills/` directory

### Commands
- `composer surge-standards` — Apply coding standards
- `composer surge-scan` — Dry run/scan project

### Significance
This is the closest implementation to the community's "one-command setup" goal. Directly addresses the AI Coding Starterkit proposal (#3541110).

---

## Agentic Skills Module (drupal.org)

**URL:** https://www.drupal.org/project/ai_skills
**Spec:** agentskills.io
**Status:** Experimental

### 3 Official Skills
1. **coding-standards** — Drupal coding standards enforcement
2. **issue-queue** — Drupal.org issue queue workflow
3. **contribute-fix** — Contribution workflow (from scottfalconer)

### Key Issue #3565489: First-Class Agent-Skills Support
- Proposes modules should include `skills/` folder versioned with code
- "Share good defaults via libraries/packages, allow projects to customize/override/extend"

### Issue #3569130: Directory Rename
- Renamed from `.claude/skills/` to just `skills/` to be tool-agnostic
- Reflects broader community shift toward agent-agnostic skill storage

### Installation Methods
- Via `skills.sh`: `npx skills add`
- Via Drupal Surge: `composer surge-standards`
- Via manual copy to `.claude/skills/` or `.agents/skills/`

---

## Omedia/drupal-skill (NEW — not previously cataloged)

**URL:** https://github.com/Omedia/drupal-skill
**Skills:** 3 (frontend, backend, tooling)
**Structure:** Separate directories with `references/` and `assets/`

---

## nonzod/drupaldev-claude-skill (NEW — not previously cataloged)

**URL:** https://github.com/nonzod/drupaldev-claude-skill
**Structure:** Organized by language:
```
coding_standards/
├── accessibility/
├── composer/
├── css/
├── javascript/
├── markup/
├── php/
├── spelling/
├── sql/
├── twig/
└── yaml/
```

---

## Bloomidea/drush-mcp (NEW — March 2026)

**URL:** https://github.com/Bloomidea/drush-mcp
**Tools:** 17 exposed via Drush
**Capabilities:** Entity CRUD, discovery/introspection, cache/watchdog/config management, PHP eval, SQL queries
**Transports:** Local, SSH, Docker
**Multi-site support:** Yes
**Compatible:** Claude Code, Cursor, Codex, Gemini, Windsurf

---

## Context7 MCP + Drupal Documentation

Context7 serves Drupal documentation with these library IDs:

| Library | ID | Snippets | Score |
|---------|-----|----------|-------|
| Drupal | /drupal/drupal | 211 | 56.8 |
| Selwyn Polit d9book | /selwynpolit/d9book | 1,989 | 75.3 |
| Drupal Core | /drupal/core | 97 | -- |
| UI Patterns 2 | /websites/project_pages_drupalcode_ui_patterns | 137 | 42.4 |

The d9book library (1,989 snippets, 75.3 score) is the same source bundled by grasmash/drupal-claude-skills.

---

## AI Module Security Advisory Detail

**SA-CONTRIB-2026-028** (March 11, 2026)
- **Vulnerability:** Rendering AI-generated HTML/Markdown in preview could expose secret LLM communications (system prompts, context data)
- **CVSS:** 11/25 (Moderately Critical)
- **Affected:** AI Automators, AI Translate, AI API Explorer, AI Content Suggestions
- **Fixed:** v1.1.11, v1.2.12
- **Lesson:** AI integration creates novel attack surfaces (prompt injection through rendered output)

---

## AI for WCAG/Accessibility

| Module | Installs | Purpose |
|--------|----------|---------|
| editoria11y | 21,155 | Real-time a11y checker, "Fix with AI" button |
| ai_image_alt_text | 7,231 | Vision model alt text generation |
| ai_accessibility | 3 | MVP: axe-core + ChatGPT |
| media_accessibility_audit | -- | Alt text review with confidence indicators |
| autoalt | -- | Bulk alt text generation |

---

## The Ban Debate (#3574093)

Issue "Ban LLM code contributions" is "Needs review":
- **catch** documented 3 specific cases of wasted reviewer time on AI-generated code
- Middle-ground proposals: moratoriums for core, contrib sets own policies
- Community leaning toward guardrails + quality gates, not blanket bans
