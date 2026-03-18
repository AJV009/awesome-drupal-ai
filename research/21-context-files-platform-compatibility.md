# AI Context Files in Drupal Modules & Platform Compatibility

## Critical Drupal.org Issues About AI Context in Core

### Issue #3568936: "Embrace the chaos, add AGENTS.md to core"
- **URL:** https://www.drupal.org/project/drupal/issues/3568936
- **Status:** Active discussion
- **Significance:** Proposal to add AGENTS.md file directly to Drupal core
- **Blog coverage:** https://www.thedroptimes.com/66271/agents-md-drupal-core-discussion
- **Jacob Rockowitz's analysis:** https://www.jrockowitz.com/blog/drupal-agents-md — "Should Drupal core include an AGENTS.md file?"

### Issue #3565489: "Proposal: First-class support for agent-skills"
- **URL:** https://www.drupal.org/project/ai/issues/3565489
- **Project:** AI module
- **Significance:** Proposing that the Drupal AI module natively supports the agentskills.io standard

### Issue #3558328: "Create a Claude Skill for using the Drupal Brand Guidelines"
- **URL:** https://www.drupal.org/project/ai_initiative/issues/3558328
- **Project:** AI Initiative
- **Significance:** Official skill for Drupal brand guidelines — ensures AI follows brand standards

### Issue #3516268: "Consider adding a Claude.md file" (MCP module)
- **URL:** https://www.drupal.org/project/mcp/issues/3516268
- **Significance:** Even individual contrib modules discussing adding CLAUDE.md

---

## Context Control Center (CCC) Module

- **URL:** https://www.drupal.org/project/ai_context
- **Meta roadmap:** https://www.drupal.org/project/ai_context/issues/3567798
- **March 2026 sprint:** https://www.drupal.org/project/ai_context/issues/3573719
- **Description:** Centralized context management for AI in Drupal
- **Status:** Active development with sprint planning
- **Relevance:** HIGH — this is the Drupal-native approach to AI context management

---

## amazee.io AGENTS.md for Drupal

- **URL:** https://github.com/amazeeio/drupal-agents-md
- **Description:** "Drupal AGENTS.md: provide context and instructions to help AI coding agents work on your Drupal 10.x+ project"
- **Author:** amazee.io (Lagoon hosting provider)
- **Significance:** Additional AGENTS.md template alongside Droptica's — shows multiple vendors creating these

---

## Drupal.org Skills/Skill Modules

### Claude Skill - Drupal and DDEV Site Setup (drupal.org)
- **URL:** https://www.drupal.org/project/claude_skill_drupal_ddev_site_setup
- **Coverage:** https://www.thedroptimes.com/55926/james-abraham-experiments-with-claude-skill-drupal-and-ddev-automation
- **Significance:** Skills being published as drupal.org contrib projects

### Skills Module
- **URL:** https://www.drupal.org/project/skills
- **Description:** Skills module on drupal.org

### Skilling Module
- **URL:** https://www.drupal.org/project/skilling
- **Description:** Skilling module on drupal.org

---

## Additional Drupal Skills Repos (Not Previously Cataloged)

### Omedia/drupal-skill
- **URL:** https://github.com/Omedia/drupal-skill
- **New finding** — not in previous research

### nonzod/drupaldev-claude-skill
- **URL:** https://github.com/nonzod/drupaldev-claude-skill
- **Description:** SKILL Claude for Drupal development
- **New finding**

### 0ldh/claude-code-agents-orchestra (Drupal developer agent)
- **URL:** https://github.com/0ldh/claude-code-agents-orchestra/blob/main/agents/specialized-tools/cms/drupal-developer.md
- **Description:** Drupal developer agent within a larger agents orchestra
- **New finding**

### alirezarezvani/claude-skills (192 skills including potential Drupal)
- **URL:** https://github.com/alirezarezvani/claude-skills
- **Description:** 192+ Claude Code skills & agent plugins for multiple coding agents
- **New finding**

---

## Context7 MCP + Drupal

### How Context7 Works
- **URL:** https://context7.com/
- **Docs:** https://context7.com/docs/resources/all-clients
- **Description:** Serves up-to-date, version-specific documentation to LLMs/AI code editors
- **Upstash blog:** https://upstash.com/blog/context7-mcp

### Drupal Integration
- Used by oscarnovasf/claude-drupal-plugin as a bundled MCP
- Used by gkastanis/drupal-claude-code-sub-agent-collective as optional MCP
- Provides Drupal API documentation access to AI tools
- **LangDB listing:** https://langdb.ai/app/mcp-servers/context7-mcp-b4495416-5510-4770-9994-7a6ec01c4803

---

## Conventions for AI Context Files in Drupal Projects

