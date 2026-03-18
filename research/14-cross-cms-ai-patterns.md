# Cross-CMS AI Development Tool Patterns

## Laravel Boost (The Inspiration)

Laravel's AI coding starter kit that directly inspired Drupal's proposal.

### What It Includes
- Dedicated MCP server with 15+ specialized tools
- AI can query databases, execute code, access logs
- Vectorized documentation enabling semantic search across version-specific guides
- Curated AI guidelines for framework conventions and coding patterns

### Distribution
- Single-command installation
- Automatically configures AI tool settings
- Version-aware documentation access

### Relevance to Drupal
Ronald te Brake's "AI Coding Starter Kit for Drupal" proposal explicitly models after Laravel Boost. The key pattern: **unified, opinionated, one-command setup** rather than fragmented individual tools.

---

## Shopware AI Coding Tools

**URL:** https://github.com/shopwareLabs/ai-coding-tools

### Architecture
```
shopwareLabs/ai-coding-tools/
├── .claude-plugin/          # Plugin configuration
├── plugins/                 # Individual plugins
│   ├── dev-tooling/        # MCP servers, hooks, LSP
│   ├── gh-tooling/         # GitHub integration
│   ├── test-writing/       # Test generation
│   ├── adr-writing/        # Architecture Decision Records
│   ├── chunkhound-integration/
│   └── ci-failure-interpretation/
├── AGENTS.md
└── SECURITY.md
```

### 6 Plugins Available
1. **dev-tooling** — MCP servers, hooks, LSP for PHP (PHPStan, ECS, PHPUnit, Symfony Console), JS (ESLint, Prettier, Jest, TypeScript, Vite), Shopware LSP
2. **gh-tooling** — GitHub integration
3. **test-writing** — Test generation
4. **adr-writing** — Architecture Decision Records with AI
5. **chunkhound-integration** — Code chunking
6. **ci-failure-interpretation** — Interpret CI failures with AI

### Platform Support
Claude Code exclusively (via plugin architecture)

### Patterns to Learn From
- **Plugin marketplace approach** — modular, installable components
- **LSP integration** — Language Server Protocol for framework-specific intelligence
- **ADR writing** — AI for architecture documentation
- **CI failure interpretation** — AI reads CI logs and explains failures
- **AGENTS.md included** — project context file

---

## WordPress AI Development Tools

### NickOrtiz/cursorrules
- **URL:** https://github.com/NickOrtiz/cursorrules
- **Description:** Portable Cursor rules for WordPress development, 10up-inspired
- **Features:** Silent AI code suggestions, WordPress/Gutenberg best practices, portable prompt templates
- **Status:** Minimal (2 commits, 0 stars)

### WordPress AI Landscape
- Much less organized than Drupal's AI initiative
- No equivalent of drupal/ai module or Drupal AI Initiative
- Individual agency efforts (10up) rather than community-wide coordination
- WordPress VIP has PHPCS integration but no AI-specific tooling

### Assessment
WordPress AI development tooling is **significantly behind** Drupal's organized initiative. Drupal's community-driven approach with $1.5M funding and 50+ contributors is unique in the CMS space.

---

## Symfony AI Tools

- Symfony is Drupal's base framework
- Drupal AI module has **Symfony AI integration** (mentioned in sprint deliverables)
- No dedicated Symfony AI coding tools found comparable to Drupal's ecosystem
- LLPhant (PHP LangChain equivalent) works with Symfony/Drupal

---

## Linux Kernel AI Approach (Referenced in Starterkit Proposal)

The Drupal AI Starterkit proposal references the Linux kernel's approach to AI-assisted contributions. Key pattern:
- Strict coding standards documented for AI consumption
- Contribution guidelines machine-readable
- Automated checking against standards

---

## GitHub spec-kit (Referenced in Starterkit Proposal)

GitHub's spec-kit tool was mentioned in the Drupal Starterkit proposal discussion as an inspirational model for structuring AI coding rules.

---

## Key Patterns Across CMS/Frameworks

| Pattern | Laravel | Shopware | WordPress | Drupal |
|---------|---------|----------|-----------|--------|
| Unified starter kit | ✅ Boost | ❌ | ❌ | 🔄 Proposed |
| MCP servers | ✅ 15+ tools | ✅ via dev-tooling | ❌ | ✅ Multiple |
| AGENTS.md/context files | ✅ | ✅ | ❌ | ✅ Droptica |
| AI coding skills | ❌ | ✅ 6 plugins | ❌ | ✅ 12+ repos |
| Cursor rules | ✅ | ❌ | ✅ (minimal) | ✅ cursor.directory + ivangrynenko |
| Community AI initiative | ❌ | ❌ | ❌ | ✅ $1.5M, 28 orgs |
| AI module framework | ❌ | ❌ | ❌ | ✅ drupal/ai (48+ providers) |
| Recipe-based distribution | ❌ | ❌ | ❌ | ✅ Drupal Recipes |

### Drupal's Unique Advantages
1. **Only CMS with a funded AI initiative** ($1.5M, formal governance)
2. **Most comprehensive AI module ecosystem** (65+ modules)
3. **Recipe-based distribution** for AI features
4. **Most active agent skills community** (12+ repos, 50+ skills)
5. **MCP integration** at both Drupal site level and development tool level

### What Drupal Can Learn
1. **Laravel Boost's one-command simplicity** — Drupal needs this badly
2. **Shopware's CI failure interpretation plugin** — applicable to Drupal CI
3. **Shopware's ADR writing plugin** — architecture documentation with AI
4. **Shopware's LSP integration** — Drupal could have a Drupal LSP for AI tools
