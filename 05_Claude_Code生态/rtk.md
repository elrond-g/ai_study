# rtk

> https://github.com/rtk-ai/rtk

## 项目简介

rtk 是一个 LLM 代理层压缩工具，通过在请求到达 LLM 之前对 message 进行智能压缩，降低 Token 消耗，从而减少 Claude Code 等工具的 API 调用成本。

## 核心机制

**代理压缩流程：**
```
Claude Code → rtk 代理层 → [压缩处理] → Claude API
                                ↓
                         Token 减少 30-60%
```

压缩策略：
- 移除重复信息
- 压缩长代码段（保留结构，省略细节）
- 智能摘要历史对话
- 去除与当前任务无关的上下文

## 核心功能

- **透明代理**：对 Claude Code 完全透明，无需修改配置
- **智能压缩**：在保持语义完整的前提下最大化压缩率
- **成本监控**：实时显示节省的 token 数量和费用
- **可配置策略**：调整压缩力度，平衡精度和成本

## 使用场景

- Claude Code 重度用户控制 API 成本
- 企业部署 Claude Code 时的成本优化
- 长上下文任务的 token 管理

## 与 `.claudeignore` 的区别

- `.claudeignore`：静态过滤，完全排除某些文件
- `rtk`：动态压缩，保留信息但减少 token

## 相关链接

- GitHub: https://github.com/rtk-ai/rtk
