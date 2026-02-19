---
skill_id: 026
category: security
title: 安全扫描 (Security Scanning)
title_zh: 安全扫描
description: Automated security scanning for code vulnerabilities, dependencies, and secrets
description_zh: 自动化扫描代码漏洞、依赖项和敏感信息
version: 1.0.0
tags: [security, scanning, vulnerability, secrets, dependencies]
author: oc-security
created_at: 2026-02-19
---

# 安全扫描 (Security Scanning)

## 概述

安全扫描技能提供自动化的代码安全审计能力，检测代码中的安全漏洞、敏感信息泄露和不安全的依赖项。

## 核心功能

### 1. 静态代码分析 (SAST)
- 检测常见安全漏洞 (SQL 注入、XSS、命令注入等)
- 识别不安全的 API 使用模式
- 检查认证和授权逻辑缺陷

### 2. 依赖项扫描 (SCA)
- 检测已知漏洞的第三方依赖 (CVE 数据库)
- 识别过时或不推荐的包版本
- 生成软件物料清单 (SBOM)

### 3. 敏感信息检测
- 扫描硬编码的 API Key、密码、私钥
- 检测配置文件中的敏感数据
- 识别 Git 历史中泄露的凭证

## 使用示例

```bash
# 运行完整安全扫描
./scripts/security-scan.sh --path ./src --output report.json

# 仅扫描依赖项
./scripts/security-scan.sh --dependencies-only

# 仅扫描敏感信息
./scripts/security-scan.sh --secrets-only
```

## 输出格式

```json
{
  "scan_date": "2026-02-19T17:00:00Z",
  "total_issues": 3,
  "critical": 1,
  "high": 1,
  "medium": 1,
  "low": 0,
  "issues": [
    {
      "severity": "critical",
      "type": "hardcoded_secret",
      "file": "config.py",
      "line": 42,
      "description": "检测到硬编码的 API Key"
    }
  ]
}
```

## 注意事项

- ⚠️ 本工具仅用于安全审计，不修复漏洞
- ⚠️ 发现的敏感信息应立即从代码库中移除
- ⚠️ 定期更新 CVE 数据库以保持扫描准确性

## 相关技能

- Skill 027: 渗透测试
- Skill 016: 单元测试
- Skill 018: CI/CD 流水线
