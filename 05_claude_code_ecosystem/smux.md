# smux

> ⭐ 644+ | Bash + tmux | https://github.com/ShawnPana/smux | MIT

## 项目简介

smux 是基于 tmux 的终端多路复用配置方案，内置多代理间通信能力。核心创新：将终端作为中立的 Agent 通信平台，让 Claude Code、Codex、Gemini CLI 等不同 AI Agent 能够在 tmux 窗格间相互交互和协作，无需 API 或专有协议。

## 核心功能

### 用户端
- 预配置 tmux 配置，Option 键绑定（无前缀键）
- 鼠标操作 + 窗格标签 + 最小状态栏
- 快捷导航：Option+i/k/j/l 移动，Option+n 新窗格，Option+w 关闭

### Agent 端（tmux-bridge CLI）
- `type`：输入文本（不含 Enter）
- `keys`：发送特殊按键
- `read`：捕获窗格内容
- 任何能运行 bash 的工具都能参与

### 多 Agent 协作
- Claude Code 和 Codex 等 Agent 可通过终端窗格相互通信
- 无需 API 或专有协议，终端即共享界面
- 实现真正的跨工具 Agent 协作工作流

## 技术特点

- 核心依赖仅 tmux
- Bash 实现，零额外依赖
- Homebrew 安装（macOS）或包管理器（Linux）

## 为什么值得关注

1. **Agent 通信新范式**：终端作为 Agent 通信中枢，跳过复杂的 API 对接
2. **工具中立**：任何支持 bash 的 AI 工具都能参与协作
3. **零成本集成**：无需修改 Agent 代码，只需在 tmux 窗格中运行

## 相关链接

- GitHub: https://github.com/ShawnPana/smux
