---
skill_id: "035"
category: testing
title: 测试驱动开发 (Test Driven Development)
title_zh: 测试驱动开发
description: Enforce TDD workflow with write tests first, implement code, then refactor cycle for reliable software
description_zh: 强制执行 TDD 工作流：先写测试、再实现代码、最后重构，确保软件可靠性
version: "1.0.0"
tags: [tdd, testing, methodology, quality, refactoring]
author: obra
source: obra/superpowers
installs: 11100
created_at: "2026-02-15"
---

# 测试驱动开发

## 概述

测试驱动开发（TDD）技能强制执行"红-绿-重构"循环：先编写失败的测试，再编写最少代码使测试通过，最后重构代码。防止 AI Agent 跳过测试直接写代码。

## 适用场景

- 新功能开发
- Bug 修复（先写复现测试）
- 代码重构（先确保测试覆盖）
- API 开发
- 核心业务逻辑实现

## TDD 循环

### 1. 红（Red）
- 编写一个失败的测试
- 测试应描述期望的行为
- 运行测试确认失败

### 2. 绿（Green）
- 编写最少的代码使测试通过
- 不要过度设计
- 运行测试确认通过

### 3. 重构（Refactor）
- 改善代码结构和可读性
- 消除重复
- 运行测试确认仍然通过

## 核心原则

| 原则 | 说明 |
|------|------|
| 测试先行 | 永远先写测试 |
| 最小实现 | 只写让测试通过的最少代码 |
| 小步前进 | 每次只添加一个测试 |
| 持续重构 | 每个绿灯后考虑重构 |

## 使用方式

```bash
npx skills add obra/superpowers -g -y
```
