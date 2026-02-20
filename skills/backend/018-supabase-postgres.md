---
skill_id: "018"
category: backend
title: Supabase Postgres 最佳实践 (Supabase Postgres Best Practices)
title_zh: Supabase Postgres 最佳实践
description: Postgres performance optimization and best practices from Supabase covering queries, schemas, RLS and connection handling
description_zh: 来自 Supabase 的 Postgres 性能优化最佳实践，涵盖查询优化、Schema 设计、RLS 和连接管理
version: "1.0.0"
tags: [postgres, supabase, database, sql, optimization, rls]
author: supabase
source: supabase/agent-skills
installs: 21000
created_at: "2026-02-15"
---

# Supabase Postgres 最佳实践

## 概述

来自 Supabase 团队的 Postgres 最佳实践指南，帮助 AI Agent 编写更高质量的数据库代码。按影响优先级分为 8 大类，涵盖查询性能、连接处理、行级安全等核心主题。

## 适用场景

- 编写或审查 Postgres 查询
- 设计数据库 Schema
- 配置 Supabase 项目
- 优化数据库性能
- 实现行级安全（RLS）策略

## 规则分类（按优先级）

### 1. 查询性能
- 使用适当的索引
- 避免 SELECT *
- 使用 EXPLAIN ANALYZE 分析查询
- 批量操作替代逐行操作

### 2. 连接管理
- 使用连接池（PgBouncer）
- 合理设置连接超时
- 避免连接泄漏

### 3. Schema 设计
- 选择正确的数据类型
- 合理使用约束
- 规范化 vs 反规范化权衡
- 使用 UUID 作为主键

### 4. 行级安全（RLS）
- 为所有表启用 RLS
- 编写高效的 RLS 策略
- 避免 RLS 性能陷阱
- 测试 RLS 策略

### 5. 迁移管理
- 使用事务性迁移
- 避免锁表操作
- 渐进式 Schema 变更

## 使用方式

```bash
npx skills add supabase/agent-skills -g -y
```
