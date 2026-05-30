# Understand-Anything

将任意代码库、知识库或文档转化为可探索、可搜索、可提问的交互式知识图谱。支持 Claude Code、Codex、Cursor、Copilot、Gemini CLI 等主流 AI 编程工具。

## 核心特性

### 多 Agent 代码分析管道
使用多 Agent 管道分析项目结构，自动提取类、函数、依赖关系，构建可交互的知识图谱。

### 交互式探索
不仅展示静态图表，支持在图谱中点击节点查看详情、追踪调用链、搜索符号定义。

### 广泛平台兼容
支持 Claude Code、Codex CLI、Cursor、GitHub Copilot、Gemini CLI、OpenCode、Trae 等，通过 Plugin 机制集成。

### 知识图谱优先
以图为组织核心而非传统树状文件浏览，更适合理解大型复杂代码库的架构关系。

## 技术架构

- **前端**：基于 Web 的交互式图形界面
- **后端**：多 Agent 管道，Claude API 驱动分析
- **集成**：Claude Code Plugin 标准，兼容 agentskills.io 规范

## 安装与使用

```bash
# Claude Code 中安装
/plugin install understand-anything@claude-plugins-official
```

Web demo: https://understand-anything.com/demo/

## GitHub

https://github.com/Lum1104/Understand-Anything
