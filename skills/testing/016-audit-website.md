---
skill_id: "016"
category: testing
title: 网站审计工具 (Audit Website)
title_zh: 网站审计工具
description: Comprehensive website audit tool for SEO, performance, content and security that fits into AI workflow
description_zh: 全面的网站审计工具，涵盖 SEO、性能、内容和安全检查，无缝融入 AI 工作流
version: "1.0.0"
tags: [audit, seo, performance, security, testing, website]
author: squirrelscan
source: squirrelscan/skills
installs: 22600
created_at: "2026-02-15"
---

# 网站审计工具

## 概述

SquirrelScan 是一个全面的网站审计工具，支持 SEO、性能、内容质量和安全性检查。单一二进制文件，零依赖，完美融入 AI 工作流。

## 适用场景

- 网站 SEO 健康检查
- 页面性能分析（Core Web Vitals）
- 内容质量评估
- 安全漏洞扫描
- 竞品网站分析

## 审计维度

### SEO 审计
- Meta 标签完整性
- 标题层级结构
- 内链/外链分析
- 结构化数据检查
- 移动端适配

### 性能审计
- 页面加载时间
- Core Web Vitals (LCP, FID, CLS)
- 资源优化建议
- 缓存策略检查

### 安全审计
- HTTPS 配置
- 安全头检查
- 混合内容检测
- Cookie 安全属性

## 使用方式

```bash
npx skills add squirrelscan/skills -g -y
```
