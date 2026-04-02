# ccleaks — Claude Code 泄露源码分析站

> 网站 | https://www.ccleaks.com/

## 简介

ccleaks 是一个专注于分析 Claude Code 泄露源码的网站。从泄露的 `cli.js.map` sourcemap 中逆向还原了 1,884 个 TypeScript 文件，揭示了 8 个未发布功能、隐藏斜杠命令、秘密环境变量、未公开的模型 ID 以及完整的内部架构。

## 背景事件

- Claude Code 源码通过 sourcemap 意外泄露
- 泄露源码镜像在 GitHub 获得 84,000+ Stars
- Anthropic 发起 8,000+ 次 DMCA 版权删除请求，后缩减至 1 个仓库 + 96 个 fork
- 安全研究员 Chaofan Shou 首先发现泄露，相关帖子获得 2800 万+ 浏览
- Anthropic Mythos 模型在 Claude Code 泄露前 5 天也发生泄露

## 分析内容

- **1,884 个 TypeScript 文件**完整还原
- **8 个未发布功能**和隐藏斜杠命令
- **秘密环境变量**和未公开的模型 ID
- **完整内部架构**分析
- 社区基于泄露源码构建的修改版本和自定义 fork

## 衍生项目

- **OpenClaude**：社区 fork，允许使用任意 LLM（OpenAI、Gemini、DeepSeek、Ollama）运行 Claude Code 的工具
- **claw-code**：Clean-room 重写版本，100,000+ Stars

## 相关链接

- 网站: https://www.ccleaks.com/
