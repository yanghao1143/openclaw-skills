---
skill_id: "022"
category: docs
title: 技术文档写作最佳实践 (Technical Writing)
title_zh: 技术文档写作最佳实践
description: Master technical documentation writing principles, structure design and language techniques for clear and accurate docs
description_zh: 掌握技术文档的写作原则、结构设计和语言表达技巧，撰写清晰、准确、易于理解的技术文档
version: "1.0.0"
tags: [docs, writing, technical-writing, documentation, best-practices]
author: openclaw
source: yanghao1143/openclaw-skills
installs: 45200
created_at: "2026-02-15"
---

# 技术文档写作最佳实践

## 技能描述
掌握技术文档的写作原则、结构设计和语言表达技巧，撰写清晰、准确、易于理解的技术文档。

## 核心知识点

### 1. 文档类型与目标读者
- 教程 (Tutorial): 面向新手，逐步引导完成具体任务
- 操作指南 (How-to Guide): 面向有经验用户，解决特定问题
- 参考文档 (Reference): 面向所有用户，提供完整 API/配置说明
- 解释性文档 (Explanation): 面向深度用户，讲解概念和原理
- Diátaxis 框架: 上述四种类型的理论基础

### 2. 文档结构原则
- 倒金字塔结构: 最重要信息放在开头
- 单一职责: 每个章节/段落只讲一个主题
- 渐进式披露: 从简单到复杂，层层深入
- 一致性: 术语、格式、风格保持统一
- 可扫描性: 使用标题、列表、代码块增强可读性

### 3. 语言表达技巧
- 主动语态: "系统会返回错误" 而非 "错误会被返回"
- 简洁明了: 避免冗长句子，每句不超过 25 词
- 具体明确: 避免"可能"、"大概"等模糊词汇
- 第二人称: 使用"你"而非"用户"，增强亲近感
- 现在时态: 描述功能时使用现在时

### 4. 代码示例规范
- 完整性: 示例代码应可独立运行
- 注释: 关键步骤添加注释说明
- 真实性: 使用真实的变量名和场景
- 格式: 使用语法高亮和一致的缩进
- 测试: 确保示例代码经过验证

### 5. 文档维护与版本控制
- 文档即代码: 使用 Markdown + Git 管理
- 版本对齐: 文档版本与软件版本对应
- 审查流程: 技术审查 + 语言审查
- 反馈机制: 提供"此页是否有用？"等反馈入口
- 自动化: CI/CD 检查链接、拼写、格式

## 检查清单
- 明确文档类型 (教程/指南/参考/解释)
- 使用倒金字塔结构，重要信息前置
- 每个章节只讲一个主题
- 使用主动语态和第二人称
- 代码示例完整、可运行、有注释
- 术语和格式保持一致
- 添加适当的标题、列表、代码块
- 提供前置条件和验证步骤
- 包含错误处理和常见问题
- 设置反馈机制和更新日志

## 参考资料
- [Diátaxis 框架](https://diataxis.fr/)
- [Google Developer Documentation Style Guide](https://developers.google.com/style)
- [Microsoft Writing Style Guide](https://learn.microsoft.com/en-us/style-guide/)
