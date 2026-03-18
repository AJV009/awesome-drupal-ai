# Final Niche Gap-Filling: Commerce, Moderation, Image Gen, Adaptable Modules

## Dries Buytaert: Claude Code Meets Drupal

**URL:** https://dri.es/claude-code-meets-drupal
- 30-minute session, didn't touch IDE once
- Tasks: custom Drush command, constructor refactoring, annotation-to-attribute conversion
- "I expected mixed results but was surprised by how useful it proved to be"
- Video demonstration created
- Strong signal from Drupal founder endorsing Claude Code

## Dries Buytaert: Adaptable Modules

**URL:** https://dri.es/adaptable-drupal-modules-code-meant-to-be-adapted-not-installed
**Coverage:** https://www.thedroptimes.com/65265/dries-proposes-adaptable-modules-ai-ready-drupal-code-sharing
- New concept: site-specific, tested code that others reuse and MODIFY using AI
- AI tools analyze module architecture, understand embedded decisions, regenerate adjusted versions
- Paradigm shift from "install and configure" to "adapt and customize"
- Directly relevant to how AI will change Drupal module ecosystem

## Dries Buytaert: AI Creates Asymmetric Pressure on Open Source

**URL:** https://dri.es/ai-creates-asymmetric-pressure-on-open-source
- AI amplifies contributions but also enables low-quality submissions
- Referenced in issue #3570498 ("AI tools for contributors and maintainers")

---

## Drupal Commerce + AI

### AI Commerce Module
- **URL:** https://www.drupal.org/project/ai_commerce
- **Description:** AI-specific module for Drupal Commerce
- **Relevance:** Direct intersection of ecommerce and AI

### Centarro's AI Exploration
- **URL:** https://www.centarro.io/blog/exploring-ai-accelerate-drupal-commerce-development
- **Description:** Exploring AI to accelerate Drupal Commerce development using Cursor and AI tools
- **Quote from Ryan Szrama (Centarro):** "We've opened the door internally for more experimentation with IDEs, models, and other tools that don't replace the developer but augment his or her ability"

---

## AI Content Moderation in Drupal

### AI Comment Moderation Module
- **URL:** https://www.drupal.org/project/ai_comment_moderation
- **Description:** AI-powered comment moderation
- **Relevance:** Automated content governance

### Droptica Guide
- **URL:** https://www.droptica.com/blog/how-set-automatic-ai-content-moderation-drupal-modules-and-examples/
- **Also on Medium:** https://droptica.medium.com/how-to-set-up-automatic-ai-content-moderation-in-drupal-modules-and-examples-4133418fc143
- Covers automatic AI content moderation setup with modules and examples

### External: ModerationAPI
- **URL:** https://moderationapi.com/integrations/drupal-content-moderation
- **Description:** External content moderation service with Drupal integration

---

## AI Image Generation in Drupal

### Blog: "State of AI Image Generation in Drupal"
- **URL:** https://stefvanlooveren.me/blog/state-ai-image-generation-drupal
- **Author:** Stef Van Looveren
- Covers DALL-E, Stable Diffusion integration via the AI module

### AI Module Image Capabilities
- Text-to-image via AI Core submodule
- Providers: OpenAI (DALL-E), AWS Bedrock (Titan), Azure
- CKEditor image generation plugin (ai_image submodule)
- Alt text generation via vision models

---

## amazee.ai Provider Details

### Technical Whitepaper
- **URL:** https://amazee.ai/drupal-ai-provider-whitepaper.pdf
- Detailed technical documentation

### Key Features
- **URL:** https://amazee.ai/drupal-ai
- **Blog:** https://www.amazee.io/blog/post/experience-the-power-of-drupal-ai-for-free/
- **Drupal.org:** https://www.drupal.org/about/starshot/initiatives/ai/blog/building-smarter-drupal-sites-with-the-amazeeai-ai-provider
- Privacy-first, data-sovereign AI
- Only provider bundling LLMs AND Vector Database
- Processing regions: Switzerland, Germany, US, Australia
- 30 days unlimited free AI tokens for new installs
- Works on any Drupal 10.2+ site, any hosting platform
- Ships with Drupal CMS 2.0 as default provider

---

## AI Testing

### AI Agents Test Module
- **URL:** https://www.drupal.org/project/ai_agents_test
- Automated QA testing for AI agents
- Runs known prompts against agents to ensure consistent behavior

---

## DrupalForge AI Templates

Known templates available:
- Drupal CMS AI (with $1 AI key limit)
- AI Coding Assistant
- AI Automator
- AI SEO Analyzer
- AI Translation
- Canvas AI
- AI for Compliance and Accessibility
- Automated Testing Kit

Free, no Docker required, 30-day environments.

---

## Headless Drupal + AI

### Current Stack
- Drupal + AI module + JSON:API/GraphQL → Next.js frontend
- AI Search provides vector/semantic search with RAG
- MCP Server exposes Drupal content to AI tools
- No dedicated "headless AI" module, but components compose well

### Reference
- Digital Polygon guide: https://www.digitalpolygon.com/blog/introduction-to-headless-drupal
- BRAINSUM: https://www.brainsum.com/blog/harnessing-power-decoupled-architecture-nextjs-and-drupal

---

## Hosting Provider AI Features (Beyond Big 4)

### DevPanel
- **URL:** https://www.devpanel.com/blog/drupal-hosting-providers-comparison-2026/
- AI-assisted onboarding, instant environment cloning
- Used at EC hackathon for deployment

### Dropsolid
- **URL:** https://dropsolid.com/en/knowledge-hub/why-cmsdxp-drupal-backbone-ai-driven-knowledge-platform-and-how-we-guide
- "Why a CMS/DXP like Drupal is the backbone of an AI-driven knowledge platform"
- Offer Drupal AI certification courses (EUR 299-499)

---

## Additional Modules Found

### Accessibility Toolkit
- **URL:** https://www.drupal.org/project/a11y
- **Description:** Comprehensive accessibility toolkit for Drupal

### AI Agents Test
- **URL:** https://www.drupal.org/project/ai_agents_test
- **Description:** QA testing framework for AI agents

---

## Research Completeness Assessment

After 25+ files and 8 waves of research agents covering 90+ distinct search queries:

### Well-Covered Areas (Confidence: HIGH)
- Agent skills repos and their contents
- DDEV AI plugins
- MCP servers for Drupal
- drupal.org AI modules (65+)
- Community initiative ($1.5M, 28 orgs)
- Roadmap 2026 and Canvas AI
- Developer workflow patterns
- Events and training
- Cross-CMS comparisons
- Europa Web Platform
- PHP analysis tools
- Claude Code plugin ecosystem
- Issue queue discussions
- Platform compatibility

### Known Remaining Gaps (Confidence: MEDIUM)
- Individual agency case studies (private/client work, rarely published)
- Exact DrupalCon Chicago 2026 session content (happening this week)
- Drupal Slack #ai channel discussions (no public archive)
- Private/enterprise AI setups not published publicly
- Upcoming Drupal AI module 2.0 features (still in dev branch)

### Likely Not Findable
- Internal EC/Europa Web Platform AI tooling documentation
- Agency-specific CLAUDE.md/AGENTS.md files (proprietary)
- Unreleased/unannounced tools
