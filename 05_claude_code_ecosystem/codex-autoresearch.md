# codex-autoresearch

> ⭐ 625 | Python | https://github.com/leo-lilinxiao/codex-autoresearch

## 项目简介

面向 Codex/Claude Code 的自导向迭代式学习 Skill，持续循环"修改→验证→保留/丢弃"，理论上可无限执行。灵感来自 Karpathy 的 autoresearch 概念，将其移植为可直接挂载到 AI 编程工具的 Skill 形式。

## 核心功能

- **自导向迭代**：无需人工干预，Agent 自主决定每次迭代的修改方向
- **验证闭环**：每次修改后自动运行验证，根据结果决定保留或回滚
- **无限循环**：设计为持续运行，直到任务完成或被手动停止
- **Skill 格式**：标准 SKILL.md 格式，可直接挂载到 Claude Code、Codex 等工具

## 与原版 autoresearch 的区别

| 特性 | Karpathy autoresearch | codex-autoresearch |
|------|------|------|
| 运行方式 | 独立脚本 | Skill（挂载到现有工具） |
| 目标 | AI 模型自训练 | 代码迭代优化 |
| 接入成本 | 需单独部署 | 一行命令安装 |

## 使用场景

- 让 AI 自主优化某个算法或函数，持续改进直到达标
- 自动化重复性代码重构工作
- 探索 AI 自主编程的边界

## 相关链接

- GitHub: https://github.com/leo-lilinxiao/codex-autoresearch
