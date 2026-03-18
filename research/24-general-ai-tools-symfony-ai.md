# General AI Coding Tools & Symfony AI for Drupal Development

## AI Coding Agent Landscape 2026

### Tier 1: Front-Runners
| Tool | Best For | PHP/Drupal Relevance |
|------|---------|---------------------|
| **Claude Code** | Complex debugging, unfamiliar codebases, architectural changes | ★★★★★ Best reasoning, most Drupal-specific tools |
| **Cursor** | Feature tweaks, refactors, tests, bug fixes | ★★★★ Good daily driver, .cursorrules support |
| **Codex (OpenAI)** | CLI workflows, deterministic multi-step tasks | ★★★ Good for automation |
| **GitHub Copilot (Agent Mode)** | Enterprise environments, low friction | ★★★ Widely available but less customizable |
| **Cline** | VS Code power users, model flexibility | ★★★★ Choose models, tune cost |

### Tier 2: Runner-Ups
| Tool | Key Strength | Drupal Relevance |
|------|-------------|-----------------|
| RooCode | Reliability on large multi-file changes | ★★★ |
| Aider | Git-native CLI workflows | ★★★ Compatible via AGENTS.md |
| Gemini CLI | Terminal-first simplicity | ★★ |
| Junie | IntelliJ/PhpStorm integration | ★★★ For PhpStorm Drupal devs |
| Kiro | Spec-driven, Amazon | ★★ Same SKILL.md format |

### Tier 3: Emerging
- AWS Kiro, Kilo Code, Zencoder

---

## Symfony AI — Critical for Drupal

**URL:** https://symfony.com/doc/current/ai.html
**Significance:** Drupal is built on Symfony. Symfony AI components are directly usable in Drupal.

### Core Components

| Component | Purpose | Drupal Application |
|-----------|---------|-------------------|
| **Platform** | Unified AI provider interface | Use in custom Drupal modules instead of direct API calls |
| **Agent** | AI agent framework with tools | Build Drupal-specific agents with Symfony's agent system |
| **Chat** | Conversation history management | Power chatbot features in Drupal |
| **Store** | Vector DB abstraction (ChromaDB, Pinecone, Weaviate, MongoDB) | Backend for AI Search module |
| **Mate** | MCP server component | Bridge between Drupal and AI assistants |
| **AI Bundle** | Symfony integration bundle | Service container integration for Drupal |
| **MCP Bundle** | MCP SDK integration | Protocol-based AI communication |

### Supported Providers (via Symfony AI Platform)
OpenAI, Anthropic, Google Gemini, Azure OpenAI, AWS Bedrock, Mistral, Ollama — same providers as Drupal AI module

### Key Features
- Multi-platform with single consistent API
- Tool calling (extend agents with custom tools)
- RAG with vector store integration
- Structured output (PHP classes/array schemas)
- Multi-modal (text, images, audio)
- Streaming support

### Relevance to Drupal
The Drupal AI module's sprint deliverables mentioned "Symfony AI integration" — this confirms Drupal is building on Symfony AI components rather than maintaining a parallel implementation. This is a significant architectural decision.

---

## AI Pair Programming Best Practices (2026 Consensus)

### Planning & Process
1. **Write plans first** — Markdown plan → AI critiques → save as instructions.md
2. **Edit-test loop** — Write failing tests → review → AI implements solutions
3. **Demand reasoning before code** — Request step-by-step explanations first

### Context Management
4. **Curate context strategically** — Don't dump entire codebases; use Context7 MCP or gitingest summaries
5. **Version control discipline** — Granular commits via `git add -p` for readable diffs
6. **Keep prompts laser-focused** — Specific file references, line numbers, exact terminology
7. **Re-index after major changes** — Rebuild project indexes post-refactor
8. **Use file references over copy-paste** — Use `@` syntax for current file states

### Testing & Debugging
9. **You specify tests, AI generates** — Define edge cases, error conditions; AI generates boilerplate
10. **Debug systematically** — Request diagnostic reports: modified files, root causes, multiple approaches

### Code Quality
11. **Establish style guidelines** — System prompt with error handling, docs, code length limits
12. **Senior-level code review** — Treat ALL AI output like junior developer PRs

