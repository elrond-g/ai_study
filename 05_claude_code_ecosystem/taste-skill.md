# Taste Skill

Anti-Slop 前端框架，为 AI Agent 注入"品味"。提供可移植的 Agent Skills，升级 AI 生成的界面：更强的布局、排版、动效和间距，告别千篇一律的模板化 UI。同时包含用于参考板、品牌套件的图像生成技能。

## 核心特性

### Agent Skills 格式
遵循 agentskills.io 标准，可安装到 Codex、Cursor、Claude Code 等主流 AI 编程工具。

### 前端品味升级
通过 Skills 文件注入设计原则和约束，让 AI 生成的 UI 更具设计感，而非千篇一律的 boilerplate。

### 图像生成技能
内置参考板（web、mobile、brand kits）生成技能，配合 AI 图像生成器使用，再交给 Code Agent 实现。

### 一键安装
通过 npx skills add 一键安装全部或单个技能。

## 技术架构

- **格式**：agentskills.io SKILL.md 标准
- **安装**：npx skills add
- **兼容**：Codex、Cursor、Claude Code

## 安装与使用

```bash
npx skills add https://github.com/Leonxlnx/taste-skill
```

## GitHub

https://github.com/Leonxlnx/taste-skill
