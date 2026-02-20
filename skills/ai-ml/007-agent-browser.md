---
skill_id: "007"
category: ai-ml
title: 浏览器自动化工具 (Agent Browser)
title_zh: 浏览器自动化工具
description: Automates browser interactions for web testing, form filling, screenshots, and data extraction
description_zh: 自动化浏览器交互，用于 Web 测试、表单填写、截图和数据提取
version: "1.0.0"
tags: [browser, automation, testing, scraping, agent]
author: vercel-labs
source: vercel-labs/agent-browser
installs: 112800
created_at: "2026-02-15"
---

# 浏览器自动化工具

## 概述

浏览器自动化工具是一个为 AI Agent 设计的无头浏览器自动化 CLI。当用户需要浏览网站、与网页交互、填写表单、截图、测试 Web 应用或从网页提取信息时，此技能会被触发。

## 适用场景

- 浏览和导航网站
- 填写和提交表单
- 截取网页截图
- 测试 Web 应用功能
- 从网页提取数据
- 自动化重复的浏览器操作

## 核心功能

### 1. 页面导航

```bash
# 打开网页
agent-browser navigate https://example.com

# 等待页面加载完成
agent-browser navigate https://example.com --wait-for-load
```

### 2. 元素交互

- 点击按钮和链接
- 输入文本到表单字段
- 选择下拉选项
- 勾选/取消复选框
- 滚动页面

### 3. 数据提取

- 获取页面文本内容
- 提取表格数据
- 读取元素属性
- 获取页面 HTML 结构

### 4. 截图与视觉

```bash
# 全页截图
agent-browser screenshot --full-page

# 指定元素截图
agent-browser screenshot --selector ".main-content"
```

### 5. 元素引用系统

工具使用确定性引用 ID（如 @e1, @e2 等）标识页面元素，便于 Agent 精确操作：

```
@e1 <button> "登录"
@e2 <input> [name="username"]
@e3 <input> [name="password"]
@e4 <a> "忘记密码？"
```

## 使用方式

```bash
# 安装
npx skills add vercel-labs/agent-browser -g -y

# 基本使用
agent-browser navigate https://example.com
agent-browser click @e1
agent-browser type @e2 "hello world"
agent-browser screenshot
```

## 常见用例

| 用例 | 命令示例 |
|------|----------|
| 登录测试 | navigate → type username → type password → click login |
| 数据采集 | navigate → extract table → save to file |
| UI 测试 | navigate → screenshot → compare baseline |
| 表单自动填写 | navigate → fill fields → submit → verify |

## 注意事项

- 仅用于合法的自动化测试和数据提取
- 遵守目标网站的 robots.txt 和使用条款
- 避免过于频繁的请求，设置合理的延迟
- 敏感操作（如支付）需要人工确认
