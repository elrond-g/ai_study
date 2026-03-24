# data-analyst-agent

> ⭐ 18 | Python | https://github.com/chenningling/data-analyst-agent

## 项目简介

基于大模型的自动化数据分析工具，支持上传 Excel/CSV 文件，由 AI Agent 自动规划并执行分析任务，最终生成带可视化图表的复盘报告。同时也是一个学习项目，对比展示了 5 种不同的 Agent 循环架构设计思路。

## 核心功能

- **自动化分析**：上传数据文件，AI 自主规划分析步骤并执行
- **可视化报告**：自动生成含图表的数据分析复盘报告
- **5 种 Agent 架构模式**：在同一项目中对比 ReAct、Plan-then-Execute 等不同实现
- **支持 Excel/CSV**：常见数据格式开箱即用

## 5 种 Agent 运行模式（学习价值）

| 模式 | 设计思路 |
|------|------|
| 基础循环 | 简单 ReAct 循环，逐步调用工具 |
| 规划模式 | 先生成完整计划再执行 |
| 反思模式 | 执行后反思结果并修正 |
| 多 Agent 协作 | 分析师 + 编码员分工协作 |
| 层级 Agent | 主 Agent 管理子 Agent |

## 使用场景

- 快速完成销售、运营、财务等业务数据的分析报告
- 学习和对比不同 Agent 循环架构的优劣
- 作为构建企业数据分析 Agent 的参考实现

## 相关链接

- GitHub: https://github.com/chenningling/data-analyst-agent
