# Claude-to-IM-skill

> ⭐ 2k+ | TypeScript | https://github.com/op7418/Claude-to-IM-skill | MIT

## 项目简介

Claude-to-IM-skill 是一个将 Claude Code / Codex 桥接到 IM 平台的 Skill，让你通过 Telegram、Discord、飞书/Lark、QQ、微信等聊天界面与 AI 编程 Agent 对话。该 Skill 从 [CodePilot](https://github.com/op7418/CodePilot) 的 IM 桥接模块中提取，面向偏好轻量 CLI 方案的用户。

## 工作原理

```
You (Telegram/Discord/飞书/QQ/微信)
  ↕ Bot API
Background Daemon (Node.js)
  ↕ Claude Agent SDK 或 Codex SDK（通过 CTI_RUNTIME 配置）
Claude Code / Codex → 读写你的代码库
```

Skill 启动后台守护进程，连接 IM Bot 与 Claude Code/Codex 会话，IM 消息转发给 AI Agent，响应（含工具调用、权限请求、流式预览）回传到聊天窗口。

## 核心功能

- **五大 IM 平台**：Telegram、Discord、飞书/Lark、QQ、微信，可任意组合启用
- **交互式引导设置**：`/claude-to-im setup` 向导式收集 Token 和配置
- **权限控制**：工具调用需用户通过内联按钮（Telegram/Discord）或文字命令（飞书/QQ/微信）显式批准
- **流式预览**：Telegram 和 Discord 支持实时查看 Claude 的响应过程
- **会话持久化**：对话在守护进程重启后保持
- **密钥保护**：Token 以 `chmod 600` 存储，日志自动脱敏

## 安装方式

```bash
# Claude Code（推荐）
npx skills add op7418/Claude-to-IM-skill

# Codex
git clone https://github.com/op7418/Claude-to-IM-skill.git ~/code/Claude-to-IM-skill
bash ~/code/Claude-to-IM-skill/scripts/install-codex.sh
```

## 为什么值得关注

解决了 AI 编程 Agent 的移动端访问问题——不在电脑前也能通过手机 IM 下达编码指令、审批权限、查看进展。五平台覆盖 + 零代码配置的设计让桥接门槛极低。

## 相关链接

- GitHub: https://github.com/op7418/Claude-to-IM-skill
- 桌面 GUI 版本: https://github.com/op7418/CodePilot
