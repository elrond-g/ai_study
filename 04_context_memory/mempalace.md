# MemPalace

> ⭐ 31k+ | Python | https://github.com/milla-jovovich/mempalace | MIT

## 项目简介

MemPalace 是目前基准测试得分最高的开源 AI 长期记忆系统。借鉴古希腊记忆宫殿（Method of Loci）的空间记忆原理，将 AI 对话组织为翼（Wing）→ 厅（Hall）→ 室（Room）→ 柜（Closet）→ 抽屉（Drawer）的层级结构。核心策略是"存储一切，然后让它可被找到"——使用 ChromaDB 原文存储对话，不做 LLM 摘要/提取，通过语义搜索检索。

## 基准测试

| 模式 | LongMemEval R@5 | 说明 |
|------|-----------------|------|
| Raw（原文） | **96.6%** | 500 题，零 API 调用，已被独立复现 |
| AAAK（压缩） | 84.2% | 实验性，有损压缩换 Token 密度 |

96.6% 是已公开发布的 LongMemEval 最高分，完全本地运行、零成本。

## 记忆宫殿架构

- **Wing（翼）**：每个项目、人物或主题拥有独立翼
- **Room（室）**：翼内按主题分室（项目想法、人员、财务等）
- **Closet（柜）**：摘要层，指向原始文件所在的抽屉
- **Drawer（抽屉）**：原始文件存储位置
- **Hall（厅）**：连接同一翼内的房间
- **Tunnel（隧道）**：连接不同翼的房间，实现跨域知识关联

## 核心特点

- **原文存储**：ChromaDB 存储完整对话，不做 LLM 摘要，保留全部上下文
- **完全本地**：不使用任何外部 API 或服务，数据不离开本机
- **MCP 协议支持**：19 个 MCP 工具，Claude/ChatGPT/Cursor/Gemini 等工具可直接调用
- **三种数据挖掘模式**：projects（代码/文档）、convos（对话导出）、general（自动分类为决策/里程碑/问题/偏好）
- **AAAK 方言**（实验性）：有损缩写方言，压缩重复实体的 Token 消耗，任何 LLM 均可读取无需解码器

## 使用方式

```bash
pip install mempalace

# 初始化 → 挖掘数据 → 搜索
mempalace init ~/projects/myapp
mempalace mine ~/chats/ --mode convos
mempalace search "why did we switch to GraphQL"

# Claude Code 集成
claude plugin marketplace add milla-jovovich/mempalace

# MCP 集成（适用于各种 AI 工具）
claude mcp add mempalace -- python -m mempalace.mcp_server
```

## 成本对比

| 方案 | 加载 Token | 年成本 |
|------|-----------|--------|
| 全量粘贴 | 1950 万（超出上下文窗口） | 不可能 |
| LLM 摘要 | ~65 万 | ~$507 |
| **MemPalace 唤醒 + 5 次搜索** | **~1.35 万** | **~$10** |

## 为什么值得关注

31K Stars 的热度源于一个简单但深刻的设计选择：不信任 AI 判断什么值得记住，而是存储一切原文并用结构化空间组织让检索高效。96.6% LongMemEval 最高分、完全本地零成本、MCP 原生支持的组合，使其成为当前最有竞争力的开源 AI 记忆方案。

## 相关链接

- GitHub: https://github.com/milla-jovovich/mempalace
