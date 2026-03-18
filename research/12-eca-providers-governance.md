# ECA + AI Integration, Provider Landscape, Governance & Specialized Topics

## ECA (Event-Condition-Action) + AI Integration

### AI Integration - ECA Module
- **URL:** https://www.drupal.org/project/ai_integration_eca
- **Version:** 1.0.0-rc3 (December 12, 2025)
- **Install:** `composer require 'drupal/ai_integration_eca:^1.0@RC'`
- **Sites using:** 153
- **Maintainers:** jurgenhaas, lammensj (creator), marcus_johansson

### How It Works
Integrates AI capabilities with ECA framework, enabling AI operations as actions within ECA models:
- Chat operations
- Moderation operations
- TextToSpeech operations
- Additional AI operation types

### Setup
1. Enable the module
2. Access an ECA model
3. Incorporate AI operation type as action

### ECA Base Module
- **URL:** https://www.drupal.org/project/eca
- **Version:** 3.0.11 (stable, March 10, 2026)
- **Version:** 3.1.0-beta1 (Drupal 11.3+/12.0+)
- **Modeller:** BPMN.iO (JavaScript visual tool in Drupal admin)
- **Docs:** https://ecaguide.org/
- Features: Plugin managers, context stack, caching, loops, logging, recursion prevention, 20+ sub-modules

### DrupalCon Session
- **"ECA, AI and MCP: Connecting Context, Intelligence and Action"** — Vienna 2025
- **URL:** https://events.drupal.org/vienna2025/session/eca-ai-and-mcp-connecting-context-intelligence-and-action

---

## AI Provider Landscape

### Provider Count
**48+ providers** integrated via the AI module
- **Full list:** https://new.drupal.org/ai/about-drupal-ai/providers

### Major Provider Modules on drupal.org
| Module | Provider | URL |
|--------|----------|-----|
| ai_provider_acquia | Acquia AI Gateway | drupal.org/project/ai_provider_acquia |
| ai_provider_anthropic | Anthropic (Claude) | drupal.org/project/ai_provider_anthropic |
| ai_provider_openai | OpenAI (GPT) | drupal.org/project/ai_provider_openai |
| ai_provider_ollama | Ollama (local) | drupal.org/project/ai_provider_ollama |
| ai_provider_deepseek | DeepSeek | drupal.org/project/ai_provider_deepseek |
| ai_provider_google_vertex | Google Vertex AI | drupal.org/project/ai_provider_google_vertex |
| gemini_provider | Google Gemini | drupal.org/project/gemini_provider |

