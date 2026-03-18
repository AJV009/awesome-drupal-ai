# Final Niche Findings: Usage Stats, Core Issue, Module Upgrader

## Drupal AI Module Usage Statistics

**As of March 2026:**
- **13,293 reported installations** — substantial adoption
- **195 project stars** on drupal.org
- **16 maintainers** (including marcus_johansson, yautja_cetanu, kevinquillen)

### Current Releases
| Version | Date | Drupal Compatibility |
|---------|------|---------------------|
| 1.3.0 | March 12, 2026 | ^10.5 \|\| ^11.2 |
| 1.2.12 | March 11, 2026 | ^10.4 \|\| ^11 |
| 1.1.11 | March 11, 2026 | ^10.2 \|\| ^11 |
| 2.0.x-dev | Active | Next major |

### Submodules Included
- AI Core (provider access, model integration)
- AI Explorer (admin testing interface)
- AI Automators (field population, workflow chains)
- AI Search (semantic search, vector databases)
- AI Assistants & Chatbot framework
- CKEditor integration
- Content assistance tools
- Translation, validation, moderation capabilities

---

## Drupal Core Issue #3570498: AI Tools for Contributors and Maintainers

**URL:** https://www.drupal.org/project/drupal/issues/3570498
**Status:** Active
**Reporter:** Dries Buytaert
**Created:** January 30, 2026
**Updated:** March 12, 2026

### Purpose
Collecting community experiences with AI tools for:
1. **Contributors:** patch writing, error detection, documentation, testing
2. **Maintainers:** code review, issue triage, bug identification, quality checks

### Notable Community Discussion

**Positive Use Cases:**
- **Scott Falconer:** Agent skills that search Drupal.org for similar issues before proposing patches — prevents redundant work
- **Ronald te Brake:** CodeRabbit for code review — "quality getting better and better", identifies bugs as preliminary screening
- **Jonathan Shaw:** Skill for searching Drupal.org GitLab across contrib projects for code examples

**Concerns:**
- **nod_:** Algorithmic bias in LLM-assisted credit attribution — blogged about "algorithmic bias against Drupal community values"
- **catch:** Issue credit assignment takes 30s-30min per issue; LLMs with 60% accuracy "helps exactly 0% because I would have no idea what is the 60% correct"
- **dww:** Environmental and ethical concerns (energy, job displacement, democracy impacts) — references Larry Garfield's "Selfish AI" blog

**Policy Proposals:**
- **spec0:** Bayesian framework for measuring AI code quality/reliability as git hook or pipeline

### Significance
This is the **official Drupal core issue** for AI tooling policy. Any "standard" recommendations should align with the community consensus forming here. The discussion shows both enthusiasm and significant concerns that need to be addressed.

---

## Gábor Hojtsy: AI-Assisted Drupal Module Upgrader Revival

**URL:** https://www.hojtsy.hu/blog/2026-mar-07/my-experiment-bringing-drupal-module-upgrader-back-dead-less-24-hours
**Date:** March 7, 2026

### Background
Drupal Module Upgrader (DMU) — created 2014, abandoned due to PHP 8 compatibility issues with Pharborist library.

### AI Tool Used
Claude Code

### Process
1. Fed Andy Fowlston's unmerged PR to Claude Code → "thorough code review that looked great on human scan"
2. Claude Code fixed bugs and expanded test coverage
3. Produced "full green Pharborist test run ready for PHPUnit 12 — in just a few hours"
4. Resolved dependencies and deprecation notices
5. Updated DMU for Drupal 10 and 11
6. Updated transformations to produce Drupal 10/11 code instead of D8/D9

### Result
**DMU 2.0.0-alpha2 released within 24 hours**, fully functional, complete test suite passing.

### Key Quote
"Modern tools can be used to save precious work created by very caring humans" — LLMs effectively complement deterministic tools for legacy code modernization.

### Significance
Demonstrates AI can **revive abandoned Drupal tools** — not just write new code but resurrect and modernize existing community work. Directly relevant to the "ways to contribute to Drupal using AI" research goal.

---

## Drupal Core AI Context Files

### Current State
- **No CLAUDE.md or AGENTS.md in Drupal core** as of March 2026
- Issue #3570498 is the discussion where this might be proposed
- Jacob Rockowitz (jrockowitz.com) has specifically advocated for an AGENTS.md in Drupal core

