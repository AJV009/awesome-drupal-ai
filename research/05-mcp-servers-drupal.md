# MCP (Model Context Protocol) Servers Relevant to Drupal Development

## MCP Ecosystem Context

### Official PHP SDK
- **Blog:** http://blog.modelcontextprotocol.io/posts/2025-09-05-php-sdk/
- **Relevance:** HIGH — PHP SDK enables native MCP server development in PHP/Drupal

### MCP Registry & Roadmap
- **Registry Preview:** http://blog.modelcontextprotocol.io/posts/2025-09-08-mcp-registry-preview/
- **2026 Roadmap:** http://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/

---

## Drupal-Specific MCP Servers & Modules

### DrupalMCP.io (Drupal MCP Project)
- **URL:** https://drupalmcp.io/
- **Setup:** https://drupalmcp.io/en/mcp-server/setup-configure/
- **Roadmap:** https://drupalmcp.io/en/roadmap/
- **Description:** Dedicated MCP implementation for Drupal
- **Relevance:** HIGH — purpose-built MCP server for Drupal

### Drupal MCP Module (drupal.org)
- **URL:** https://www.drupal.org/project/mcp
- **Releases:** https://www.drupal.org/project/mcp/releases
- **Documentation:** https://mcp-77a54f.pages.drupalcode.org/
- **Description:** Model Context Protocol module for Drupal
- **Relevance:** HIGH — official contributed module

### MCP Server Module (drupal.org)
- **URL:** https://www.drupal.org/project/mcp_server
- **Description:** Turns your Drupal site into an MCP server for AI tools like Claude and Cursor
- **Coverage:** https://www.thedroptimes.com/66132/turn-your-drupal-site-mcp-server-ai-tools-claude-and-cursor
- **Relevance:** HIGH — enables Drupal sites to serve context to AI tools

### MCP Client Module (drupal.org)
- **URL:** https://www.drupal.org/project/mcp_client
- **Description:** MCP client for Drupal — allows Drupal to consume MCP servers
- **Relevance:** MEDIUM-HIGH

### MCP Tools Module (drupal.org)
- **URL:** https://www.drupal.org/project/mcp_tools
- **Description:** Additional MCP tooling for Drupal
- **Relevance:** MEDIUM-HIGH

### Omedia/mcp-server-drupal (TypeScript)
- **URL:** https://github.com/Omedia/mcp-server-drupal
- **Description:** TS-based companion MCP server for the Drupal MCP module, works with STDIO transport
- **Relevance:** HIGH — TypeScript companion for Drupal MCP module

### peximo/drupal-mcp-server
- **URL:** https://github.com/peximo/drupal-mcp-server
- **Description:** Drupal MCP server implementation
- **Relevance:** MEDIUM

### Cleversoft-IT/drupal-modules-mcp
- **URL:** https://github.com/Cleversoft-IT/drupal-modules-mcp
- **Description:** MCP servers for Drupal development. Includes tools for querying Drupal.org module. Integrates with Cline and other MCP-compatible clients
- **Relevance:** HIGH — queries drupal.org module info from AI tools

### Cleversoft-IT/drupal-tools-mcp
- **URL:** https://github.com/Cleversoft-IT/drupal-tools-mcp
- **Description:** MCP servers for Drupal development. Includes tools for querying Drupal.org modules AND interacting with Drush commands. Integrates with Cline
- **Relevance:** HIGH — Drush integration via MCP

---

## DDEV MCP Servers

### codingsasi/ddev-mcp
- **URL:** https://github.com/codingsasi/ddev-mcp
- **NPM:** https://www.npmjs.com/package/ddev-mcp
- **Listings:** LobeHub, MCP Servers directories
- **Description:** MCP server for DDEV with tooling for platform.sh, playwright, drush, wp-cli
- **Relevance:** HIGH — comprehensive DDEV MCP integration

### AkibaAT/ddev-mcp
- **URL:** https://github.com/AkibaAT/ddev-mcp
- **Listings:** LobeHub, mcpservers.org, playbooks.com
- **Description:** DDEV MCP Server
- **Relevance:** HIGH

---

## Drush MCP Bridge

### bloomidea/drush-mcp-bridge
- **URL:** https://packagist.org/packages/bloomidea/drush-mcp-bridge
- **Description:** MCP bridge for Drush commands
- **Relevance:** HIGH — enables AI tools to run Drush commands via MCP

