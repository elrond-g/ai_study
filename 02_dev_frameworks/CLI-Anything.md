# CLI-Anything

> ⭐ 21,722 | Python | https://github.com/HKUDS/CLI-Anything

## 项目简介

CLI-Anything 是香港大学数据科学实验室开源的项目，目标是让所有软件都具备 Agent 原生（Agent-Native）能力。它通过自动分析软件的文档、帮助信息和使用模式，生成 AI Agent 可以调用的标准化 CLI 接口。

## 核心功能

- **自动接口生成**：解析任意软件的文档，自动生成 Agent 可调用的命令描述
- **Agent-Native 转换**：将传统软件转化为 AI Agent 可理解和使用的工具
- **统一调用格式**：所有工具遵循统一的输入/输出规范
- **自动工具发现**：Agent 可动态发现和学习新工具的使用方法

## 技术特点

- Python 实现，支持多种 CLI 工具的自动解析
- 基于 LLM 理解工具文档，生成结构化的工具描述
- 兼容 LangChain、AutoGPT 等主流 Agent 框架

## 使用场景

- 将企业内部工具快速接入 AI Agent 工作流
- 构建能够自主学习使用新工具的通用 AI Agent
- 研究 Agent 工具使用能力的扩展方法

## 相关链接

- GitHub: https://github.com/HKUDS/CLI-Anything
