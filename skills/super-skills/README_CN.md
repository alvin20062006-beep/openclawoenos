# Super Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://skills.sh/)

一个元技能，用于将复杂请求分解为可执行的子任务，识别所需能力，搜索生态系统，并在需要时创建新技能。

## 功能特性

- **任务分解** — 将复杂请求拆分为原子任务
- **能力映射** — 将任务映射到通用能力类型
- **技能搜索** — 在生态系统中查找现有技能
- **差距分析** — 识别缺失的能力
- **技能创建** — 在需要时生成新技能

## 安装

```bash
npx clawhub@latest install super-skills     # ClawHub（推荐）
npx skills add anthropics/super-skills -g   # Skills CLI
```

## 快速开始

```
分析 → 分解 → 搜索 → 填补空白 → 执行
```

## 能力参考

| 能力类型 | 状态 | 搜索关键词 |
|----------|------|------------|
| `browser_automation` | ❌ | browser, puppeteer, playwright |
| `api_integration` | ❌ | api, rest, {服务名} |
| `message_delivery` | ❌ | slack, discord, email |
| `data_extraction` | ⚠️ | pdf, ocr, parse |
| `content_generation` | ✅ | — |
| `scheduling` | ✅ | — |

✅ 内置 &nbsp;|&nbsp; ⚠️ 复杂场景需技能 &nbsp;|&nbsp; ❌ 需要技能

## 示例

**请求：** "监控 GitHub Issues 并通知 Discord"

| 任务 | 能力 | 状态 |
|------|------|------|
| 轮询 GitHub API | `api_integration` | 🔧 |
| 解析 Issue 数据 | `data_extraction` | ✅ |
| 格式化消息 | `content_generation` | ✅ |
| 发送到 Discord | `message_delivery` | 🔧 |

## 常用命令

```bash
# 搜索
npx skills find <关键词>
npx clawhub@latest search <关键词>

# 安装
npx clawhub@latest install <技能>
npx skills add <技能> -g

# 创建
npx skills init <名称>
```

**浏览：** [skills.sh](https://skills.sh/) · [clawhub.com](https://clawhub.com/)

## 分解原则

- **原子性** — 一个任务 = 一个动作
- **独立性** — 最小化依赖
- **可验证性** — 明确的成功标准
- **可复用性** — 优先通用方案

## 目录结构

```
super-skills/
├── SKILL.md                    # 主技能定义
├── references/
│   └── capability_types.md     # 能力类型参考
└── assets/
    └── skill_template.md       # 新技能模板
```

## 许可证

MIT
