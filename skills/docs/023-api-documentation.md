---
skill_id: "023"
category: docs
title: API 文档编写指南 (API Documentation)
title_zh: API 文档编写指南
description: Master API documentation standards including OpenAPI/Swagger specs, interactive docs generation and best practices
description_zh: 掌握 API 文档的标准结构、OpenAPI/Swagger 规范、交互式文档生成和最佳实践
version: "1.0.0"
tags: [docs, api, openapi, swagger, documentation, rest]
author: openclaw
source: yanghao1143/openclaw-skills
installs: 38700
created_at: "2026-02-15"
---

# API 文档编写指南

## 技能描述
掌握 API 文档的标准结构、OpenAPI/Swagger 规范、交互式文档生成和最佳实践，编写专业易用的 API 文档。

## 核心知识点

### 1. API 文档的核心要素
- 概述: API 用途、适用场景、快速开始
- 认证: 支持的认证方式 (API Key, OAuth2, JWT)
- 端点列表: 所有可用端点的路径、方法、参数
- 请求/响应示例: 真实的请求和响应数据
- 错误码: 所有可能的错误码及含义
- 速率限制: 请求频率限制和配额
- 版本信息: API 版本号和弃用策略
- SDK/客户端: 官方支持的编程语言客户端

### 2. OpenAPI 规范 (Swagger)

```yaml
openapi: 3.0.3
info:
  title: 示例 API
  version: 1.0.0
paths:
  /messages:
    post:
      summary: 发送消息
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: object
              required: [channel, message]
              properties:
                channel:
                  type: string
                message:
                  type: string
      responses:
        '200':
          description: 成功
        '400':
          description: 参数错误
```

### 3. 交互式文档工具
- Swagger UI: 可视化浏览和测试 API
- ReDoc: 美观的三栏布局文档
- Stoplight Elements: 现代化 API 文档
- Postman Collection: 可导入的 API 集合

### 4. 代码示例生成
- 多语言示例: cURL, Python, JavaScript, Go, Java
- SDK 自动生成: 从 OpenAPI 生成客户端库
- 在线沙盒: 提供可交互的测试环境

### 5. 文档维护策略
- 文档即代码: OpenAPI 文件纳入版本控制
- CI/CD 集成: 自动验证和发布文档
- 变更日志: 记录 API 变更和弃用通知
- 反馈循环: 收集用户反馈改进文档

## 检查清单
- 编写完整的 OpenAPI 3.0 规范文件
- 包含所有端点的路径、方法、参数
- 提供请求和响应的完整示例
- 定义所有错误码和状态码
- 说明认证方式和速率限制
- 生成多语言代码示例
- 部署交互式文档
- 添加变更日志和版本说明

## 参考资料
- [OpenAPI Specification](https://swagger.io/specification/)
- [Swagger Tools](https://swagger.io/tools/)
- [ReDoc](https://redocly.com/)
