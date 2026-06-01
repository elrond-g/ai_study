# Agent Memory Techniques

NirDiamant 出品的 AI Agent 记忆技术全景教程，30 个可运行 Jupyter Notebook 覆盖从对话缓冲区到生产部署的完整记忆技术栈。

## 核心特性

### 六大技术家族

| 家族 | 解决的问题 | 技术编号 |
|------|-----------|----------|
| **Short-term Memory** | 单次对话上下文管理，控制上下文窗口大小 | 01-05 |
| **Long-term Memory** | 跨会话持久化存储，向量/实体/知识图谱/情景/语义记忆 | 06-11 |
| **Cognitive Architectures** | 工作记忆、层级记忆、反思记忆等认知架构 | 12-19 |
| **Retrieval & Routing** | 何时检索什么内容的策略与路由 | 20-23 |
| **Frameworks** | Mem0、Letta(MemGPT)、Zep、Graphiti 等生产级框架实战 | 24-27 |
| **Evaluation & Production** | 记忆系统评测基准(LoCoMo)与生产部署模式 | 28-30 |

### 关键亮点

- **全部可运行**：每个技术都是独立 Jupyter Notebook，下载即用
- **决策树引导**：内置决策树帮你按场景选择合适的技术
- **对比矩阵**：30 种技术的持久性/检索方式/Token 成本/适用场景对比表
- **学习路径**：新手从 01 Conversation Buffer 开始，逐层深入

## 技术架构

- **语言**：Python 3.10+，Jupyter Notebook
- **核心依赖**：LangChain、OpenAI API、向量数据库、图数据库
- **覆盖框架**：Mem0、Letta (MemGPT)、Zep、Graphiti、MemOS
- **评测基准**：LoCoMo 长对话记忆评测

## 安装与使用

```bash
git clone https://github.com/NirDiamant/Agent_Memory_Techniques.git
cd Agent_Memory_Techniques
pip install -r requirements.txt
jupyter notebook
```

按编号顺序学习，或直接用决策树选择目标场景对应的 Notebook。

## GitHub

https://github.com/NirDiamant/Agent_Memory_Techniques
