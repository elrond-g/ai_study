# RCLI

> ⭐ 1,287 | C++ | https://github.com/RunanywhereAI/RCLI

## 项目简介

RCLI 是一个完全本地运行的语音控制 macOS 助手，集成语音识别（STT）、本地 LLM 推理和 RAG 文档问答能力。无需云服务，所有计算在本机完成，数据不离设备。

## 核心功能

- **本地语音控制**：语音转文字后直接调用本地 LLM 处理指令
- **macOS 系统集成**：可控制 macOS 的各类操作（应用启动、文件操作等）
- **本地 RAG**：对接本地文档库，实现语音问答
- **TTS 回复**：支持 Kokoro TTS 和 Kitten TTS 语音合成输出

## 技术特点

- C++ 核心，针对 Apple Silicon（Metal GPU）优化
- 集成 llama.cpp 推理引擎，支持 Qwen3、LFM2 等模型
- 使用 Parakeet 进行语音识别，支持离线工作
- 工具调用（Tool Calling）支持，可执行系统级操作

## 使用场景

- 注重隐私、不想数据上云的 Mac 用户
- 构建完全离线的语音助手原型
- 探索端侧 AI 与系统控制的集成方案

## 相关链接

- GitHub: https://github.com/RunanywhereAI/RCLI
