# Context-Engineering

> https://github.com/davidkimai/Context-Engineering

## 项目简介

Context-Engineering 是上下文工程（Context Engineering）实践的系统性资源库，由 davidkimai 维护。上下文工程是 Prompt 工程的进化形态——不再只是优化单条 prompt，而是系统设计 AI 在整个任务周期中接收什么信息、何时接收、以何种结构接收。

## 核心思想

**从 Prompt 工程到上下文工程：**
- **Prompt 工程**：优化单次输入的措辞
- **上下文工程**：设计 AI 的信息流动架构

上下文工程的关键维度：
1. **信息选择**：哪些信息应该出现在上下文中
2. **信息结构**：如何组织这些信息（格式、顺序）
3. **信息时机**：在任务的哪个阶段注入哪些信息
4. **信息压缩**：如何在 token 限制内最大化信息密度

## 核心内容

- **架构模式**：Static、Dynamic、Agentic 三类上下文架构
- **CLAUDE.md 模式**：利用持久化文件传递项目上下文
- **记忆系统设计**：短期/长期记忆的分层架构
- **实践案例**：K8s Agent、代码助手等场景的上下文设计

## 使用场景

- 设计生产级 AI Agent 的上下文架构
- 优化 Claude Code 等工具的 CLAUDE.md 配置
- 学习超越 prompt 工程的系统性 AI 工程思维

## 相关链接

- GitHub: https://github.com/davidkimai/Context-Engineering
