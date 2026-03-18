# Claude Code Plugin & Skills Ecosystem for Drupal

## Skills vs Plugins Architecture

### Standalone Skills (`.claude/` directory)
- **Skill names:** `/hello`
- **Best for:** Personal workflows, project-specific, quick experiments
- Short names, immediate access
- Files at `.claude/skills/<name>/SKILL.md` or `.claude/commands/<name>.md`

### Plugins (`.claude-plugin/plugin.json`)
- **Skill names:** `/plugin-name:hello` (namespaced)
- **Best for:** Team sharing, community distribution, versioned releases
- Installed from marketplace, require manifest

**Key insight:** "Custom commands have been merged into skills." A file at `.claude/commands/deploy.md` and a skill at `.claude/skills/deploy/SKILL.md` both create `/deploy` and work the same way.

### Agent Skills Standard
Claude Code extends the agentskills.io standard with:
- **Invocation control** (user-invoked vs auto-invoked)
- **Subagent execution**
- **Dynamic context injection**

---

## Official Claude Code Bundled Skills

| Skill | Purpose |
|-------|---------|
| `/batch <instruction>` | Large-scale parallel changes across codebase using git worktrees |
| `/claude-api` | Load Claude API reference for project's language (incl. PHP) |
| Others | Various development workflow skills |

---

## Official Claude Code Plugins (anthropics/claude-code/plugins)

| Plugin | Purpose | Key Feature |
|--------|---------|-------------|
| agent-sdk-dev | Agent SDK development | `/new-sdk-app` command |
| claude-opus-4-5-migration | Model migration | Automated prompt migration |
| code-review | PR review | 5 parallel Sonnet agents |
| commit-commands | Git workflow | `/commit`, `/commit-push-pr` |
| feature-dev | Feature development | 7-phase workflow with code-explorer, code-architect, code-reviewer agents |
| frontend-design | Frontend UI | Auto-invoked for frontend work |
| hookify | Custom hooks | Analyze conversations for problematic behaviors |
| explanatory-output-style | Educational | Implementation explanations |

---

## Drupal-Specific Claude Code Plugins

### oscarnovasf/claude-drupal-plugin (Spanish, TypeScript)
- **Three-plugin system:** drupal-global (base), drupal-backend, drupal-frontend
- **MCPs:** Context7, Obsidian, Playwright
- **Agents:** context7, drupal-backend, drupal-frontend
- **Commands:** /drupal-setup, /update-changelog, /component (SDC)
- **Security hooks:** Protected paths for core, settings, vendor, node_modules
- **Install:** `claude plugin marketplace add` + `claude plugin install`

### gkastanis/drupal-workflow
- **16 skills, 4 agents, 10 commands** (see file 17)
- Quality-gate hooks for session start, pre/post tool use, subagent start, task completion
- Semantic documentation with Logic IDs
- Structural index auto-generation

---

## Plugin Creation for Drupal

### Standard Plugin Structure
```
plugin-name/
├── .claude-plugin/
│   └── plugin.json          # Metadata
├── commands/                 # Slash commands
├── agents/                   # Specialized agents
├── skills/                   # Agent Skills
├── hooks/                    # Event handlers
├── .mcp.json                 # MCP configuration
└── README.md
```

### plugin.json Format
```json
{
  "name": "drupal-dev-tools",
  "description": "Development tools for Drupal",
  "version": "1.0.0",
  "author": { "name": "Author" }
}
```

### Scopes
- `--scope user` (default, all projects)
- `--scope project` (specific project)
- `--scope local` (not synced)

### Plugin Marketplace Distribution
```bash
claude plugin marketplace add https://github.com/user/plugin-repo.git
claude plugin install plugin-name@marketplace-name
```

---

## Hook Events for Drupal Quality Gates

| Event | When | Drupal Use Case |
|-------|------|-----------------|
| SessionStart | Plugin loaded | Display activation, regen structural index |
| PreToolUse | Before tool execution | Block access to sensitive files |
| PostToolUse | After tool execution | Run PHP lint, PHPCS on modified files |
| SubagentStart | Before subagent | Inject Drupal version context |
| TaskCompleted | Task done | Run quality gates |
| PreBash | Before bash command | Block destructive commands |

---

## Distribution Methods Summary

| Method | Tool | Example |
|--------|------|---------|
| Git clone | Any | `git clone <repo> .claude/skills/<name>` |
| Composer | Drupal-native | `composer require ablerz/claude-skill-drupal-module` |
| agr CLI | agent-resources | `agr add madsnorgaard/drupal-agent-resources/drupal-expert` |
| npx skills | agentskills.io | `npx skills add drupal-canvas/skills` |
| Claude plugin | Claude Code | `claude plugin install drupal-global@drupal-tools` |
| DDEV addon | DDEV | `ddev get FreelyGive/ddev-claude-code` |
| Setup script | Standalone | `~/drupal-agentic-workflow/bin/setup.sh .` |

---

## What This Means for the "Standard" List

The standard install could use multiple distribution methods:
1. **DDEV addons** for environment setup (`ddev get`)
2. **Composer** for Drupal module skills (`composer require`)
3. **Claude plugin** for the comprehensive plugin (`claude plugin install`)
4. **AGENTS.md** template via curl/git for project context

An ideal "one-command" solution would wrap all of these into a single DDEV addon or script.
