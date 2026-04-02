# Build for iOS and macOS — Codex Use Cases

> OpenAI Developers | https://developers.openai.com/codex/use-cases/native-ios-macos-apps

## 简介

OpenAI Codex 官方发布的原生 iOS/macOS 应用开发指南，介绍如何用 Codex Agent 搭建 SwiftUI 项目、保持 CLI 优先的构建循环，并在深入开发时集成 XcodeBuildMCP 和专用 SwiftUI Skills。

## 核心工作流

### 1. 脚手架搭建（Greenfield）

- 用纯 Prompt 让 Codex 生成 SwiftUI 初始项目 + 构建脚本
- 保持 CLI 优先：使用 `xcodebuild` 完成 build/test/archive 等操作，避免依赖 Xcode GUI
- 可选用 **Tuist** 作为更清洁的项目生成器，终端内完成项目生成和构建

### 2. 深度项目自动化

- 使用 **XcodeBuildMCP** 进入完整 Xcode 项目后的深度自动化：
  - 检查 Schemes 和 Targets
  - 启动模拟器
  - 截取屏幕截图
  - 读取日志和 UI 交互
- 让 Codex 在 Agent 循环中持续迭代，无需切回 Xcode GUI

### 3. 迭代开发

- 明确告诉 Codex：是全新项目还是已有项目
- 指定需要保持兼容的平台（iOS/macOS）
- 定义验证循环的期望

## 推荐 Skills

| Skill 名称 | 用途 |
|------------|------|
| SwiftUI expert | 通用 SwiftUI 最佳实践 |
| SwiftUI Pro | SwiftUI 代码审查（现代 API、可维护性、无障碍、性能） |
| Liquid glass expert | iOS/macOS 26 新 Liquid Glass API 适配 |
| SwiftUI performance | 扫描 SwiftUI 常见性能错误，生成优先级修复报告 |
| Swift concurrency expert | 处理 Swift 并发诊断和编译器警告 |
| SwiftUI view refactor | 拆分大文件、统一 SwiftUI 代码风格 |
| SwiftUI patterns | `@Observable` 和 `@Environment` 架构模式 |

## 推荐技术栈

| 需求 | 推荐工具 | 理由 |
|------|---------|------|
| UI 框架 | SwiftUI | 跨 Apple 平台最快的原型方式 |
| 构建工具 | xcodebuild / Tuist | 终端内完成构建，不依赖 Xcode GUI |
| 项目自动化 | XcodeBuildMCP | 深度控制 Schemes/模拟器/截图/日志 |
| 分发工具 | App Store Connect CLI | Agent 全流程内直接提交到 App Store |

## 实用技巧

- **先从基础开始**：全新项目先用纯 Prompt，不需要立即上 Skill 或 MCP
- **小范围验证循环**：每次修改后运行最窄的验证命令，通过后再扩展到完整构建
- **CLI 优先**：`xcodebuild` 支持 list schemes、build、test、archive、build-for-testing、test-without-building
- **适时引入 XcodeBuildMCP**：当需要 Scheme 检查、模拟器控制、截图和 UI 交互时

## Starter Prompt 示例

```
Scaffold a starter SwiftUI app and add a build-and-launch script I can wire to a `Build` action in my local environment.

Constraints:
- Stay CLI-first. Prefer Apple's `xcodebuild`; if a cleaner setup helps, it's okay to use Tuist.
- If this repo already contains a full Xcode project, use XcodeBuildMCP to list targets, pick the right scheme, build, launch, and capture screenshots while you iterate.
- Reuse existing models, navigation patterns, and shared utilities when they already exist.
- Keep iOS and macOS compatibility intact unless I explicitly scope the work to one platform.
- Use a small trustworthy validation loop after each change, then expand to broader builds only when the narrower check passes.
- Tell me whether you treated this as a greenfield scaffold or an existing-project change.

Deliver:
- the app scaffold or requested feature slice
- a small build-and-launch script with the exact commands
- the smallest relevant validation steps you ran
- the exact scheme, simulator, and checks you used
```

## 适用场景

- 全新 SwiftUI 项目的快速脚手架搭建
- 已有 Apple 平台项目需要 Agent 辅助迭代
- 团队希望原生 UI 任务保持 Agent 化和 CLI 优先的开发模式

## 相关链接

- 原文: https://developers.openai.com/codex/use-cases/native-ios-macos-apps
- XcodeBuildMCP: https://github.com/nickthedude/XcodeBuildMCP
- Tuist: https://tuist.io/
- Codex Skills 文档: https://developers.openai.com/codex/docs/skills
