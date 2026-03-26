# pi-autoresearch

Shopify CEO Tobi Lutke 开源的自主实验循环插件，受 Karpathy autoresearch 启发，为 pi 构建的自动化实验优化工具。适用于测试速度、Bundle 大小、LLM 训练性能、构建时间、Lighthouse 分数等多种优化目标。

## 核心特性

- **全自动循环**：编辑 → 提交 → 运行实验 → 记录结果 → 保留或回滚 → 重复，不中断则永不停止
- **智能初始化**：Agent 询问目标、命令、指标和文件范围，或从上下文自动推断
- **持久化日志**：每次实验结果追加到 `autoresearch.jsonl`，支持中断恢复和上下文重置
- **正确性检查**：通过 `autoresearch.checks.sh` 在每次通过基准测试后运行测试/类型检查/lint，确保优化不破坏功能
- **置信度评分**：3+ 次运行后报告置信度分数（≥2.0× 为可信改进，<1.0× 在噪声范围内）
- **方案记录**：`autoresearch.md` 记录所有尝试过的方案，新 Agent 可直接获取完整上下文

## 工作流程

1. 设定优化目标和基准命令
2. 自动创建分支，写入 `autoresearch.md` 和 `autoresearch.sh`
3. 运行基准测试，开始自主循环
4. 每次实验记录到 `autoresearch.jsonl`（一行一条）
5. 通过则提交保留，失败则回滚，持续迭代

## 安装

```bash
pi install https://github.com/davebcn87/pi-autoresearch
```

或手动复制 extensions 和 skills 目录到 `~/.pi/agent/`，然后执行 `/reload`。

## 链接

- GitHub: https://github.com/davebcn87/pi-autoresearch
