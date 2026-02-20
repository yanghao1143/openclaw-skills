---
skill_id: "005"
category: design
title: 前端界面设计指南 (Frontend Design)
title_zh: 前端界面设计指南
description: Create distinctive, production-grade frontend interfaces with high design quality that avoid generic AI aesthetics
description_zh: 创建独特的、生产级前端界面，具有高设计质量，避免千篇一律的 AI 生成风格
version: "1.0.0"
tags: [frontend, design, ui, css, components, aesthetics]
author: anthropics
source: anthropics/skills
installs: 203700
created_at: "2026-02-15"
---

# 前端界面设计指南

## 概述

前端界面设计指南帮助创建独特的、生产级前端界面，避免千篇一律的"AI 生成风格"。当用户要求构建 Web 组件、页面、仪表盘、表单、落地页或任何 UI 时，此技能会被触发。

## 适用场景

- 构建 Web 组件、页面或应用
- 创建落地页、仪表盘、表单
- 设计 React 组件或 HTML/CSS 布局
- 美化和优化现有 Web UI
- 需要高质量视觉设计的前端项目

## 核心设计原则

### 1. 确立设计方向

- 选择一个明确的美学方向并坚持到底
- 避免"什么都有一点"的混搭风格
- 定义设计令牌（Design Tokens）：颜色、字体、间距、圆角
- 建立一致的视觉语言

### 2. 排版系统（Typography）

- 选择有个性的字体组合（标题 + 正文）
- 建立清晰的字体层级（h1-h6, body, caption）
- 行高、字间距精心调整
- 中文排版注意：字体回退、标点挤压、段落间距

### 3. 色彩系统（Color System）

- 定义主色、辅助色、中性色、语义色
- 确保 WCAG AA 对比度标准
- 支持亮色/暗色主题切换
- 使用 CSS 自定义属性管理颜色

### 4. 间距与布局（Spacing & Layout）

- 使用 4px/8px 基准网格
- 一致的间距比例（xs, sm, md, lg, xl）
- CSS Grid 和 Flexbox 合理搭配
- 响应式断点设计

### 5. 组件设计（Component Design）

- 原子化设计：从基础元素到复合组件
- 状态完整：default, hover, active, focus, disabled, loading, error
- 交互反馈：微动画、过渡效果
- 无障碍：键盘导航、屏幕阅读器支持

### 6. 动效与过渡（Motion & Transitions）

- 有目的的动画，不是装饰
- 遵循物理运动规律（缓入缓出）
- 尊重 `prefers-reduced-motion`
- 加载状态使用骨架屏而非旋转图标

## 避免的常见问题

| 问题 | 正确做法 |
|------|----------|
| 默认 Tailwind 样式 | 自定义设计令牌 |
| 纯白背景 + 蓝色按钮 | 有个性的配色方案 |
| 所有圆角都是 8px | 根据层级使用不同圆角 |
| 无过渡效果 | 添加微妙的 hover/focus 过渡 |
| 忽略暗色模式 | 从一开始就支持主题切换 |

## 实战示例

```css
/* 设计令牌示例 */
:root {
  --color-primary: #2563eb;
  --color-surface: #fafafa;
  --color-text: #1a1a2e;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --space-unit: 8px;
  --font-heading: 'Inter', sans-serif;
  --font-body: 'Noto Sans SC', sans-serif;
}

/* 按钮组件 */
.btn-primary {
  background: var(--color-primary);
  border-radius: var(--radius-md);
  padding: calc(var(--space-unit) * 1.5) calc(var(--space-unit) * 3);
  transition: all 0.2s ease;
}

.btn-primary:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
}
```

## 使用方式

```bash
# 安装技能
npx skills add anthropics/skills@frontend-design -g -y
```
