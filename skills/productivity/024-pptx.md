---
skill_id: "024"
category: productivity
title: PPT 演示文稿工具 (PPTX)
title_zh: PPT 演示文稿工具
description: Create, edit and analyze PowerPoint presentations with design guidance, content extraction and OOXML workflows
description_zh: 创建、编辑和分析 PowerPoint 演示文稿，提供设计指导、内容提取和 OOXML 工作流
version: "1.0.0"
tags: [pptx, powerpoint, presentation, document, office]
author: anthropics
source: anthropics/skills
installs: 14500
created_at: "2026-02-15"
---

# PPT 演示文稿工具

## 概述

PPT 演示文稿工具帮助创建、编辑和分析 PowerPoint 文件。PPTX 文件本质上是包含 XML 文件和资源的 ZIP 压缩包，可以直接读取和编辑。

## 适用场景

- 创建新的演示文稿
- 编辑现有 PPT 内容
- 提取 PPT 中的文本和图片
- 批量生成演示文稿
- 应用设计模板

## 核心功能

### 创建演示文稿
- 从 Markdown 生成 PPT
- 自定义幻灯片布局
- 添加图表和数据可视化
- 应用主题和配色方案

### 编辑操作
- 修改文本内容
- 替换图片
- 调整布局和样式
- 添加动画效果

### 内容提取
- 提取所有文本内容
- 导出图片资源
- 提取演讲者备注
- 转换为 Markdown

## 使用方式

```bash
npx skills add anthropics/skills@pptx -g -y
```