### Gap
This is a **significant gap** — Drupal core lacks AI context files that would help AI tools generate better Drupal-conforming code. The Starterkit proposal (#3541110) and the core issue (#3570498) are the active discussions.

---

## Summary of Unique Data in This File

| Finding | Value |
|---------|-------|
| drupal/ai has 13,293 installations | Quantifies adoption |
| 16 maintainers on AI module | Shows community investment |
| Latest release: v1.3.0 (Mar 12, 2026) | Very active development |
| Core issue #3570498 by Dries | Official policy discussion |
| Community split on AI usefulness | Important for recommendations |
| DMU revived in 24 hours with AI | Concrete AI contribution example |
| No CLAUDE.md in Drupal core | Key gap to address |

---

## Related AI Module Installation Statistics

| Module | Installations | Purpose |
|--------|-------------|---------|
| AI (drupal/ai) | 13,293 | Core AI framework |
| CKEditor 5 Premium (with AI) | 13,180 | AI writing in editor |
| AI Image Alt Text | 7,231 | AI-generated alt text |
| TMGMT DeepL | 3,335 | Neural machine translation |
| Smart Content | 666 | Rules-based personalization (no AI) |
| AI Translate | 237 | AI-powered translation |
| AI Search | 51 | Semantic vector search |
| AI Accessibility | 3 | WCAG scanning + AI suggestions |

### Growth Context
13,293 installs in ~18 months is exceptional. Comparisons:
- Editoria11y (accessibility): 21,155 sites (5+ years)
- TMGMT (translation): 11,088 sites (14 years)
- GraphQL: 6,859 sites (11 years)
- Next.js for Drupal: 3,402 sites (3+ years)

---

## Ban LLM Contributions Debate — Key Arguments

### Issue #3574093: "Ban LLM Code Contributions"
- **Proposed by:** ghost of drupal past (Feb 17, 2026) — Status: Needs review

**FOR a ban:**
- **catch (core committer):** 3 specific cases — 5,000-line MR reimplemented existing functionality; 4,500-line MR generated 121 review comments; phantom bug report consumed committer time
- **nicxvan:** "Burden of proof of utility is on the new tool." Banning now easier to reverse than extracting thousands of problematic lines
- **dww:** Environmental destruction, exploited labor, surveillance concerns transcend code quality
- **phenaproxima:** Quality and trust built over decades matter more than convenience

**AGAINST a ban:**
- **scott falconer:** Banning based on quality "resembles aiming for high writing standards by banning keyboards"; CI already filters poor work
- **aporie:** Detection is imperfect; newcomers using AI might become skilled developers
- **scott falconer:** LLMs may enable people with cognitive disabilities to contribute meaningfully

**Middle ground:**
- **cainaru:** Moratorium on LLM contributions to core (revisited periodically), allow contrib own policies
- **aporie:** AI-detection tagging, "AI-assisted coder" roles for trusted developers

---

## AI in Drupal CI Pipeline — Status

No dedicated AI-powered CI pipeline in Drupal core as of March 2026. However:
- **Issue #3562505** proposed "Prototype automated AI review pipeline" (404 — restricted/early)
- **spec0's proposal** in #3570498: Bayesian analysis as git hook for semantic verification
- **CodeRabbit** used informally by some contributors (Ronald te Brake) as pre-review screening
- DrupalCI remains focused on PHPUnit, PHPStan, code standards — no AI integration at infra level

---

## WCAG Accessibility + AI Modules

| Module | Installs | WCAG Coverage |
|--------|----------|---------------|
| Editoria11y + AI submodule | 21,155 | Real-time a11y checking, "Fix with AI" button |
| AI Image Alt Text | 7,231 | WCAG 1.1.1 (Non-text Content) |
| AI Accessibility | 3 | axe-core scanning + ChatGPT suggestions (MVP) |

---

## AI Personalization in Drupal — Gap Analysis

- **Acquia Lift:** EOL as of Jan 31, 2026 (replaced by VWO with no AI)
- **Smart Content:** 666 installs — rules-based, NOT AI-powered
- **Personalization module:** 3 installs — geolocation/taxonomy scoring, no AI
- **AI Automators:** Can be used for personalization workflows but not purpose-built
- **Gap:** No dedicated AI personalization module exists combining behavioral data with LLM-powered content adaptation

---

## Headless/Decoupled Drupal + AI Pattern

Emerging architectural pattern:
```
[Drupal Backend]
  - drupal/ai (provider abstraction)
  - AI Search (vector embeddings via Search API)
  - AI Automators (content enrichment on save)
  - JSON:API / GraphQL (expose enriched content)
       |
       v
[Decoupled Frontend (Next.js, React, etc.)]
  - Consumes AI-enriched content via API
  - Frontend chatbot calls Drupal's AI assistant endpoints
  - Semantic search powered by Drupal's vector index
```
No dedicated "headless AI" module, but drupal/ai + Search API + JSON:API creates a functional stack.

---

## EU Translation Gap

- No `tmgmt_etranslation` or `oe_translation` modules found on drupal.org (404)
- EC's DGT eTranslation service covers 24 EU languages but no public Drupal integration module
- EC likely uses private/internal integration code not on public registry
- **Poetry** module (historical DGT connector) also 404 — maintained in EC private repos
