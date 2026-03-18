# PHP Static Analysis, Testing & Code Quality Tools with AI for Drupal

## PHPStan + AI Integration

### PHPStan MCP Servers

#### lunetics/php-mcp-phpstan
- **URL:** https://github.com/lunetics/php-mcp-phpstan
- **Description:** MCP server for PHPStan static analysis integration with LLM agents
- **Relevance:** HIGH — enables AI coding tools to run PHPStan checks

#### larspohlmann/mcp-phpstan-server
- **URL:** https://github.com/larspohlmann/mcp-phpstan-server
- **Listings:** https://playbooks.com/mcp/larspohlmann/mcp-phpstan-server, https://lobehub.com/mcp/larspohlmann-mcp-phpstan-server, https://mcplane.com/mcp_servers/phpphpstan
- **Description:** Minimal MCP server in pure PHP exposing PHPStan, zero dependencies
- **Relevance:** HIGH — lightweight, no dependencies

#### PHPStan MCP in PHP SDK Example
- **URL:** https://deepwiki.com/eduardocruz/mcp-php-sdk/6.1-phpstan-mcp-server-example
- **Description:** Example of building PHPStan MCP server with PHP SDK

### PHPStan for Drupal
- **Guide:** https://mglaman.dev/blog/writing-better-drupal-code-static-analysis-using-phpstan (Matt Glaman)
- **Practical example:** https://codingadventures.netlify.app/how-to-use-phpstan-on-your-drupal-module-a-practical-example-of-mine/

### PHPocalypse MCP Server
- **URL:** https://playbooks.com/mcp/plapinski-phpocalypse
- **Description:** PHP-focused MCP server for AI agents
- **Relevance:** MEDIUM

---

## Drupal Rector (Automated Code Transformation)

### drupal-rector
- **URL:** https://github.com/palantirnet/drupal-rector
- **Drupal.org:** https://www.drupal.org/project/rector
- **Description:** Developer utility for automatically upgrading deprecated code
- **Guides:**
  - https://www.palantir.net/blog/jumpstart-your-drupal-9-upgrade-drupal-rector
  - https://www.cmsdrupal.com/blog/drupal-8-drupal-9-upgrade
  - https://gole.ms/blog/glimpse-drupal-9-upgrade-drupal-rector
  - https://gole.ms/guidance/automated-removal-deprecations-easy-drupal-9-upgrades

### Upgrade Rector Module
- **URL:** https://www.drupal.org/project/upgrade_rector
- **Description:** Automated Drupal compatibility fixes

### AI + Rector Potential
- Rector provides AST-based code transformation
- AI could generate Rector rules for custom code patterns
- No direct AI-Rector integration found yet — **gap in ecosystem**

---

## PHP CodeSniffer (PHPCS) for Drupal

### Core Tool
- **URL:** https://github.com/PHPCSStandards/php_codesniffer
- **Legacy:** https://github.com/squizlabs/PHP_CodeSniffer
- **Guides:**
  - https://www.droptica.com/blog/improving-code-quality-phpcodesniffer-tool/
  - https://www.twilio.com/en-us/blog/developers/community/improving-php-code-quality-php-codesniffer-phpcs-laravel

### Drupal-Specific Code Quality
- **hussainweb/drupal-code-quality:** https://github.com/hussainweb/drupal-code-quality — Docker image with QA tools
- **Guide:** https://hussainweb.me/code-quality-check-tools-for-drupal/
- **Five Jars analysis:** https://fivejars.com/insights/top-php-static-code-analysis-tools-drupal/
- **Jeff Geerling CI guide:** https://www.jeffgeerling.com/blogs/jeff-geerling/ci-deployments-code-analysis-drupal-php

### AI + PHPCS
- Shopware's dev-tooling plugin integrates ECS (Easy Coding Standard, PHPCS alternative) via MCP
- The ronaldtebrake/drupal-coding-standards-skill enforces standards via AI
- DDEV commands (phpcs, phpcbf) used by ablerz/claude-skill-drupal-module
- No direct PHPCS MCP server found — **potential gap**

---

## drupal-check (Deprecation Checking)

### Tool
- **URL:** https://github.com/mglaman/drupal-check
- **Author:** Matt Glaman
- **Description:** Check Drupal code for deprecations and discover bugs via static analysis

### Related Modules
- **Upgrade Status:** https://www.drupal.org/project/upgrade_status — essential for Drupal upgrades
  - Guide: https://www.thedroptimes.com/41909/upgrade-status-module-essential-tool-drupal-website-upgrades
  - ImageX guide: https://imagexmedia.com/blog/prepare-drupal-upgrade-status-module
- **Deprecation Dashboard:** https://www.thedroptimes.com/55124/drupal-deprecation-dashboard-relaunched-with-drupal-12-readiness-data

### AI + Deprecation Fixing
- Gábor Hojtsy's experiment: "Bringing Drupal Module Upgrader back from the dead in less than 24 hours" (Mar 2026)
  - **URL:** https://www.hojtsy.hu/blog/2026-mar-07/my-experiment-bringing-drupal-module-upgrader-back-dead-less-24-hours
  - Used AI to revive the Drupal Module Upgrader tool
