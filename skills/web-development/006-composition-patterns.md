---
skill_id: "006"
category: web-development
title: React 组合模式 (Vercel Composition Patterns)
title_zh: React 组合模式
description: React composition patterns that scale for building flexible component libraries
description_zh: 构建灵活可扩展 React 组件的组合模式指南
version: "1.0.0"
tags: [react, composition, patterns, components, architecture]
author: vercel-labs
source: vercel-labs/agent-skills
installs: 48600
created_at: "2026-02-15"
---

# React 组合模式

## 概述

用于构建灵活、可维护 React 组件的组合模式指南。通过复合组件、状态提升和内部组合来避免布尔属性泛滥，使代码库在扩展时更易于人类和 AI Agent 理解。

## 适用场景

- 重构包含大量布尔属性的组件
- 构建可复用的组件库
- 设计灵活的组件 API
- 审查组件架构
- 使用复合组件或 Context Provider

## 规则分类（按优先级）

| 优先级 | 分类 | 影响程度 | 前缀 |
|--------|------|----------|------|
| 1 | 组件架构 | 高 | `architecture-` |
| 2 | 状态管理 | 中 | `state-` |
| 3 | 实现模式 | 中 | `patterns-` |
| 4 | React 19 API | 中 | `react19-` |

## 核心模式

### 复合组件模式

将一个复杂组件拆分为多个协作的子组件，通过 Context 共享状态：

```jsx
// ❌ 布尔属性泛滥
<Card showHeader showFooter showAvatar isCompact hasActions />

// ✅ 复合组件
<Card>
  <Card.Header>
    <Card.Avatar />
  </Card.Header>
  <Card.Body>内容</Card.Body>
  <Card.Footer>
    <Card.Actions />
  </Card.Footer>
</Card>
```

### 状态提升

将共享状态提升到最近的公共祖先，避免 prop drilling：

```jsx
// ✅ 状态提升 + Context
const FormContext = createContext();

function Form({ children }) {
  const [values, setValues] = useState({});
  return (
    <FormContext.Provider value={{ values, setValues }}>
      {children}
    </FormContext.Provider>
  );
}
```

### React 19 新特性

- `use()` Hook — 在组件中读取 Promise 和 Context
- Server Components — 默认在服务端渲染
- Actions — 简化表单提交和数据变更
- `useOptimistic` — 乐观更新 UI
