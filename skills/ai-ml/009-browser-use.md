---
skill_id: "009"
category: ai-ml
title: 浏览器使用技能 (Browser Use)
title_zh: 浏览器使用技能
description: Automates browser interactions across sessions for web testing, form filling, screenshots, and data extraction
description_zh: 跨会话自动化浏览器交互，用于 Web 测试、表单填写、截图和数据提取
version: "1.0.0"
tags: [browser, automation, testing, scraping, session, browser-use]
author: browser-use
source: browser-use/browser-use
installs: 89600
created_at: "2026-02-15"
---

# 浏览器使用技能

## 概述

Browser Use 是一个开源的浏览器自动化框架，专为 AI Agent 设计。它支持跨会话的浏览器交互，包括 Web 测试、表单填写、截图和数据提取。与 Agent Browser 类似但更侧重于会话持久化和复杂工作流。

## 适用场景

- 需要跨多个页面的复杂浏览器操作
- 持久化会话的自动化任务
- Web 应用端到端测试
- 批量数据采集和处理
- 需要登录状态保持的操作

## 核心功能

### 1. 会话管理

- 创建和管理浏览器会话
- 会话状态持久化（Cookie、LocalStorage）
- 多标签页支持
- 会话恢复和续接

### 2. 页面交互

```python
from browser_use import Agent

agent = Agent(
    task="登录网站并提取数据",
    llm=your_llm,
)

result = await agent.run()
```

### 3. 智能元素识别

- 自动识别页面交互元素
- 基于语义理解定位元素
- 处理动态加载的内容
- 支持 iframe 和 Shadow DOM

### 4. 数据提取

- 结构化数据提取
- 表格数据解析
- 文本内容获取
- 截图和视觉分析

## 与 Agent Browser 的区别

| 特性 | Browser Use | Agent Browser |
|------|-------------|---------------|
| 会话持久化 | ✅ 支持 | ❌ 不支持 |
| 编程语言 | Python | CLI (Node.js) |
| 多标签页 | ✅ 支持 | 有限支持 |
| LLM 集成 | 内置 Agent 循环 | 外部调用 |
| 适用场景 | 复杂工作流 | 简单自动化 |

## 安装与配置

```bash
# 安装
pip install browser-use

# 或作为技能安装
npx skills add browser-use/browser-use -g -y
```

## 使用示例

### 基本用法

```python
from browser_use import Agent
from langchain_openai import ChatOpenAI

agent = Agent(
    task="搜索 Python 最新版本并返回版本号",
    llm=ChatOpenAI(model="gpt-4o"),
)

result = await agent.run()
print(result)
```

### 带会话的用法

```python
from browser_use import Agent, Browser

browser = Browser()
agent = Agent(
    task="登录后台并导出报表",
    llm=your_llm,
    browser=browser,
)

# 第一次运行：登录
await agent.run()

# 第二次运行：复用登录状态
agent2 = Agent(
    task="查看最新订单",
    llm=your_llm,
    browser=browser,  # 复用同一浏览器实例
)
await agent2.run()
```

## 注意事项

- 遵守目标网站的使用条款
- 设置合理的请求间隔
- 敏感操作需要人工确认
- 注意数据隐私和安全
