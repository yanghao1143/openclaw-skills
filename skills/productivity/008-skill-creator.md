---
skill_id: "008"
category: productivity
title: 技能创建指南 (Skill Creator)
title_zh: 技能创建指南
description: Guide for creating effective skills that extend AI agent capabilities with specialized knowledge, workflows, or tool integrations
description_zh: 创建高效技能的指南，通过专业知识、工作流或工具集成扩展 AI Agent 的能力
version: "1.0.0"
tags: [skills, creator, guide, meta, agent, workflow]
author: anthropics
source: anthropics/skills
installs: 167500
created_at: "2026-02-15"
---

# 技能创建指南

## 概述

技能创建指南是一个"元技能"（Meta Skill），帮助用户创建或更新能够扩展 AI Agent 能力的技能。当用户想要创建新技能或更新现有技能时，此技能会被触发。

## 适用场景

- 创建全新的 Agent 技能
- 更新和改进现有技能
- 设计技能的结构和工作流
- 打包专业知识为可复用的技能
- 集成外部工具到技能中

## 技能文件结构

### SKILL.md 基本结构

```markdown
---
name: my-skill
description: 简短描述技能的用途和触发条件
---

# 技能名称

## 概述
技能的详细描述和使用场景

## 核心指令
Agent 应遵循的具体指令

## 参考资料
相关文档和链接
```

### 前置元数据（Frontmatter）

| 字段 | 必填 | 说明 |
|------|------|------|
| `name` | 是 | 技能的唯一标识符（kebab-case） |
| `description` | 是 | 简短描述，包含触发条件 |
| `version` | 否 | 语义化版本号 |
| `tags` | 否 | 分类标签 |

## 创建技能的步骤

### 1. 确定技能范围

- 明确技能要解决的问题
- 定义触发条件（用户说什么时激活）
- 确定输入和输出格式
- 划定技能边界（不做什么）

### 2. 编写核心指令

- 使用清晰、具体的语言
- 提供步骤化的操作流程
- 包含示例和模板
- 定义错误处理策略

### 3. 添加参考资料

- 链接到相关文档
- 提供代码示例
- 包含常见问题解答
- 添加最佳实践建议

### 4. 测试和迭代

- 在真实场景中测试技能
- 收集用户反馈
- 持续改进指令质量
- 更新版本号

## 技能设计原则

| 原则 | 说明 |
|------|------|
| 单一职责 | 每个技能只做一件事 |
| 渐进式披露 | 从简单到复杂，按需展开 |
| 可组合性 | 技能之间可以协作 |
| 幂等性 | 多次执行结果一致 |
| 容错性 | 优雅处理异常情况 |

## 发布技能

```bash
# 初始化技能项目
npx skills init my-skill

# 本地测试
npx skills test my-skill

# 发布到 GitHub
git init && git add . && git commit -m "Initial skill"
git remote add origin https://github.com/user/my-skill
git push -u origin main
```

## 使用方式

```bash
# 安装技能
npx skills add anthropics/skills@skill-creator -g -y
```
