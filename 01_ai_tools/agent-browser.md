# agent-browser

Vercel Labs 出品的 AI Agent 浏览器自动化 CLI 工具，通过 CDP（Chrome DevTools Protocol）直连 Chrome/Chromium，为 AI 编码代理提供完整的浏览器控制能力。25.7K Stars，179 位贡献者，Apache 2.0 开源。

## 核心特性

### 浏览器控制命令
- **导航**：`open`（打开 URL）、`close`（关闭页面）
- **交互**：`click`、`dblclick`、`fill`、`type`、`select`、`check`、`press`、`scroll`、`hover`
- **观察**：`snapshot`（无障碍树）、`screenshot`（页面截图）
- **对话框处理**：自动检测 alert/confirm/prompt 弹窗，支持接受/拒绝操作

### 标注截图（Annotated Screenshots）
`--annotate` 参数在截图上叠加编号标签，每个标签 `[N]` 对应引用 `@eN`，使多模态 AI 模型能够推理视觉布局、无标签图标按钮、Canvas 元素等文本无障碍树无法捕获的内容。这是该工具最大的差异化特性。

### 实时仪表盘
本地 Web 仪表盘（端口 4848），实时显示浏览器视口和命令活动流，方便监控 Agent 会话。

### 并发命名会话
多 Agent 并行运行时，通过命名会话隔离各自的浏览器实例，避免冲突。

### 批量执行
通过管道传入 JSON 数组到 `batch` 命令，单次调用执行多个命令，避免逐命令启动进程的开销。

### 网络流量捕获
`network har start/stop` 命令以 HAR 1.2 格式捕获和导出网络流量。

### WebSocket 流
每个会话自动启动 WebSocket 流服务器，支持实时状态推送。

## 安装方式

```bash
# npm 全局安装
npm i -g agent-browser

# Homebrew
brew install agent-browser

# Cargo（Rust）
cargo install agent-browser

# 安装 Chrome
agent-browser install
```

## 技术架构

- **双路径实现**：Node.js + Rust（Native 实验性），目标全面迁移到 Rust
- **零额外依赖**：不需要 Playwright 或 Node.js daemon，自动检测已有的 Chrome/Brave/Playwright/Puppeteer 安装
- **包管理**：pnpm
- **调试工具**：trace 录制、Chrome DevTools profiling、console 消息查看、错误追踪、元素高亮

## 平台支持

- **本地浏览器**：Chrome、Brave、Playwright、Puppeteer 自动检测
- **云端浏览器**：Kernel（https://kernel.sh）远程浏览器基础设施，`-p kernel` 标志连接，支持隐身模式和持久化配置
- **移动端**：iOS 模拟器和真机 Safari 测试，通过 Appium 驱动，支持 `device list`、`tap`、`swipe` 触摸命令

## 生态集成

已被主流 AI 编码代理广泛采用：
- opencode（127.3K 安装）
- codex（96.4K 安装）
- gemini-cli（94.2K 安装）
- github-copilot（90.4K 安装）
- cursor（86.8K 安装）

同时提供 Claude Code Skill（`skills/agent-browser/SKILL.md`）。

## 与同类工具对比

| 特性 | agent-browser | bb-browser | lightpanda |
|------|--------------|------------|------------|
| 定位 | AI Agent CLI | 浏览器即 API | AI 专用无头浏览器 |
| 底层 | CDP 直连 Chrome | 真实 Chrome 登录态 | 自研引擎 |
| 标注截图 | ✅ | ❌ | ❌ |
| 移动端 | ✅ iOS | ❌ | ❌ |
| 云端浏览器 | ✅ Kernel | ❌ | ❌ |
| Stars | 25.7K | - | - |

## GitHub

https://github.com/vercel-labs/agent-browser
