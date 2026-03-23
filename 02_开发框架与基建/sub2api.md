# sub2api（Sub2API-CRS2）

> ⭐ 7,873 | Go | https://github.com/Wei-Shaw/sub2api

## 项目简介

sub2api（CRS2）是一个一站式开源中转服务，将 Claude、OpenAI、Gemini、Antigravity 等 AI 订阅统一转化为标准 LLM API 接口。支持拼车共享和成本分摊，让原生工具（Claude Code、Cursor 等）无缝对接不同来源的订阅账号。

## 核心功能

- **多订阅统一接入**：Claude/Max/Team、OpenAI、Gemini、Antigravity 订阅全支持
- **拼车共享**：多用户共享同一订阅，自动分摊 Token 配额和费用
- **API 格式标准化**：统一输出 OpenAI 兼容格式，所有原生工具直接使用
- **Claude Code 直连**：支持 Claude Code、Cursor、Continue 等工具直接对接

## 技术特点

- Go 实现，高并发处理能力，低资源占用
- 支持 cc2api、2api、Antigravity2api 多种中转模式
- 内置请求路由和负载均衡

## 使用场景

- 团队共享 Claude Max/Team 订阅，降低人均成本
- 将 Claude 网页订阅接入需要 API 的开发工具
- 个人用户在多个 AI 工具间统一管理订阅

## 相关链接

- GitHub: https://github.com/Wei-Shaw/sub2api