### Drupal-Specific Application
These practices directly map to the Drupal AI development workflow:
- Plan-first → CLAUDE.md / AGENTS.md
- Edit-test → ddev phpunit + AI
- Curate context → Context7 MCP for Drupal docs
- Style guidelines → Drupal coding standards skill
- Code review → drupal-reviewer agent

---

## SKILL.md Authoring Best Practices (Official Claude Docs)

### Core Principles

**1. Concise is key**
- Only add context Claude doesn't already have
- Challenge: "Does Claude really need this explanation?"
- Default: Claude is already very smart

**2. Set appropriate degrees of freedom**
- High freedom for variable tasks (text-based instructions)
- Low freedom for fragile operations (exact scripts/commands)

**3. Progressive disclosure**
- Metadata (~100 tokens) loaded at startup
- SKILL.md (<5000 tokens recommended) loaded on activation
- Reference files loaded only when needed

**4. Test with real usage**
- Try different phrasings
- Test edge cases
- Verify outputs match expectations

### For Drupal Skills Specifically
- Keep SKILL.md under 500 lines
- Move detailed Drupal API reference to `references/` directory
- Include specific code examples for Drupal patterns (not just descriptions)
- Reference `api.drupal.org` for live documentation

---

## MCP Server Best Practices

### From the ecosystem research:
1. **Focus on read-first** — Start with read-only tools, add write capabilities carefully
2. **Use transport abstraction** — Support both STDIO and HTTP for maximum compatibility
3. **Implement auth** — API keys at minimum; OAuth 2.1 for production
4. **Limit tool scope** — Specific, well-named tools > generic Swiss-army-knife tools
5. **Include descriptions** — Every tool needs a clear description for AI discovery
6. **Handle errors gracefully** — Return structured error responses, not crashes
7. **Rate limit** — Prevent runaway AI token costs

### Drupal-Specific MCP Patterns
- Use Tool API module for plugin-based tool discovery
- Leverage Drupal's permission system for access control
- Cache responses to reduce API overhead
- Use Drush as the execution bridge (proven stable)

---

## PHP-Specific AI Tools Beyond Drupal

### Neuron AI (PHP Agent Framework)
- **URL:** https://www.neuron-ai.dev/
- Production-ready PHP agents with RAG, multi-agent, human-in-the-loop
- Works with Symfony/Drupal stack
- No official Drupal module yet

### PHPocalypse MCP
- Wraps PHPStan + PHP-CS-Fixer + PHPUnit via YAML config
- Single MCP server for all PHP quality tools
- Archived but concept proven

### Composer AI Tools
- No dedicated AI Composer management tool found
- madsnorgaard's drupal-agent-resources `/config-export` and `/module-scaffold` commands fill this gap

---

## Twig AI Assistance

- **No dedicated Twig AI tools found**
- Storybook MCP serves Twig component documentation
- gxleano/drupal-agentic-workflow includes `drupal-frontend-expert` skill with Twig patterns
- ECL (Europa Component Library) uses Twig — opportunity for ECL-specific AI skills
- Gap: No Twig template validation MCP server exists

---

## AI for Database Schema Design

- **No dedicated Drupal schema AI tool found**
- The AI Agents Field Type Agent creates/edits fields (closest equivalent)
- AI Architect (aia) module generates content types, fields, form/view displays from NL
- Gap: No tool specifically optimizes database schema for performance

---

## drupalorg-cli 0.8.0 — AI Agent Integration

**URL:** https://mglaman.dev (March 3, 2026)
**Author:** Matt Glaman

Added GitLab issue fork and merge request commands specifically designed to be "useful for developers using AI agents to assist with Drupal.org issues." This is the CLI tool that scottfalconer/drupal-contribute-fix depends on for its contribution workflow.

Commands:
- `drupalorg issue:show <nid> --format=llm`
- `drupalorg issue:get-fork <nid> --format=llm`
- `drupalorg mr:list <nid> --format=llm`
- `drupalorg mr:status <nid> <mr-iid> --format=llm`

The `--format=llm` flag formats output specifically for AI agent consumption.
