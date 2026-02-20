---
skill_id: "004"
category: other
title: Remotion 视频创作知识库 (Remotion Best Practices)
title_zh: Remotion 视频创作知识库
description: Best practices for creating programmatic videos with Remotion in React, covering assets, timing, transitions and captions
description_zh: 使用 Remotion 在 React 中创建程序化视频的最佳实践，涵盖资源管理、时间控制、转场效果和字幕
version: "1.0.0"
tags: [remotion, video, react, animation, programmatic-video]
author: remotion-dev
source: remotion-dev/skills
installs: 95200
created_at: "2026-02-15"
---

# Remotion 视频创作知识库

## 概述

Remotion 是一个强大的框架，允许你使用 React 以编程方式创建视频。此技能提供 Remotion 项目的最佳实践，涵盖资源管理、时间控制、转场效果、字幕等核心主题。

## 适用场景

- 使用 React 创建程序化视频
- 批量生成数据驱动的视频内容
- 创建动画演示、教程视频
- 构建自动化视频生产流水线
- 需要精确控制视频时间轴和动画

## 核心概念

### 1. 项目结构

```
my-video/
├── src/
│   ├── Root.tsx          # 注册所有 Composition
│   ├── compositions/     # 视频组件
│   │   ├── MyVideo.tsx
│   │   └── Intro.tsx
│   ├── components/       # 可复用组件
│   └── assets/           # 静态资源
├── public/               # 公共资源
└── remotion.config.ts    # Remotion 配置
```

### 2. 时间控制（Timing）

- 使用 `useCurrentFrame()` 获取当前帧
- 使用 `useVideoConfig()` 获取 fps、宽高等配置
- 使用 `<Sequence>` 组件控制时间段
- 使用 `interpolate()` 创建平滑动画

```tsx
import { useCurrentFrame, interpolate } from 'remotion';

const MyComponent = () => {
  const frame = useCurrentFrame();
  const opacity = interpolate(frame, [0, 30], [0, 1], {
    extrapolateRight: 'clamp',
  });
  return <div style={{ opacity }}>淡入效果</div>;
};
```

### 3. 资源管理（Assets）

- 使用 `staticFile()` 引用 public 目录资源
- 使用 `<Img>` 组件替代 `<img>` 确保资源加载完成
- 使用 `<Audio>` 和 `<Video>` 组件处理媒体
- 使用 `delayRender()` / `continueRender()` 等待异步资源

### 4. 转场效果（Transitions）

- 使用 `@remotion/transitions` 包
- 内置效果：fade, slide, wipe, flip
- 可自定义转场动画
- 使用 `<TransitionSeries>` 组件串联场景

### 5. 字幕（Captions）

- 使用 `@remotion/captions` 处理字幕
- 支持 SRT、VTT 格式导入
- 逐字/逐句动画效果
- 自定义字幕样式和位置

### 6. 渲染与导出

```bash
# 本地预览
npx remotion preview

# 渲染视频
npx remotion render MyComposition out/video.mp4

# 渲染 GIF
npx remotion render MyComposition out/animation.gif --image-format png

# 服务端渲染
npx remotion lambda render ...
```

## 最佳实践

| 实践 | 说明 |
|------|------|
| 使用 `<Sequence>` | 组织时间线，避免手动计算帧 |
| 使用 `spring()` | 创建自然的弹性动画 |
| 预加载资源 | 使用 `preloadVideo()` / `preloadAudio()` |
| 避免 `useEffect` | Remotion 渲染是确定性的，不需要副作用 |
| 使用 `calculateMetadata` | 动态计算视频时长和参数 |

## 使用方式

```bash
# 安装技能
npx skills add remotion-dev/skills -g -y

# 创建 Remotion 项目
npx create-video@latest
```
