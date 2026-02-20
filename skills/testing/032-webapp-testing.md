---
skill_id: "032"
category: testing
title: Web 应用测试工具 (Webapp Testing)
title_zh: Web 应用测试工具
description: Toolkit for testing local web applications using Playwright with screenshots, browser logs and UI verification
description_zh: 使用 Playwright 测试本地 Web 应用的工具包，支持截图、浏览器日志和 UI 验证
version: "1.0.0"
tags: [testing, playwright, e2e, browser, automation, ui]
author: anthropics
source: anthropics/skills
installs: 12100
created_at: "2026-02-15"
---

# Web 应用测试工具

## 概述

Web 应用测试工具使用 Playwright 自动化测试本地 Web 应用。支持启动服务器、浏览 DOM、截图、查看浏览器日志和验证用户流程。

## 适用场景

- 本地 Web 应用功能测试
- 前端 UI 行为验证
- 端到端用户流程测试
- 调试 UI 问题
- 截图对比测试

## 核心功能

### 服务器管理
- 自动启动开发服务器
- 等待服务器就绪
- 管理服务器生命周期

### 页面交互
- 导航和点击
- 表单填写和提交
- 等待元素出现
- 处理弹窗和对话框

### 验证和调试
- 截取页面截图
- 捕获浏览器控制台日志
- 检查 DOM 结构
- 网络请求监控

### 测试模式
- 单次验证
- 用户流程测试
- 视觉回归测试

## 使用方式

```bash
npx skills add anthropics/skills@webapp-testing -g -y
```
