---
skill_id: "002"
category: web-development
title: React/Next.js 性能优化指南 (Vercel React Best Practices)
title_zh: React/Next.js 性能优化指南
description: React and Next.js performance optimization guidelines from Vercel Engineering with 57 rules across 8 categories
description_zh: 来自 Vercel 工程团队的 React 和 Next.js 性能优化指南，包含 8 大类 57 条规则
version: "1.0.0"
tags: [react, nextjs, performance, optimization, vercel]
author: vercel-labs
source: vercel-labs/agent-skills
installs: 149400
created_at: "2026-02-15"
---

# React/Next.js 性能优化指南

## 概述

来自 Vercel 工程团队的全面性能优化指南，适用于 React 和 Next.js 应用。包含 8 大类 57 条规则，按影响程度排序，指导自动化重构和代码生成。

## 适用场景

- 编写新的 React 组件或 Next.js 页面
- 实现数据获取（客户端或服务端）
- 审查代码的性能问题
- 重构现有 React/Next.js 代码
- 优化打包体积或加载时间

## 规则分类（按优先级）

| 优先级 | 分类 | 影响程度 | 前缀 |
|--------|------|----------|------|
| 1 | 消除瀑布流 | 关键 | `async-` |
| 2 | 打包体积优化 | 关键 | `bundle-` |
| 3 | 服务端性能 | 高 | `server-` |
| 4 | 客户端数据获取 | 中高 | `client-` |
| 5 | 重渲染优化 | 中 | `rerender-` |
| 6 | 渲染性能 | 中 | `rendering-` |
| 7 | JavaScript 性能 | 中低 | `js-` |
| 8 | 高级模式 | 低 | `advanced-` |

## 核心规则速查

### 1. 消除瀑布流（关键）

- `async-defer-await` — 将 await 移到实际使用的分支中
- `async-parallel` — 对独立操作使用 Promise.all()
- `async-dependencies` — 对部分依赖使用 better-all
- `async-api-routes` — 在 API 路由中尽早启动 Promise，延迟 await
- `async-suspense-boundaries` — 使用 Suspense 流式传输内容

### 2. 打包体积优化（关键）

- `bundle-barrel-imports` — 直接导入，避免桶文件
- `bundle-dynamic-imports` — 对重型组件使用 next/dynamic
- `bundle-defer-third-party` — 在 hydration 后加载分析/日志
- `bundle-conditional` — 仅在功能激活时加载模块
- `bundle-preload` — 在 hover/focus 时预加载以提升感知速度

### 3. 服务端性能（高）

- `server-auth-actions` — 像 API 路由一样认证 Server Actions
- `server-cache-react` — 使用 React.cache() 进行请求级去重
- `server-cache-lru` — 使用 LRU 缓存进行跨请求缓存
- `server-dedup-props` — 避免 RSC props 中的重复序列化
- `server-serialization` — 最小化传递给客户端组件的数据

### 4. 客户端数据获取（中高）

- `client-swr` — 使用 SWR 进行客户端数据获取
- `client-optimistic` — 使用乐观更新提升感知速度

### 5. 重渲染优化（中）

- `rerender-context-split` — 拆分 Context 避免不必要的重渲染
- `rerender-memo` — 合理使用 React.memo 和 useMemo
