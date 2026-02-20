---
skill_id: "037"
category: ai-ml
title: MCP 服务器构建指南 (MCP Builder)
title_zh: MCP 服务器构建指南
description: Guide for creating high-quality MCP servers that enable LLMs to interact with external services through well-designed tools
description_zh: 创建高质量 MCP 服务器的指南，使 LLM 能够通过精心设计的工具与外部服务交互
version: "1.0.0"
tags: [mcp, model-context-protocol, llm, tools, api, integration]
author: anthropics
source: anthropics/skills
installs: 10800
created_at: "2026-02-15"
---

# MCP 服务器构建指南

## 概述

MCP（Model Context Protocol）服务器构建指南帮助创建高质量的 MCP 服务器，使 LLM 能够通过标准化的工具接口与外部 API 和服务交互。支持 Python（FastMCP）和 Node/TypeScript（MCP SDK）。

## 适用场景

- 构建 MCP 服务器集成外部 API
- 为 AI Agent 创建自定义工具
- 将现有服务封装为 MCP 工具
- 设计 MCP 工具的输入/输出 Schema

## 核心概念

### MCP 架构
- Server：提供工具和资源
- Client：AI Agent 调用工具
- Transport：通信协议（stdio, HTTP）

### 工具设计原则
- 单一职责：每个工具做一件事
- 清晰的输入 Schema
- 有意义的错误信息
- 幂等性设计

### Python 实现（FastMCP）

```python
from fastmcp import FastMCP

mcp = FastMCP("my-server")

@mcp.tool()
def search_docs(query: str) -> str:
    """搜索文档库"""
    # 实现搜索逻辑
    return results
```

### TypeScript 实现

```typescript
import { McpServer } from "@modelcontextprotocol/sdk/server/mcp.js";

const server = new McpServer({ name: "my-server" });

server.tool("search_docs", { query: z.string() }, async ({ query }) => {
  // 实现搜索逻辑
  return { content: [{ type: "text", text: results }] };
});
```

## 使用方式

```bash
npx skills add anthropics/skills@mcp-builder -g -y
```
