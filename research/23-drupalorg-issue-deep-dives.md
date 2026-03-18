# Deep Dive: Drupal.org Issue Queue Discussions on AI

## Issue #3541110: AI Coding Starterkit

**URL:** https://www.drupal.org/project/ai_initiative/issues/3541110
**Status:** Active | **Reporter:** ronaldtebrake | **Created:** Aug 13, 2025

### Problem Statement
Drupal lacks unified AI dev experience vs Laravel Boost. Solutions fragmented across Claude Code module, MCP servers, Cursor rules.

### Proposed Solution
Tool-agnostic AI starter kit with: version-specific docs, coding standards, optional MCP server, infrastructure-independent, easy config file integration.

### Discussion Thread
- **jphelan:** "+1 would love to see something like Boost for Drupal"
- **breidert (1xINTERNET):** "Sounds interesting"
- **ronaldtebrake:** Started building at Surge project (drupal.org/project/surge)
- **andypost:** Referenced Linux kernel MCP implementation as model
- **prashant.c:** "This would be extremely helpful" (from LinkedIn discovery)
- **pdjohnson:** Suggested following Drupal CMS documentation model with curated, branded docs
- **andypost:** Referenced GitHub's spec-kit tool for cross-agent integration
- **jcorrego (Jan 2026):** "I would use this for sure. Already looking at your doc MCP as a start."

### Current Status
Active but unassigned. Surge module is the primary implementation. Community supportive but no formal assignment yet.

---

## Issue #3565489: First-Class Support for Agent-Skills

**URL:** https://www.drupal.org/project/ai/issues/3565489
**Status:** Active | **Priority:** Major | **Reporter:** fago | **Created:** Jan 3, 2026

### Proposal: 7 Key Areas
1. **Scope:** Development and site-building contexts
2. **Portability:** Independent of project setup (DDEV, Lando, Docker)
3. **Aggregation:** Centralized skill collection for agent discovery
4. **Best Practices:** Defaults via packages, allow customization
5. **Module Integration:** `skills/` folders within modules, auto-versioned
6. **Vendor Independence:** Test across multiple agents, not just Claude
7. **Specialized Skills:** Domain tools for docs, config, issue management

### Key Discussion
- **yautja_cetanu:** "I've seen multiple people try different skill libraries. Find some place to collect them all!"
- **ronaldtebrake:** Demonstrated PoC that dynamically composes AGENTS.md based on environment (DDEV/Lando/Docker detection). Skills exist at multiple levels: within modules (Commerce, Canvas) and as shared libraries.

### Significance
This would make Drupal the first CMS with native agent-skills support in its module system.

---

## Issue #3568936: Add AGENTS.md to Drupal Core

**URL:** https://www.drupal.org/project/drupal/issues/3568936
**Status:** Closed (works as designed) | **Reporter:** nod_ | **Created:** Jan 22, 2026

### Why It Was Created
LLM tools generate low-quality contributions. AGENTS.md would guide AI to follow proper contribution workflows, coding standards, DDEV usage, modern JS practices.

### Key Discussion Points

**Support (lauriii):**
- Elevated to Major priority
- "Essential infrastructure for relevance"
- AGENTS.md as "executable documentation" forcing maintainers to keep guidelines current
- AI-generated code should be treated as personally responsible work

**Skepticism (catch):**
- "We generally have not had drive-by LLM-generated MR spam against core"
- Real problems: unreviewed vibe-coded MRs, LLM-generated issue reviews adding verbosity
- Concerns that AGENTS.md "encourages problematic submissions rather than preventing them"

**Technical proposals (andypost):**
- Referenced LLVM's AI tool policy
- curl's PR enforcement of disclosure
- AGENTS.md as policy enforcement mechanism

### Why It Was Closed
Reporter (nod_) reversed position, citing personal concerns about "addictive tool mechanics." Closed as "works as designed" — no patches merged.

### Community Alternative
amazeeio/drupal-agents-md and Droptica's template serve as external alternatives.

---

## Issue #3570498: AI Tools for Contributors and Maintainers

**URL:** https://www.drupal.org/project/drupal/issues/3570498
**Status:** Active | **Reporter:** dries | **Created:** Jan 30, 2026

### What Dries Asked
Collecting experiences from contributors using AI in two categories:
1. Tools helping **contributors** (patches, testing, docs)
2. Tools helping **maintainers** (review, triage, quality checks)

### Detailed Comment Analysis

**scott-falconer (#2):**
- Agent skills can guide AI behavior — skill directs agents to check drupal.org for similar issues first
- Warns against autonomous patch submission — would overwhelm maintainers
- Proposes future "ready for agent review" stage where another dev's agent tests patches

**ronaldtebrake (#4):**
- Using CodeRabbit for reviews: "even our ai skeptics are now very happy"
- Quality improving, catching bugs effectively
- Working on Surge starterkit and skills standardization

**jonathanshaw (#5):**
- Suggested Slack channel for AI tooling
- Shared skill.md enabling AI search across drupal.org GitLab for code examples across ALL contrib projects

**ghost of drupal past (#6):**
- Environmental destruction, democratic harm, ethical concerns
- Cited AGENTS.md as proper response

**spec0 (#7):**
- Proposed Bayesian framework for quality/reliability metrics
- Uploaded besian-ai-stats.zip demonstrating concept
- "Similar to git hooks and pipeline steps"

**cmlara (#8):**
- Linked to related AI policy issue #3565917

### Community Sentiment
Split between enthusiastic adopters (scott-falconer, ronaldtebrake, jonathanshaw) and concerned skeptics (catch, ghost of drupal past, dww). Middle ground emerging around quality gates and guardrails.

---

## Issue #3574093: Ban LLM Code Contributions

**URL:** https://www.drupal.org/project/drupal/issues/3574093
**Status:** Needs review

### Key Arguments
**For ban (catch):**
- Documented 3 specific cases of wasted reviewer time
- 60% accuracy "helps exactly 0%" because can't identify which 60% is correct

**Against ban:**
- Middle-ground proposals: moratoriums for core, contrib sets own policies
- Quality gates preferred over blanket bans
- Community leaning toward guardrails + evaluation frameworks

---

## Drupal Community AI Survey Data

**From DrupalCon Vienna 2025:**
- **79.2% of community members using AI daily** (from event surveys/discussions)
- No formal published survey found, but this stat was referenced in multiple blog posts

---

## Matt Glaman's Blog

**URL:** mglaman.dev

### AI-Related Post Found
- **"AI workflows will reshape development organizations"** (Nov 27, 2025) — Reflections on what AI means for software engineers

### drupalorg-cli 0.8.0 (March 3, 2026)
- Added GitLab issue fork and merge request commands
- Explicitly designed to be "useful for developers using AI agents to assist with Drupal.org issues"
- This is the tool that scottfalconer/drupal-contribute-fix depends on
