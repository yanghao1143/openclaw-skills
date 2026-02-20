---
skill_id: "029"
category: backend
title: Better Auth 认证最佳实践 (Better Auth)
title_zh: Better Auth 认证最佳实践
description: Best practices for implementing authentication with Better Auth including social providers, 2FA, passkeys and RBAC
description_zh: 使用 Better Auth 实现认证的最佳实践，包括社交登录、双因素认证、Passkey 和 RBAC
version: "1.0.0"
tags: [auth, authentication, oauth, 2fa, passkey, rbac, security]
author: better-auth
source: better-auth/skills
installs: 13400
created_at: "2026-02-15"
---

# Better Auth 认证最佳实践

## 概述

Better Auth 是一个 TypeScript/JavaScript 认证框架。此技能提供使用 Better Auth 实现认证的最佳实践，涵盖社交登录、邮箱密码、Magic Link、双因素认证、Passkey、组织和 RBAC。

## 适用场景

- 在 TypeScript/JavaScript 应用中添加认证
- 配置社交登录（Google, GitHub, Microsoft, Apple）
- 实现双因素认证（2FA）
- 配置 Passkey 无密码登录
- 设置组织和角色权限（RBAC）

## 常见问题防范

- Session 序列化问题
- CORS 配置错误
- D1 适配器设置
- OAuth 流程错误
- JWT Token 处理

## 核心功能

### 认证方式
- 邮箱/密码
- 社交登录（OAuth2）
- Magic Link
- Passkey
- 双因素认证

### 权限管理
- 基于角色的访问控制（RBAC）
- 组织级权限
- 自定义权限策略

## 使用方式

```bash
npx skills add better-auth/skills -g -y
```