- Also: https://www.hojtsy.hu/blog/2024-apr-19/how-i-update-my-drupal-modules-drupal-11-only-gitlab-and-drupalorg-my-browser
- **Drupal Module Upgrader 2.0.0-alpha2:** https://www.thedroptimes.com/66958/drupal-module-upgrader-alpha2-d10-d11

---

## AI-Assisted Testing for Drupal

### AI Testing Module
- **URL:** https://www.drupal.org/project/ai_testing
- **Description:** AI-assisted testing module for Drupal
- **Relevance:** HIGH — dedicated AI testing module

### Automated Testing Kit
- **URL:** https://www.drupal.org/project/automated_testing_kit
- **DrupalForge Template:** https://www.drupalforge.org/template/automated_testing_kit
- **Description:** Comprehensive testing kit for Drupal

### PHPUnit + AI
- **Drupal PHPUnit docs:** https://www.drupal.org/docs/develop/automated-testing/phpunit-in-drupal
- **Types of tests:** https://www.drupal.org/docs/develop/automated-testing/types-of-tests
- **Drupal Test Traits:** https://www.drupalatyourfingertips.com/dtt
- **Freelock case study:** https://www.freelock.com/blog/john-locke/2025-09/easy-unit-testing-drupal-flake-and-ai-group-purl-case-study

### Playwright & Cypress for Drupal
- **Stanford WebCamp session:** https://webcamp.stanford.edu/session/setting-up-a-comprehensive-automated-testing-regime-for-drupal-using-cypress-and-playwright
- **Applitools Drupal testing:** https://applitools.com/blog/automated-testing-drupal-applitools/
- **Playwright MCP:** Essential for AI-driven browser testing of Drupal sites

---

## AI-Powered Code Review for Drupal

### GPT Code Reviewer Module
- **URL:** https://www.drupal.org/project/gpt_code_reviewer
- **Description:** OpenAI-powered code review for Drupal
- **Related GitHub tool:** https://github.com/rjmacarthy/gpt-code-reviewer

### Reviewer Module
- **URL:** https://www.drupal.org/project/reviewer
- **Description:** Code review module for Drupal

### AI Code Review (Bálint Pekker)
- Claude-based: https://bpekker.dev/ai-code-review/
- Cheppers: https://cheppers.com/post/drupal-ai-code-review

### Bounteous LLM Approach
- **URL:** https://www.bounteous.com/insights/2025/07/07/automating-drupal-code-refactoring-and-reviews-llms/
- AI in CI/CD pipeline for automated first-pass review

### DrupalCon Session
- **"Automate, Integrate, Innovate: AI-powered GitLab CI for Drupal module development"**
- **URL:** https://www.thedroptimes.com/event/session/46643/automate-integrate-innovate-ai-powered-gitlab-ci-drupal-module-development

---

## AI-Assisted Debugging

### DrupalForge Guide
- **URL:** https://www.drupalforge.org/blog/ai-assisted-debugging-drupal-projects-10-practical-ways-fix-bugs-faster
- **Title:** "AI-Assisted Debugging for Drupal Projects: 10 Practical Ways To Fix Bugs Faster"
- **Relevance:** HIGH — practical debugging guide

---

## AI Upgrade/Migration Tools

### AI Upgrade Module
- **URL:** https://www.drupal.org/project/ai_upgrade
- **Description:** AI-assisted Drupal upgrades

### AI Content Migrate
- **URL:** https://www.drupal.org/project/ai_content_migrate
- **Description:** AI-assisted content migration

### AI Migration
- **URL:** https://www.drupal.org/project/ai_migration
- **Description:** Full AI migration framework

### AI Migrate Agent
- **URL:** https://www.drupal.org/project/ai_migrate
- **Description:** AI migration helper

### Valuebound Guide
- **URL:** https://www.valuebound.com/blog/drupal-migration-made-easy-recipes-and-ai-tools
- **Description:** Migration with Recipes + AI tools

### Pantheon Guide
- **URL:** https://pantheon.io/learning-center/drupal/ai
- **Description:** Streamlining workflows with Drupal AI modules
- Also: https://pantheon.io/learning-center/drupal-migration

---

## Summary: PHP Quality + AI Integration Points

| Tool | AI Integration | Status |
|------|---------------|--------|
| PHPStan | MCP servers (2+) | ✅ Available |
| PHPCS | Via coding standards skill | ✅ Available |
| Rector | No direct AI integration | ❌ Gap |
| drupal-check | Deprecation info for AI context | 🔄 Partial |
| PHPUnit | AI test generation | ✅ Via skills |
| Playwright | MCP server | ✅ Available |
| Code Review | GPT + Claude tools | ✅ Available |
| Debugging | DrupalForge guide | ✅ Documented |
| Upgrades | AI Upgrade module | ✅ Available |
| Migration | Multiple AI modules | ✅ Available |
