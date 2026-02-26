# Capability Types Reference

Standard capability types for task decomposition and skill matching.

## Quick Reference

| Capability | Status | Description | Keywords |
|------------|--------|-------------|----------|
| `browser_automation` | ❌ | Web navigation, scraping | browser, puppeteer, playwright |
| `web_search` | ❌ | Search engines | search, google, bing |
| `api_integration` | ❌ | REST/GraphQL APIs | api, rest, {service} |
| `data_extraction` | ⚠️ | PDF, HTML, OCR | parse, pdf, ocr |
| `data_transformation` | ✅ | Format conversion | — |
| `content_generation` | ✅ | LLM native | — |
| `file_operations` | ⚠️ | CSV, Excel, JSON | file, csv, excel |
| `message_delivery` | ❌ | Slack, Discord, email | slack, discord, email |
| `scheduling` | ✅ | Cron, timers | — |
| `authentication` | ❌ | OAuth, tokens | oauth, auth, token |
| `database_operations` | ❌ | SQL, NoSQL | sql, mongodb, postgres |
| `code_execution` | ✅ | Scripts, shell | — |
| `version_control` | ⚠️ | Git, PRs | git, github, pr |
| `testing` | ⚠️ | Unit/E2E tests | test, jest, pytest |
| `deployment` | ❌ | Docker, K8s, CI/CD | deploy, docker, k8s |
| `monitoring` | ❌ | Logs, alerts | monitor, alert, log |

✅ Native &nbsp;|&nbsp; ⚠️ Complex needs skill &nbsp;|&nbsp; ❌ Skill required

## Capability Details

### browser_automation
**Use:** Login, form filling, scraping, screenshots
```bash
npx skills find browser puppeteer
```

### web_search
**Use:** Research, documentation, current events
```bash
npx skills find search google
```

### api_integration
**Use:** GitHub, Notion, cloud services, SaaS
```bash
npx skills find github api
npx skills find notion
```

### data_extraction
**Use:** PDF text, HTML parsing, OCR
```bash
npx skills find pdf extract
```

### data_transformation
**Use:** CSV↔JSON, data cleaning, ETL
**Note:** Native code execution handles most cases.

### content_generation
**Use:** Summarization, translation, writing
**Note:** LLM native. Search only for specialized generation.

### file_operations
**Use:** CSV/Excel, JSON/YAML, compression
```bash
npx skills find excel csv
```

### message_delivery
**Use:** Slack, Discord, email, Telegram, SMS
```bash
npx skills find slack discord
```

### scheduling
**Use:** Daily tasks, periodic automation
**Note:** Use system cron directly.

### authentication
**Use:** OAuth flows, API keys, sessions
```bash
npx skills find oauth auth
```

### database_operations
**Use:** SQL, NoSQL, data persistence
```bash
npx skills find postgres mongodb
```

### code_execution
**Use:** Scripts, shell commands, builds
**Note:** Built-in. Skills for specialized runtimes only.

### version_control
**Use:** Git ops, PR management, code review
```bash
npx skills find github pr
```

### testing
**Use:** Unit tests, E2E, test generation
```bash
npx skills find jest playwright
```

### deployment
**Use:** Docker, K8s, cloud deploy, CI/CD
```bash
npx skills find docker deploy
```

### monitoring
**Use:** Health checks, log analysis, alerting
```bash
npx skills find monitor alert
```

## Examples

### Email → Slack Digest

```yaml
- Access emails      → browser_automation
- Extract content    → data_extraction ✅
- Generate summary   → content_generation ✅
- Send to Slack      → message_delivery
```

### GitHub Issue Monitor

```yaml
- Poll GitHub        → api_integration
- Parse data         → data_extraction ✅
- Generate summary   → content_generation ✅
- Post notification  → message_delivery
- Schedule           → scheduling ✅
```

## Search

```bash
npx skills find {keyword}
npx skills find {service}
npx skills find {capability} {domain}
```

Browse: https://skills.sh/
