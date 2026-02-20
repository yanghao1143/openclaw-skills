---
skill_id: "003"
category: design
title: Web 界面设计规则审查工具 (Web Design Guidelines)
title_zh: Web 界面设计规则审查工具
description: Review UI code for Web Interface Guidelines compliance including accessibility, keyboard support, form behavior, animation and performance
description_zh: 审查 UI 代码是否符合 Web 界面设计规范，涵盖无障碍访问、键盘支持、表单行为、动画和性能等方面
version: "1.0.0"
tags: [design, ui, ux, accessibility, review, audit, web-guidelines]
author: vercel-labs
source: vercel-labs/agent-skills
installs: 186300
created_at: "2026-02-15"
---

# Web 界面设计规则审查工具

## 概述

Web 界面设计规则审查工具用于检查 UI 代码是否符合 Web 界面设计规范。当用户要求"审查我的 UI"、"检查无障碍性"、"审计设计"、"审查 UX"或"对照最佳实践检查我的网站"时，此技能会被触发。

## 适用场景

- 用户要求审查 UI 代码的合规性
- 检查网站的无障碍访问（Accessibility）
- 审计设计系统的一致性
- 审查用户体验（UX）问题
- 对照 Web 最佳实践进行检查

## 审查规则分类

### 1. 无障碍访问（Accessibility）

- 语义化 HTML 标签使用
- ARIA 属性正确性
- 颜色对比度检查
- 屏幕阅读器兼容性
- 替代文本（alt text）完整性
- 焦点管理和焦点可见性

### 2. 键盘支持（Keyboard Support）

- 所有交互元素可通过键盘访问
- Tab 顺序合理
- 快捷键不与系统冲突
- 焦点陷阱（Focus Trap）正确实现
- Escape 键关闭弹窗/下拉

### 3. 表单行为（Form Behavior）

- 表单验证反馈清晰
- 错误信息关联到对应字段
- 必填字段标识明确
- 提交状态反馈（loading/success/error）
- 自动填充（autocomplete）属性正确

### 4. 动画与过渡（Animation）

- 尊重 `prefers-reduced-motion` 设置
- 动画时长合理（200-500ms）
- 避免闪烁和抖动
- 过渡效果平滑自然
- 加载动画提供进度反馈

### 5. 性能（Performance）

- 图片懒加载和尺寸优化
- 关键 CSS 内联
- 字体加载策略（font-display）
- 避免布局偏移（CLS）
- 首屏内容优先加载

### 6. 响应式设计（Responsive）

- 移动端优先的断点设计
- 触摸目标尺寸 ≥ 44px
- 视口元标签正确设置
- 图片响应式适配
- 文字可缩放不溢出

## 审查输出格式

审查结果以简洁的 `文件:行号` 格式输出，便于快速定位和修复：

```
src/components/Button.tsx:15 — 缺少 aria-label 属性
src/pages/Home.tsx:42 — 颜色对比度不足 (2.1:1, 需要 4.5:1)
src/components/Modal.tsx:8 — 缺少焦点陷阱实现
```

## 使用方式

```bash
# 安装技能
npx skills add vercel-labs/agent-skills@web-design-guidelines -g -y

# 触发审查
# 在 Agent 对话中说："审查我的 UI" 或 "检查无障碍性"
```

## 常见问题修复建议

| 问题 | 修复方案 |
|------|----------|
| 缺少 alt 文本 | 为所有 `<img>` 添加描述性 alt |
| 对比度不足 | 使用 WCAG AA 标准调整颜色 |
| 键盘不可访问 | 使用语义化标签或添加 tabindex |
| 动画过快 | 设置 duration ≥ 200ms |
| 布局偏移 | 为图片/视频设置固定宽高 |
