---
skill_id: "028"
category: productivity
title: Word 文档处理工具 (DOCX)
title_zh: Word 文档处理工具
description: Comprehensive document creation, editing and analysis with tracked changes, comments and formatting preservation
description_zh: 全面的 Word 文档创建、编辑和分析，支持修订追踪、批注和格式保留
version: "1.0.0"
tags: [docx, word, document, office, editing]
author: anthropics
source: anthropics/skills
installs: 13400
created_at: "2026-02-15"
---

# Word 文档处理工具

## 概述

Word 文档处理工具提供全面的 DOCX 文件操作能力。DOCX 文件本质上是包含 XML 文件和资源的 ZIP 压缩包，可以直接读取和编辑。

## 适用场景

- 创建新的 Word 文档
- 编辑现有文档内容
- 处理修订追踪和批注
- 提取文档文本
- 批量生成文档

## 核心功能

### 文档创建
- 从 Markdown 生成 DOCX
- 自定义样式和格式
- 添加页眉页脚
- 插入表格和图片

### 编辑操作
- 修改文本内容
- 添加/删除修订追踪
- 插入批注
- 格式保留编辑

### 内容提取
- 提取全文文本
- 提取表格数据
- 导出图片
- 读取文档属性

## 使用方式

```bash
npx skills add anthropics/skills@docx -g -y
```
