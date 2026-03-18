# Agentic Architecture & AI Frameworks for Drupal

## Drupal's Built-in Agentic Framework

### AI Agents Module
- **URL:** https://www.drupal.org/project/ai_agents
- **Description:** Framework for creating agents of all sorts, including text-to-action agents that manipulate Drupal configurations or content based on textual or multimodal instructions
- **Version 1.1:** No-code AI agent creation from admin interface
- **Storage:** Agents stored as configurations, enabling reuse across chatbots, CLI tools, APIs, widgets
- **Security:** Adheres to content permissions, allows human oversight

#### Built-in Agents
1. **Field Type Agent** — Create or edit fields on entities
2. **Content Type Agent** — Create, edit, and answer questions about node types
3. **Taxonomy Agent** — Manage taxonomy vocabularies and terms

#### Architecture
- Utilizes tool calling — development only needed if a tool doesn't exist for the task
- Supports multiple interfaces: chatbots, command-line, APIs, widgets
- Can be shipped in recipes or modules

### AI Agent Handler Agent
- **URL:** https://www.drupal.org/project/ai_agent_agent
- **Description:** Meta-agent that orchestrates other agents

### FlowDrop Agents
- **URL:** https://www.drupal.org/project/flowdrop_agents
- **Description:** Bridges Drupal's AI Agents with FlowDrop workflows
- **Capabilities:** Execute AI agents as workflow nodes, automate content creation, configuration changes, conversational flows, complex multi-step AI tasks
- **Origin:** Born during Drupal AI Hackathon - Plat to Impact 2026 (European Commission)
- **Relevance:** HIGH — direct EC connection, workflow automation

### AI Automators
- Part of the AI module, distinct from AI Agents
- Allow "Chain Reactions" triggered during content save process
- Multiple fields populate automatically
- Work out of the box with extensive no-code customization
- Featured in Drupal CMS 1.0: content assistance in CKEditor, Alt text generation

---

## PHP AI Frameworks

### LLPhant
- **URL:** https://github.com/LLPhant/LLPhant
- **Description:** Comprehensive PHP Generative AI Framework using OpenAI GPT 4. Inspired by LangChain
- **Requirements:** PHP 8.1+
- **Relevance:** Could be used within Drupal for custom AI integrations
- **Maturity:** Active development, well-maintained

---

## AI-Powered Code Review for Drupal

### Claude AI Code Review (bPekker.dev / Cheppers)
- **URL:** https://bpekker.dev/ai-code-review/
- **URL:** https://cheppers.com/post/drupal-ai-code-review
- **Approach:** Claude interprets code structure, flags logic flaws, suggests architectural improvements, simulates human code review
- **Scope:** Reviews .php, .module, .install, .theme, .twig, YAML files; skips core, contrib, vendor
- **Differentiation:** Goes beyond static analysis (phpstan, drupal-check) with contextual understanding

### GPT Code Reviewer Module
- **URL:** https://www.drupal.org/project/gpt_code_reviewer
- **Description:** Leverages OpenAI's AI technology to automate code review for Drupal
- **Features:** Insightful feedback and security vulnerability detection

### Bounteous LLM Approach
- **URL:** https://www.bounteous.com/insights/2025/07/07/automating-drupal-code-refactoring-and-reviews-llms/
- **Approach:** Integrating AI into CI/CD for "first pass" reviewer that catches deprecations, enforces standards, suggests architectural improvements
- **Architecture:** Hybrid approach — LLM reviews + static analysis + human review

---

## Agentic Development Workflows

### AGENTS.md for Drupal (Droptica)
- **URL:** https://www.droptica.com/blog/agentsmd-tool-how-ai-actually-speeds-drupal-work/
- **Description:** AGENTS.md file helps AI understand Drupal project context
- **Benefits:** Reduces onboarding time, improves debugging, reduces AI hallucinations
- **Compatibility:** Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin

### Talking Drupal #538 - Agentic Development Workflows
- **URL:** https://talkingdrupal.com/538
- **Format:** Podcast discussion on agentic development patterns in Drupal

### Developer Workflow Patterns (from blog posts)

#### Claude Code + DDEV Integration
- Shift to Claude Code setup with DDEV integration
- Add .claude folder in repo for plans, reference snippets, docs
- Carry context between sessions
- Source: jrockowitz.com

#### Plan-First Approach
- Ask AI to write a plan to a file first
- Execute step by step with pauses for review
- Course-correct early
- Source: jrockowitz.com

#### Iterative Markdown Requirements
- Cut and paste Markdown requirements into AI
- Review output in sidebar
- Repeat iteratively

---

## CI/CD + AI Integration

### Current State
- Traditional CI/CD for Drupal: Jenkins, GitLab CI, CircleCI, Travis CI, GitHub Actions
- Standard pipeline: build (Composer) → test (PHPUnit) → deploy
- AI integration into CI/CD pipelines is **emerging but not yet standardized**

### Existing CI/CD Tools for Drupal
- **Lullabot/drupal9ci:** GitHub Actions CI for Drupal — https://github.com/Lullabot/drupal9ci
- **mog33/gitlab-ci-drupal:** GitLab CI for Drupal 11+ — https://gitlab.com/mog33/gitlab-ci-drupal
- **drupal_gitlabci:** Drupal GitLab CI integration — https://www.drupal.org/project/drupal_gitlabci

### AI in CI/CD (Emerging)
- LLM-based code review in CI pipelines (Bounteous approach)
- AI-powered linting as part of commit hooks (gxleano/drupal-agentic-workflow)
- Quality-gate hooks (gkastanis/drupal-workflow)
- No standardized GitHub Action or GitLab CI template for AI-assisted Drupal development yet

---

## AI-Assisted Testing

### Four Kitchens Approach
- **URL:** https://www.fourkitchens.com/blog/development/ai-drupal-testing-development-efficiency/
- AI-driven testing for faster development without sacrificing quality

### Freelock / Drupal Flake Approach
- **URL:** https://www.freelock.com/blog/john-locke/2025-09/easy-unit-testing-drupal-flake-and-ai-group-purl-case-study
- Easy unit testing with Drupal Flake and AI
- Captures lessons in reusable ruleset → consistent AI testing assistant

### testRigor
- **URL:** https://testrigor.com/drupal-testing/
- AI-based automated testing tool with Drupal support

---

## AI-Powered Site Building

### Drupal CMS 1.0 (Starshot)
- Released at DrupalCon Atlanta 2025
- AI-enabled website building capabilities
- AI Automators built-in
- No-code AI agent creation

### Relevance AI Agent Template
- **URL:** https://relevanceai.com/agent-templates-software/drupal
- External platform offering Drupal AI agent template

### Workik
- **URL:** https://workik.com/drupal-code-generator
- Free AI-powered Drupal code generator (external SaaS)

---

## Drupal AI Module Code Generation
- **URL:** https://www.drupal.org/project/ai_generation
- Drupal AI code generation contributed module
