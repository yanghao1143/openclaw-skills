---
skill_id: "021"
category: web-development
title: Next.js 最佳实践 (Next Best Practices)
title_zh: Next.js 最佳实践
description: Next.js best practices across routing, data handling, caching and optimization from Vercel Labs
description_zh: 来自 Vercel Labs 的 Next.js 最佳实践，涵盖路由、数据处理、缓存和优化
version: "1.0.0"
tags: [nextjs, react, vercel, routing, caching, ssr]
author: vercel-labs
source: vercel-labs/next-skills
installs: 16000
created_at: "2026-02-15"
---

# Next.js 最佳实践

## 概述

来自 Vercel Labs 的 Next.js 最佳实践指南，涵盖 App Router、数据获取、缓存策略和性能优化。自动应用于 Next.js 开发中，防止常见错误。

## 适用场景

- 使用 Next.js App Router 开发
- 实现服务端渲染和数据获取
- 配置缓存策略
- 优化 Next.js 应用性能
- 部署到 Vercel 平台

## 核心规则

### App Router
- 优先使用 Server Components
- 合理划分 Server/Client 边界
- 使用 layout.tsx 共享布局
- 正确使用 loading.tsx 和 error.tsx

### 数据获取
- Server Components 中直接 fetch
- 使用 React.cache() 去重
- 合理使用 generateStaticParams
- 避免客户端瀑布流请求

### 缓存策略
- 理解 Next.js 四层缓存
- 合理设置 revalidate
- 使用 unstable_cache 缓存数据
- 按需重新验证（revalidatePath/Tag）

### 性能优化
- 使用 next/image 优化图片
- 使用 next/font 优化字体
- 合理使用 Suspense 边界
- 减少客户端 JavaScript

## 使用方式

```bash
npx skills add vercel-labs/next-skills -g -y
```
