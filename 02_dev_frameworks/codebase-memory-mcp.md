# Codebase Memory MCP

> ⭐ N/A | Python | https://github.com/DeusData/codebase-memory-mcp

## 项目简介

代码库记忆 MCP Server，为 AI Agent 提供跨会话的代码上下文持久化和召回能力，让 AI 在不同对话间记住项目的架构决策和代码约定。

## 核心功能

- **跨会话记忆持久化**：将代码库相关的上下文信息持久化存储，新会话自动加载
- **智能上下文召回**：根据当前任务自动匹配和召回相关的历史上下文
- **知识图谱管理**：以结构化方式组织代码库的架构信息、约定和决策记录

## 技术特点

- 基于 MCP 协议，与 Claude Code 等工具无缝集成
- 记忆数据存储在本地项目目录中，跟随代码库管理
- 支持手动标注和自动提取两种记忆录入方式

## 使用场景

- 让 AI Agent 记住项目的编码规范和架构约定，减少重复说明
- 多次会话开发同一项目时保持上下文连续性
- 团队共享代码库知识，新成员通过 AI 快速了解项目背景

## 相关链接

- GitHub: https://github.com/DeusData/codebase-memory-mcp
