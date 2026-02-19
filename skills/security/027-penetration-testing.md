---
skill_id: 027
category: security
title: 渗透测试 (Penetration Testing)
title_zh: 渗透测试
description: Automated penetration testing framework for web applications and APIs
description_zh: 自动化渗透测试框架，用于 Web 应用和 API 安全测试
version: 1.0.0
tags: [security, penetration-testing, web-security, api-security, ethical-hacking]
author: oc-security
created_at: 2026-02-19
---

# 渗透测试 (Penetration Testing)

## 概述

渗透测试技能提供自动化的安全测试框架，模拟攻击者行为检测 Web 应用和 API 的安全漏洞。

## 核心功能

### 1. Web 应用测试
- SQL 注入检测 (基于时间和布尔盲注)
- 跨站脚本 (XSS) 测试 (反射型、存储型、DOM 型)
- 跨站请求伪造 (CSRF) 检测
- 不安全的直接对象引用 (IDOR)
- 文件包含漏洞 (LFI/RFI)
- 命令注入检测

### 2. API 安全测试
- 未授权访问检测
- 速率限制绕过测试
- 批量赋值漏洞
- JWT 令牌安全测试
- GraphQL 注入检测

### 3. 认证与会话管理
- 弱密码策略检测
- 会话固定攻击测试
- 会话超时验证
- 多因素认证绕过测试

## 使用示例

```bash
# 运行完整渗透测试
./scripts/penetration-test.sh --target https://example.com --output report.html

# 仅测试 API 端点
./scripts/penetration-test.sh --target https://api.example.com --api-only

# 仅测试 SQL 注入
./scripts/penetration-test.sh --target https://example.com --tests sqli
```

## 输出格式

```json
{
  "test_date": "2026-02-19T17:00:00Z",
  "target": "https://example.com",
  "total_tests": 45,
  "passed": 40,
  "failed": 5,
  "vulnerabilities": [
    {
      "severity": "high",
      "type": "sql_injection",
      "endpoint": "/api/users",
      "parameter": "id",
      "payload": "' OR '1'='1",
      "evidence": "Database error message exposed"
    }
  ]
}
```

## 道德与合规

- ⚠️ **仅在授权目标上使用本工具**
- ⚠️ 未经授权的渗透测试可能违反法律
- ⚠️ 生产环境测试前请备份数据
- ⚠️ 遵守负责任的披露原则

## 安全警告

```
⚠️ 本工具包含攻击性测试功能，仅限安全专业人员使用
⚠️ 使用前必须获得目标系统的书面授权
⚠️ 禁止用于非法目的
⚠️ 作者不对滥用行为承担责任
```

## 相关技能

- Skill 026: 安全扫描
- Skill 018: CI/CD 流水线
- Skill 017: 集成测试

## 参考资源

- OWASP Top 10: https://owasp.org/www-project-top-ten/
- PTES: http://www.pentest-standard.org/
- NIST SP 800-115: https://csrc.nist.gov/publications/detail/sp/800-115/final
