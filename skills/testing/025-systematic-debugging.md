---
skill_id: "025"
category: testing
title: 系统化调试方法 (Systematic Debugging)
title_zh: 系统化调试方法
description: Systematic debugging methodology that ensures root cause analysis before fixes to prevent trial-and-error approaches
description_zh: 系统化调试方法论，确保在修复前进行根因分析，避免试错式修复
version: "1.0.0"
tags: [debugging, testing, root-cause, methodology, troubleshooting]
author: obra
source: obra/superpowers
installs: 13600
created_at: "2026-02-15"
---

# 系统化调试方法

## 概述

系统化调试技能强制执行"先找根因，再修复"的原则。随机修复浪费时间并制造新 Bug，快速补丁掩盖底层问题。此技能提供结构化的调试流程。

## 适用场景

- 遇到不明确的错误
- 间歇性/不稳定的 Bug
- 回归问题排查
- 复杂的多模块问题
- 性能问题定位

## 调试流程

### 1. 收集信息
- 复现问题的步骤
- 错误日志和堆栈跟踪
- 环境信息（OS、版本、配置）
- 最近的代码变更

### 2. 形成假设
- 基于证据提出 2-3 个可能的原因
- 按可能性排序
- 设计验证实验

### 3. 验证假设
- 逐一验证每个假设
- 使用最小化复现用例
- 记录验证结果

### 4. 修复和验证
- 针对根因编写修复
- 编写回归测试
- 验证修复不引入新问题

## 核心原则

| 原则 | 说明 |
|------|------|
| 先理解再修复 | 不理解问题就不要动手修 |
| 一次改一个变量 | 避免同时修改多处 |
| 用数据说话 | 日志、断点、测试，不靠猜 |
| 写回归测试 | 确保问题不再复发 |

## 使用方式

```bash
npx skills add obra/superpowers -g -y
```
