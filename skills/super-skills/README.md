# Super Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://skills.sh/)

A meta-skill for decomposing complex requests into executable subtasks, identifying capabilities, searching skills, and creating new skills when needed.

## Features

- **Task Decomposition** — Break complex requests into atomic tasks
- **Capability Mapping** — Map tasks to universal capability types
- **Skill Search** — Find existing skills in the ecosystem
- **Gap Analysis** — Identify missing capabilities
- **Skill Creation** — Generate new skills when needed

## Installation

```bash
npx clawhub@latest install super-skills     # ClawHub (Recommended)
npx skills add anthropics/super-skills -g   # Skills CLI
```

## Quick Start

```
Analyze → Decompose → Search → Fill Gaps → Execute
```

## Capability Reference

| Capability | Status | Search Keywords |
|------------|--------|-----------------|
| `browser_automation` | ❌ | browser, puppeteer, playwright |
| `api_integration` | ❌ | api, rest, {service} |
| `message_delivery` | ❌ | slack, discord, email |
| `data_extraction` | ⚠️ | pdf, ocr, parse |
| `content_generation` | ✅ | — |
| `scheduling` | ✅ | — |

✅ Built-in &nbsp;|&nbsp; ⚠️ Complex needs skill &nbsp;|&nbsp; ❌ Skill required

## Example

**Request:** "Monitor GitHub issues and notify Discord"

| Task | Capability | Status |
|------|------------|--------|
| Poll GitHub API | `api_integration` | 🔧 |
| Parse issue data | `data_extraction` | ✅ |
| Format message | `content_generation` | ✅ |
| Send to Discord | `message_delivery` | 🔧 |

## Commands

```bash
# Search
npx skills find <keyword>
npx clawhub@latest search <keyword>

# Install
npx clawhub@latest install <skill>
npx skills add <skill> -g

# Create
npx skills init <name>
```

**Browse:** [skills.sh](https://skills.sh/) · [clawhub.com](https://clawhub.com/)

## Principles

- **Atomicity** — One task = one action
- **Independence** — Minimize dependencies
- **Verifiability** — Clear success criteria
- **Reusability** — Prefer general solutions

## Structure

```
super-skills/
├── SKILL.md                    # Main definition
├── references/
│   └── capability_types.md     # Capability reference
└── assets/
    └── skill_template.md       # New skill template
```

## License

MIT
