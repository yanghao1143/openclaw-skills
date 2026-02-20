---
skill_id: "010"
category: web-development
title: React Native 开发最佳实践 (React Native Skills)
title_zh: React Native 开发最佳实践
description: React Native and Expo best practices for building performant mobile apps
description_zh: React Native 和 Expo 移动应用开发最佳实践，涵盖性能、动画、UI 模式和平台优化
version: "1.0.0"
tags: [react-native, expo, mobile, performance, animation]
author: vercel-labs
source: vercel-labs/agent-skills
installs: 34500
created_at: "2026-02-15"
---

# React Native 开发最佳实践

## 概述

React Native 和 Expo 应用的全面最佳实践指南，涵盖性能优化、动画实现、UI 模式和平台特定优化等多个类别。

## 适用场景

- 构建 React Native 或 Expo 应用
- 优化列表和滚动性能
- 使用 Reanimated 实现动画
- 处理图片和媒体资源
- 配置原生模块或字体
- 构建包含原生依赖的 Monorepo 项目

## 规则分类（按优先级）

| 优先级 | 分类 | 影响程度 | 前缀 |
|--------|------|----------|------|
| 1 | 列表性能 | 关键 | `list-performance-` |
| 2 | 动画 | 高 | `animation-` |
| 3 | 导航 | 高 | `navigation-` |
| 4 | UI 模式 | 高 | `ui-` |
| 5 | 状态管理 | 中 | `react-state-` |
| 6 | 渲染 | 中 | `rendering-` |

## 核心规则

### 列表性能（关键）

- 使用 `FlashList` 替代 `FlatList` 获得更好的性能
- 设置合理的 `estimatedItemSize` 减少布局计算
- 避免在 `renderItem` 中创建内联函数
- 使用 `getItemType` 区分不同类型的列表项

### 动画（高）

- 优先使用 Reanimated 的 `useAnimatedStyle` 而非 Animated API
- 在 UI 线程运行动画，避免 JS 线程阻塞
- 使用 `withSpring` 和 `withTiming` 创建流畅动画
- 手势动画使用 `react-native-gesture-handler`

### 导航（高）

- 使用 Expo Router 进行文件系统路由
- 预加载相邻页面提升导航速度
- 合理使用 `Stack`、`Tabs` 和 `Drawer` 导航器

### UI 模式（高）

- 使用 `SafeAreaView` 适配不同设备
- 响应式布局使用 `useWindowDimensions`
- 平台特定代码使用 `Platform.select()`
