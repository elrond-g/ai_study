# better-icons

> https://github.com/better-auth/better-icons

## 项目简介

better-icons 是一个 MCP + Claude Code Skill 的组合工具，提供 20 万+ 图标的智能搜索和自动集成能力。用自然语言描述所需图标，AI 自动在庞大的图标库中找到最合适的，并直接同步到项目代码中。

## 核心功能

- **20万+ 图标库**：聚合 Heroicons、Lucide、Tabler、Material、Phosphor 等主流图标集
- **语义搜索**：用"一个表示上传的箭头图标"这样的描述找到合适图标
- **自动集成**：找到图标后直接写入项目代码（React/Vue/SVG 等格式）
- **MCP 服务器**：作为 MCP 工具被 Claude Code 直接调用

## 技术特点

- MCP Server 架构，与 Claude Code 深度集成
- 向量化图标描述，支持语义相似搜索
- 支持多框架的代码生成（React 组件、Vue 组件、纯 SVG）

## 快速开始

在 Claude Code MCP 配置中添加 better-icons 服务器，然后直接告诉 Claude"帮我找一个设置齿轮图标并加入到 Header 组件"即可。

## 使用场景

- 前端开发中快速找到并集成合适图标
- 避免在多个图标库网站间来回切换
- AI 辅助开发时无缝处理图标需求

## 相关链接

- GitHub: https://github.com/better-auth/better-icons