### Project Root Level
| File | Tool Support | Purpose |
|------|-------------|---------|
| CLAUDE.md | Claude Code | Project-specific instructions for Claude |
| AGENTS.md | Cursor, Copilot, Claude Code, Codex, Aider, Gemini CLI, Roo Code, Zed, Devin | Universal AI context file |
| .cursorrules | Cursor IDE | Cursor-specific rules |
| .github/copilot-instructions.md | GitHub Copilot | Copilot custom instructions |
| .claude/ directory | Claude Code | Skills, agents, commands, hooks, settings |
| .kiro/skills/ | Kiro IDE | Kiro-specific skills (same SKILL.md format) |
| .gemini/ | Gemini CLI | Gemini-specific context |

### Module-Level Context (Emerging Convention)
The concept of including AI context files within individual Drupal modules is **emerging but not standardized**:
- Issue #3516268 discusses adding CLAUDE.md to the MCP module
- Issue #3558328 proposes a skill for Drupal brand guidelines
- The ablerz/claude-skill-drupal-module ships as a Composer package installable into `.claude/skills/`

### Planning Files Convention
Based on blog posts and repo patterns:
```
.claude/
├── plans/              # Implementation plans (Tag1 pattern)
├── skills/             # SKILL.md files
├── agents/             # Agent definitions
├── commands/           # Slash commands
├── hooks/              # Quality-gate hooks
├── agent-memory/       # Persistent knowledge (gkastanis pattern)
└── rules/              # Behavioral rules
```

---

## Platform Compatibility Matrix

### Agent Skills (SKILL.md) Compatible Tools
From agentskills.io: 30+ tools including:
- Claude Code (`.claude/skills/`)
- Kiro CLI (`.kiro/skills/`)
- Cursor (supports agent-skills)
- VS Code Copilot (supports agent-skills)
- Gemini CLI
- OpenHands
- Roo Code
- Codex (OpenAI)
- Junie (JetBrains)
- Aider
- Cline
- Devin

### Drupal Skills Platform Support

| Skill/Tool | Claude Code | Cursor | Copilot | Kiro | Gemini CLI | Others |
|------------|:-----------:|:------:|:-------:|:----:|:----------:|:------:|
| agentskills.io SKILL.md | ✅ | ✅ | ✅ | ✅ | ✅ | 25+ more |
| AGENTS.md (Droptica/amazee) | ✅ | ✅ | ✅ | - | ✅ | Aider, Roo, Zed, Devin |
| CLAUDE.md | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| .cursorrules | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| .github/copilot-instructions.md | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| Claude Code plugins | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| MCP servers | ✅ | ✅ | ✅ | ✅ | ✅ | Most modern tools |
| DDEV addons | Tool-agnostic (environment level) | | | | | |

### Key Takeaway
**AGENTS.md + agentskills.io SKILL.md** have the broadest tool support. CLAUDE.md and .cursorrules are tool-specific. The "standard" recommendation should prioritize:
1. **AGENTS.md** (universal)
2. **SKILL.md skills** (30+ tool support)
3. **MCP servers** (broad support)
4. Tool-specific files only as secondary additions

---

## Additional Blog Posts Discovered

### Goran Nikolovski
- **"Automating Drupal dependency management with custom Claude Code commands":** https://gorannikolovski.com/blog/automating-drupal-dependency-management-with-custom-claude-code-commands
- **"Building a Claude Code Subagent to Automate Drupal Core Updates":** https://gorannikolovski.com/blog/building-a-claude-code-subagent-to-automate-drupal-core-updates

### Bonnici
- **"Mastering Claude Code for Drupal Development: 5 tips":** https://bonnici.co.nz/blog/mastering-claude-code-drupal-development

### Ray Burgess
- **"Claude Code and Drupal - A Synthesis":** https://rayburgess.info/2025/09/16/opinions-and-ramblings-about-my-work/claude-code-and-drupal-a-synthesis/

### TheDropTimes
- **"Carlos Ospina Expands Claude Skills with Systematic Tools for Drupal and Design":** https://www.thedroptimes.com/64647/carlos-ospina-expands-claude-skills-with-systematic-tools-drupal-and-design
- **"Droptica Releases AGENTS.md Tool":** https://www.thedroptimes.com/64590/droptica-releases-agentsmd-tool-improve-ai-context-in-drupal-projects

---

## Awesome Lists & Aggregators

### skillmatic-ai/awesome-agent-skills
- **URL:** https://github.com/skillmatic-ai/awesome-agent-skills
- **Description:** "The definitive resource for Agent Skills — modular capabilities revolutionizing AI agent architecture"
- **Relevance:** Aggregator that may list Drupal skills

### LobeHub Skills Marketplace
- madsnorgaard drupal-expert: https://lobehub.com/skills/madsnorgaard-agent-resources-drupal-expert
- madsnorgaard drupal-migration: https://lobehub.com/skills/madsnorgaard-drupal-agent-resources-drupal-migration
- **Significance:** Drupal skills listed on mainstream AI marketplaces

### MCPMarket
- Drupal Coding Standards skill: https://mcpmarket.com/tools/skills/drupal-coding-standards
- **Significance:** Skills also listed on MCP-focused marketplaces
