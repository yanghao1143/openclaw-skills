---
skill_id: "001"
category: web-development
title: 技能搜索工具 (Find Skills)
title_zh: 技能搜索工具
description: Helps users discover and install agent skills from the open ecosystem
description_zh: 帮助用户发现和安装 AI Agent 技能的搜索工具
version: "1.0.0"
tags: [skills, search, discovery, cli, agent]
author: vercel-labs
source: vercel-labs/skills
installs: 272500
created_at: "2026-02-15"
---

# 技能搜索工具 (Find Skills)

## 概述

技能搜索工具帮助用户从开放的 Agent 技能生态系统中发现和安装技能。当用户询问"如何做 X"、"有没有做 X 的技能"或希望扩展 Agent 能力时，此技能会被触发。

## 使用场景

- 用户询问"如何做 X"，而 X 可能有现成的技能
- 用户说"帮我找一个做 X 的技能"
- 用户想搜索工具、模板或工作流
- 用户希望扩展 Agent 的专业能力

## Skills CLI 简介

Skills CLI (`npx skills`) 是开放 Agent 技能生态的包管理器。技能是模块化的包，通过专业知识、工作流和工具扩展 Agent 的能力。

### 核心命令

| 命令 | 说明 |
|------|------|
| `npx skills find [query]` | 交互式搜索或按关键词搜索技能 |
| `npx skills add <package>` | 从 GitHub 或其他来源安装技能 |
| `npx skills check` | 检查技能更新 |
| `npx skills update` | 更新所有已安装的技能 |

### 浏览技能目录

访问 https://skills.sh/ 浏览所有可用技能。

## 搜索技巧

### 常见技能分类

| 分类 | 搜索关键词示例 |
|------|----------------|
| Web 开发 | react, nextjs, typescript, css, tailwind |
| 测试 | testing, jest, playwright, e2e |
| DevOps | deploy, docker, kubernetes, ci-cd |
| 文档 | docs, readme, changelog, api-docs |
| 代码质量 | review, lint, refactor, best-practices |
| 设计 | ui, ux, design-system, accessibility |
| 生产力 | workflow, automation, git |

### 搜索建议

1. 使用具体关键词："react testing" 比单独的 "testing" 效果更好
2. 尝试替代词：如果 "deploy" 没结果，试试 "deployment" 或 "ci-cd"
3. 查看热门来源：许多技能来自 `vercel-labs/agent-skills` 或 `anthropics/skills`

## 安装示例

```bash
# 搜索技能
npx skills find react performance

# 安装技能（全局安装，跳过确认）
npx skills add vercel-labs/agent-skills@vercel-react-best-practices -g -y
```

## 未找到技能时

如果没有找到相关技能：
1. 告知用户没有找到现有技能
2. 提供直接帮助
3. 建议用户创建自己的技能：`npx skills init my-skill`