### Additional Providers (integrated via AI module)
- amazee.io
- AWS Bedrock
- Azure OpenAI
- Hugging Face
- Mistral
- OpenRouter (https://openrouter.ai/)
- Groq (https://docs.litellm.ai/docs/providers/groq)
- LiteLLM proxy (https://docs.litellm.ai/docs/providers)
- And 35+ more

### Ollama Setup Guide
- **TheDropTimes:** https://www.thedroptimes.com/50560/set-ollama-free-local-ai-provider-in-your-drupal-ddev-environment
- **Docs:** https://project.pages.drupalcode.org/ai/1.0.x/modules/providers/provider_ollama/

---

## AI Observability & Monitoring

### Langfuse Module
- **URL:** https://www.drupal.org/project/langfuse
- **What it does:** AI agent observability, tracing & evaluation for Drupal
- **Langfuse Platform:** https://langfuse.com/docs
- **Features:**
  - Token and cost tracking: https://langfuse.com/docs/observability/features/token-and-cost-tracking
  - Application tracing: https://langfuse.com/docs/observability/overview
  - Advanced SDK features: https://langfuse.com/docs/observability/sdk/advanced-features
- **Relevance:** HIGH — essential for production AI monitoring

### AI Dashboard
- Shipped with Drupal CMS 2.0
- Central hub for managing AI features and providers
- Issue tracking: https://www.drupal.org/project/ai_dashboard/issues/3558691

---

## Vector Database Support

### Milvus VDB Provider
- **URL:** https://www.drupal.org/project/ai_vdb_provider_milvus
- **Description:** Milvus vector database integration

### PostgreSQL Vector Support
- **Guide:** https://opensenselabs.com/blog/drupal-ai-module/drupal-ai-search-with-postgresql

### Vector Database Overview
- **TheDropTimes:** https://www.thedroptimes.com/64433/unlocking-ai-search-in-drupal-practical-guide-vector-database-modules
- **Droptica guide:** https://www.droptica.com/blog/recommended-vector-databases-vdb-drupal-overview-ai-providers/

---

## AI Content & Multimodal

### Content Strategy with AI
- **Alt text + Content Strategy:** https://www.droptica.com/blog/how-generate-image-alt-text-and-content-strategy-ai-modules-drupal/
- **AI Automators content creation:** https://www.thedroptimes.com/66189/how-droptica-uses-ai-automators-and-field-widget-actions-streamline-drupal-content-creation

### Multimodal Capabilities
- **Audio field automators** (new in AI module 1.3 sprint)
- **Image processing** (alt text generation, content analysis)
- **Gemini multimodal** via Gemini Provider: https://www.thedroptimes.com/66914/gemini-provider-101-rc1-drupal-ai

### Translation AI
- **10 Translation Modules:** https://www.thedroptimes.com/56086/10-ai-powered-translation-modules-drupal
- **QED42 guide:** https://www.qed42.com/insights/drupal-ai-translation-modules-a-smarter-way-to-translate-content

---

## AI Security

### SA-CONTRIB-2026-028
- **URL:** https://www.drupal.org/sa-contrib-2026-028
- **Module:** AI (Artificial Intelligence)
- **Severity:** Moderately critical
- **Type:** Information Disclosure
- **Status:** Patched
- **Takeaway:** AI modules need security review — this was the first significant advisory

---

## Claude Agent SDK for Drupal (Experimental)

### Module
- **URL:** https://www.drupal.org/project/ai_claude_agent_sdk
- **Description:** VERY EXPERIMENTAL — Claude Code runtime integration with Drupal
- **Coverage:** https://www.thedroptimes.com/66161/experimental-claude-agent-sdk-integrates-claude-code-runtime-with-drupal
- **Relevance:** Forward-looking — bridges Claude Code agent capabilities directly into Drupal

---

## Background Agents

### Issue: PoC for Background Agents
- **URL:** https://www.drupal.org/project/ai/issues/3560792
- **Description:** Create PoC demo of Background agents and state machine approach
- **Relevance:** HIGH — one of the 8 core capabilities in the 2026 roadmap

---

## AI Governance

### Context Control Center
- Evolved from config entities to content entities
- Revision management and targeting capabilities
- Part of the 4-week sprint deliverables

### Drupal AI Philosophy
- "Human expertise over technological replacement"
- "Collaboration — amplifying expertise rather than replacing it"
- Content permissions and human oversight built into agent framework
- Advanced governance planned: batch approvals, branch-based versioning, audit trails

---

## CKEditor AI Integration

### CKEditor 5 Premium Features
- **URL:** https://www.drupal.org/project/ckeditor5_premium_features
- **AI Assistant docs:** https://www.drupal.org/docs/extending-drupal/contributed-modules/contributed-module-documentation/ckeditor-5-premium-features/feature-guide/ai-assistant
- **ImageX blog:** https://imagexmedia.com/blog/ai-assistant-collaboration-premium-ckeditor-5-features-drupal

### AI CKEditor (Free Alternative)
- **URL:** https://www.drupal.org/project/ai_ckeditor
- **QED42 guide:** https://www.qed42.com/insights/smarter-content-editing-in-drupal-exploring-the-ai-ckeditor-module

---

## Drupal AI Ecosystem Summary Articles

- **30 Modules (DrupalForge):** https://www.drupalforge.org/blog/drupal-ai-landscape-30-frameworks-integration-modules-you-should-know
- **Optasy overview:** https://optasy.com/blog/summary-ai-tools-available-drupal-ecosystem
- **Tactis overview:** https://www.tactis.com/articles/blog/exploring-drupals-ai-ecosystem-essential-modules-and-tools
- **Drupfan ecosystem:** https://drupfan.com/en/blog/drupal-ai-modules-ecosystem-chatbots-ai-agents
- **Drupal at your Fingertips:** https://www.drupalatyourfingertips.com/ai
