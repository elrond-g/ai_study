# awesome-autoresearch

> WecoAI | 精选列表 | https://github.com/WecoAI/awesome-autoresearch

## 项目简介

awesome-autoresearch 是 WecoAI 维护的 AutoResearch 用例精选清单，汇集了各领域的自动研究/优化实例及其优化轨迹。每个条目不仅包含代码，还附带完整的优化轨迹链接，让用户能看到 Agent 尝试了什么、失败了什么、最终如何改进。

## 核心概念

AutoResearch 由 Andrej Karpathy 开创——通过一个 program.md 提示词指导 AI Agent（Claude Code、Codex 等）执行自动优化循环：

1. Agent 编辑目标文件（如 train.py）
2. 在固定时间内运行评估
3. 检查指标是否改进
4. 改进则提交，否则回滚
5. 持续循环迭代

## 收录的代表性案例

| 案例 | 成果 |
|------|------|
| Shopify 模板引擎优化 | 120 次实验 93 次提交，渲染速度 +53%，内存分配 -61% |
| GPU 内核优化（AutoKernel） | 性能从 18 TFLOPS → 187 TFLOPS |
| 古卷墨迹检测（Vesuvius Challenge） | 4 个 Agent 24/7 运行，泛化性能翻倍 |
| 语音 Agent 优化 | 评分从 0.728 → 0.969 |
| 比特币价格预测 | 328 次实验，RMSE 改进 50.5% |

## 核心特色

- **多领域适用**：LLM 训练、GPU 内核、语音 Agent、交易策略、模板引擎等
- **可验证轨迹**：每个项目附带优化进度图表和 Git 提交历史
- **社区驱动**：活跃的社区贡献，持续扩展新领域
- **基于 AIDE 框架**：WecoAI 的 aideml 提供树搜索驱动的 ML 工程 Agent 能力

## 为什么值得关注

与单纯的代码仓库不同，这个列表强调"过程透明"——不只展示最终结果，还完整记录 Agent 的探索路径和决策过程，是理解 AutoResearch 方法论的最佳入口。

## 相关链接

- GitHub: https://github.com/WecoAI/awesome-autoresearch
- AIDE 框架: https://github.com/WecoAI/aideml
- Weco AI: https://www.weco.ai/
