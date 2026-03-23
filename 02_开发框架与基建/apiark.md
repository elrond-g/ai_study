# apiark

> ⭐ 809 | TypeScript | https://github.com/berbicanes/apiark

## 项目简介

apiark 是一款隐私优先的 API 调试工具，Postman 的轻量替代品。基于 Tauri v2 构建，无需登录、无云端存储，内存占用约 60MB，所有请求数据完全本地保存。

## 核心功能

- **API 请求调试**：支持 REST、GraphQL 等各类 HTTP API 测试
- **隐私保护**：无需账号，数据不上云，完全离线可用
- **极低资源占用**：~60MB 内存，Postman 的 1/10
- **本地数据存储**：所有 Collection 和 Environment 变量存储在本地

## 技术特点

- Tauri v2 + TypeScript + Rust 架构
- 桌面原生应用，跨平台支持（macOS、Windows、Linux）
- 轻量安装包，快速启动

## 与 Postman 对比

| 维度 | apiark | Postman |
|------|--------|---------|
| 登录要求 | 无需 | 需要 |
| 数据存储 | 本地 | 云端 |
| 内存占用 | ~60MB | ~300MB+ |
| 离线使用 | 完全支持 | 受限 |

## 使用场景

- 调试 Claude API、OpenAI API 等 LLM 接口
- 注重数据安全的企业内部 API 开发
- 资源受限环境下的 API 测试

## 相关链接

- GitHub: https://github.com/berbicanes/apiark
