# AgentHub

Rust 编写的单二进制 AI Agent 控制面板，内嵌 React Web UI，为长时间运行的 AI Agent 提供运维管理能力。

## 核心特性

- **会话持久化**：关闭浏览器标签后 Agent 会话继续运行
- **ACP 结构化时间线**：查看消息、计划、工具调用、命令输出等结构化事件，替代原始终端滚动
- **多 Agent Team 编排**：Leader/Worker 工作流，支持共享协调原语
- **远程执行节点**：通过内部 gRPC 将 Agent 路由到远程节点执行
- **SQLite 持久化**：会话历史和运维记录持久存储
- **内嵌 Web UI**：React 前端编译进单个二进制，打开 localhost:8080 即用
- **完成通知**：Web UI 内接收 Agent 完成通知

## 技术栈

- Rust 后端 + 内嵌 React Web UI
- ACP 协议结构化输出
- SQLite 持久化
- gRPC 远程节点通信

## 安装

```bash
npm --prefix web ci
make run
# 打开 http://localhost:8080
```

## 链接

- GitHub: https://github.com/hawkingrei/agenthub
- 文档: https://doc.agenthub.hawkingrei.com/
