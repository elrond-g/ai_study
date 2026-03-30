# oh-my-claudecode

> Yeachan-Heo | TypeScript + Python | https://github.com/Yeachan-Heo/oh-my-claudecode | https://ohmyclaudecode.com/

## 项目简介

oh-my-claudecode 是一个团队优先型多 Agent 编排平台，将 Claude Code 从单一编码助手转变为完整的多 Agent 系统。包含 32 个专门化 Agent 和 40+ 项技能，实现从高级想法到可测试代码的全自动执行。

## 执行模式

| 模式 | 说明 |
|------|------|
| Autopilot | 自动检测意图并编排 Agent |
| Ultrapilot | 5 个并发工作线程，比顺序执行快 3-5 倍 |
| Ralph（持久模式） | 自修复循环，自动验证和修复直至 100% 完成 |
| 深度访谈 | 苏格拉底式提问澄清思路 |
| 最大并行化 | 激进的 Agent 委托同时处理多任务 |

## 32 个专门化 Agent

分为低/中/高复杂度三层，覆盖架构设计、数据科学、研究、测试、DevOps 等领域。利用 Claude Code 原生团队模式，在隔离 Git 工作树中实现真正的并行执行。

## 核心特色

- **智能模型路由**：简单任务用 Haiku，复杂推理用 Opus，节省 30-50% Token
- **持久 Python 环境**：内置 pandas/numpy/matplotlib，变量跨调用保持
- **自学引擎**：识别调试模式并保存为可复用 .omc 技能
- **自动恢复**：配额耗尽后自动等待重置并继续任务
- **团队管道**：计划 → 文档 → 执行 → 验证 → 修复

## 技术架构

通过 Claude Code 原生 Skills + Hooks 系统集成（31 个生命周期钩子），npm 包 `oh-my-claude-sisyphus`。

## 为什么值得关注

在 Claude Code 原生能力之上构建了完整的多 Agent 编排层，5 个 Agent 可同时重构不同模块——真正的并行化而非伪并行。自然语言界面零学习曲线。

## 相关链接

- GitHub: https://github.com/Yeachan-Heo/oh-my-claudecode
- 官网: https://ohmyclaudecode.com/
