# app-store-preflight-skills

> ⭐ 909 | https://github.com/truongduy2611/app-store-preflight-skills

## 项目简介

AI Agent Skill，在 iOS/macOS 项目提交 App Store 审核前，自动扫描项目中常见的拒审模式，帮助开发者提前发现问题，减少被拒概率。

## 核心功能

- **拒审模式扫描**：检测 App Store Review Guidelines 中常见的违规项
- **多维度检查**：覆盖隐私权限、UI 规范、API 使用、元数据等方面
- **Skill 格式**：标准 SKILL.md 格式，一行命令挂载到 Claude Code

## 检查范围（典型项）

- 隐私权限声明是否完整（相机、麦克风、位置等）
- 是否使用了被 App Store 禁止的私有 API
- 应用内购买流程是否符合规范
- 截图和元数据是否符合上架要求
- 崩溃和性能问题排查

## 使用场景

- 提交 App Store 前的最后一道自动化检查
- 新人 iOS 开发者快速了解常见拒审原因
- CI/CD 流程中集成上架前检查

## 相关链接

- GitHub: https://github.com/truongduy2611/app-store-preflight-skills
