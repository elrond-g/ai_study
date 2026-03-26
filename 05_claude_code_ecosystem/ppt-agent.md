# ppt-agent

自动生成高质量 PowerPoint 演示文稿的 AI Agent 系统，通过多核心协作完成从需求研究、内容规划到设计生成的全流程。

## 核心特性

- **多 Agent 架构**：
  - `research-core`：需求研究和素材收集（含网页搜索）
  - `content-core`：大纲规划和内容结构
  - `slide-core`：SVG 设计生成，Bento Grid 布局
  - `review-core`：Gemini 驱动的布局和美学优化
- **17 种内置风格**：business、tech、creative、minimal、blueprint、pixel-art、watercolor 等
- **MCP Server**：封装为标准工具（`ppt/generate`、`ppt/outline`、`ppt/review`），兼容 Claude Code/Codex/OpenCode
- **集成网页搜索**：使用 agent-reach skill，无外部依赖

## 链接

- GitHub: https://github.com/zengwenliang416/ppt-agent