---

## Browser Automation MCP

### Playwright MCP (@playwright/mcp)
- **URL:** https://github.com/microsoft/playwright-mcp
- **Guides:** https://aiagentskit.com/blog/playwright-mcp/, https://codemify.com/pageplaywritestepbystep
- **Analysis:** https://bug0.com/blog/playwright-mcp-changes-ai-testing-2026, https://bug0.com/blog/playwright-mcp-servers-ai-testing
- **Description:** AI-powered browser automation from Microsoft
- **Relevance:** HIGH — essential for testing Drupal sites via AI

---

## PHP-Specific MCP Servers

### PHP MCP PHPStan
- **URL:** https://github.com/lunetics/php-mcp-phpstan
- **Description:** PHPStan integration via MCP
- **Relevance:** HIGH — PHPStan is essential for Drupal code quality

---

## Database MCP Servers

### bytebase/dbhub
- **URL:** https://github.com/bytebase/dbhub
- **Description:** Database MCP hub supporting MySQL, PostgreSQL, and more
- **Relevance:** MEDIUM-HIGH — useful for Drupal database interactions

---

## Component Documentation MCP

### Storybook MCP Server
- **URL:** https://apify.com/baldasseva/storybook-mcp
- **Description:** MCP server for Storybook component documentation
- **Relevance:** MEDIUM — useful for Drupal theme/component development

---

## AWS MCP Servers (Web Development)

### Frontend MCP Server (AWS)
- **URL:** https://awslabs.github.io/mcp/servers/frontend-mcp-server
- **Description:** Frontend development MCP server
- **Relevance:** LOW-MEDIUM

### OpenAPI MCP Server (AWS)
- **URL:** https://awslabs.github.io/mcp/servers/openapi-mcp-server
- **Description:** OpenAPI specification MCP server
- **Relevance:** MEDIUM — useful for API-first Drupal development

---

## MCP Observability

### Sentry MCP Server Monitoring
- **URL:** https://blog.sentry.io/introducing-mcp-server-monitoring/
- **Description:** Debug MCP servers with observability
- **Relevance:** LOW-MEDIUM — useful for debugging MCP integrations

---

## Blog Posts & Guides

### "Turn Your Drupal Site Into an MCP Server"
- **URL:** https://www.thedroptimes.com/66132/turn-your-drupal-site-mcp-server-ai-tools-claude-and-cursor
- **URL:** https://bonnici.co.nz/blog/drupal-mcp-server-ai-integration

### "Exploring the Model Context Protocol (MCP) with Drupal"
- **URL:** https://albert.skibinski.nl/en/blog/exploring-model-context-protocol-mcp-drupal/
- **Author:** Albert Skibinski (askibinski on GitHub — found in agent skills repos too)

### "Drupal's Role as an MCP Server: A Practical Guide"
- **URL:** https://opensenselabs.com/blog/mcp-server

### "Model Context Protocol for Drupal"
- **URL:** https://www.mindsing.com/blog/technology-innovation/model-context-protocol-drupal/

### DrupalCon Vienna 2025 Session: "ECA, AI and MCP: Connecting Context, Intelligence and Action"
- **URL:** https://events.drupal.org/vienna2025/session/eca-ai-and-mcp-connecting-context-intelligence-and-action

### MCP Advanced Topics Course (Anthropic)
- **URL:** https://anthropic.skilljar.com/model-context-protocol-advanced-topics

---

## Assessment

The Drupal MCP ecosystem is **rapidly growing** with multiple implementations:
- 3 drupal.org modules (mcp, mcp_server, mcp_client, mcp_tools)
- External MCP servers (DrupalMCP.io, Omedia, peximo, Cleversoft-IT)
- DDEV MCP bridges (codingsasi, AkibaAT)
- Drush MCP bridge (bloomidea)
- Official PHP SDK from MCP project
- Multiple blog posts and DrupalCon sessions

### Recommended for "Standard" list:
1. drupal.org/project/mcp_server (turn Drupal into MCP server)
2. Cleversoft-IT/drupal-tools-mcp (Drupal.org + Drush via MCP)
3. codingsasi/ddev-mcp (DDEV MCP integration)
4. @playwright/mcp (browser testing)
5. lunetics/php-mcp-phpstan (code quality)
