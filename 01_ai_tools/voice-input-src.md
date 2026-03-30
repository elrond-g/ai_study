# Voice Input

> yetone | Swift | https://github.com/yetone/voice-input-src

## 项目简介

Voice Input 是一款 macOS 菜单栏语音输入应用，按住 Fn 键说话、松开自动将转录文本注入当前聚焦的输入框。基于 Apple 原生 Speech Recognition 框架，专为中文用户优化。

## 核心功能

- **全局语音输入**：Fn 键触发（不干扰 emoji 选择器），随处可用
- **实时流式转录**：Apple 原生语音识别 + 浮窗音频波形可视化
- **多语言支持**：简体中文（默认）、英文、繁体中文、日语、韩语，菜单栏快速切换
- **LLM 优化**：可选接入 OpenAI 兼容 API，特别针对中英混合场景提升准确度
- **智能输入法处理**：粘贴前自动切换至 ASCII 输入法（防止中文输入法拦截 Cmd+V），粘贴后恢复

## 技术特点

- Swift 原生 macOS 应用，macOS 14.0+ (Sonoma)
- Apple Speech Recognition Framework（本地识别，隐私友好）
- CGEvent Tap 实现全局热键监听
- 剪贴板 + 模拟粘贴实现跨应用文本注入
- `make build` 一键编译

## 为什么值得关注

1. **中文深度优化**：针对中文输入法的特殊处理（自动切换）解决了 macOS 语音输入的真实痛点
2. **极简交互**：单一 Fn 键，完全隐形集成
3. **本地隐私**：基于 Apple 原生识别框架，语音数据不离开设备
4. **开源可控**：完整源代码，可自行编译和定制

## 相关链接

- 源码: https://github.com/yetone/voice-input-src
- 分发版: https://github.com/yetone/voice-input-dist
