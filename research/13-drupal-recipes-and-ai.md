# Drupal Recipes as AI Distribution Mechanism

## What Are Drupal Recipes?

Drupal Recipes are a configuration distribution mechanism that allows pre-packaged sets of modules, configuration, and content to be applied to a Drupal site.

- **Docs:** https://www.drupal.org/docs/extending-drupal/drupal-recipes
- **Cookbook:** https://www.drupal.org/docs/extending-drupal/contributed-modules/contributed-module-documentation/distributions-and-recipes-initiative/recipes-cookbook
- **Browse recipes:** https://new.drupal.org/browse/recipes
- **Part of:** Drupal Starshot initiative: https://www.drupal.org/about/starshot

## AI-Specific Drupal Recipes

### Drupal CMS AI Recipe (Core)
- **Part of:** Drupal CMS 2.0
- **What it installs:**
  - AI Core, AI Agents, AI Dashboard
  - AI Image Alt Text
  - Anthropic Provider, OpenAI Provider
  - Drupal Canvas (visual site building)
  - Key module (secure API credentials)
- **Features:** Alt text generation, AI-powered chatbot for site building
- **Requires:** API key from OpenAI or Anthropic
- **Version:** 2.0.0 (Jan 28, 2026), 2.1.0-beta1 (Mar 13, 2026)

### AI Chatbot Recipe
- **URL:** https://www.drupal.org/project/ai_chatbot_recipe
- **Maintainer:** koppie
- **Description:** No-code solution for implementing an AI chatbot with RAG capabilities
- **Version:** 1.16.0 (Sept 27, 2025)
- **Features:**
  - RAG (Retrieval-Augmented Generation) capable
  - Key module for secure credential management
  - Input modules for configuration
- **Install:** `drush recipe ../recipes/ai-chatbot-recipe`
- **Requires:** OpenAI + Pinecone API keys

### AI LLM Optimized Content Recipe
- **URL:** https://packagist.org/packages/drupal/ai_recipe_llm_optimized_content
- **Description:** Recipe for LLM-optimized content structures

### Pronovix llms.txt Recipe
- **URL:** https://www.thedroptimes.com/49424/pronovix-releases-drupal-recipe-llmstxt-support-ai-ready-content
- **Author:** Pronovix
- **Description:** Drupal Recipe for implementing llms.txt standard
- **Purpose:** Make developer portals AI-agent-ready
- **Related:** https://pronovix.com/articles/make-your-developer-portal-ready-ai-agents

---

## Drupal-AI/ddev-drupal-ai Recipe Integration (Issue #3)

**URL:** https://github.com/Drupal-AI/ddev-drupal-ai/issues/3
**Created by:** robertoperuzzo (Aug 19, 2025)
**Status:** Open

### Problem
Current `ddev drupal-ai setup` wizard only installs modules without configuration. Users must manually:
- Configure each AI module
- Set up content types and custom fields
- Configure search indexes and vector storage
- Apply security permissions

### Proposed Solution
Create Drupal recipes for each AI functionality:
1. **Vector search** with Search API and pgvector
2. **Content generation** with editorial workflows
3. **Image analysis** with media handling
4. **Q&A systems** with knowledge bases
5. **Code assistants** with snippet management
6. **Document processing** with extraction workflows

Enhanced `functionalities.yaml` to reference recipes alongside modules, with config overrides for environment-specific settings.

### Relevance
HIGH — This is the missing piece: using Drupal Recipes to distribute complete AI configurations, not just module lists.

---

## How Drupal CMS Uses Recipes for AI

- Drupal CMS (Starshot) installs AI features via recipes
- Recipes handle module installation + configuration + permissions in one step
- Blog: https://www.drupal.org/blog/drupal-cms-20-is-here-visual-building-ai-and-site-templates-transform-drupal
- Review: https://dev.to/victorstackai/review-drupal-cms-starshot-recipe-system-for-ai-driven-site-building-4kn0

---

## Recipes + AI Migration
- **Blog:** https://www.valuebound.com/blog/drupal-migration-made-easy-recipes-and-ai-tools
- Combining Drupal Recipes with AI tools for easier migrations

---

## Assessment

Drupal Recipes are a **critical distribution mechanism** for AI tooling:
1. The core Drupal CMS AI recipe already bundles AI modules + providers + Canvas
2. The AI Chatbot Recipe provides a complete RAG chatbot setup
3. The ddev-drupal-ai issue #3 proposes recipes for each AI functionality
4. Pronovix demonstrates recipes for llms.txt
5. Recipes could distribute AI agent configurations (not just modules)

### Gap
No recipe exists yet for the **developer tooling side** (DDEV plugins, SKILL.md files, MCP servers, AGENTS.md). The "AI Coding Starterkit" proposal could leverage recipes for the site-facing parts and a separate mechanism (DDEV addon, Composer package) for the development tools.
