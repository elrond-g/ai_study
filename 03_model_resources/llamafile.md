# LlamaFile

> ⭐ 25k+ | C/C++ | https://github.com/Mozilla-Ocho/llamafile

## 项目简介

Mozilla 出品，将大语言模型打包为单个可执行文件，实现跨平台零依赖运行 LLM。下载即运行，无需安装任何环境。

## 核心功能

- **单文件分发**：将模型权重与推理引擎打包为一个可执行文件，双击即可运行
- **跨平台兼容**：同一个文件支持 macOS / Linux / Windows / FreeBSD 等多平台
- **内置 Web 服务**：启动后自动提供 Web UI 和 API 接口，无需额外配置

## 技术特点

- 基于 Cosmopolitan Libc 实现真正的跨平台单文件可执行
- 底层使用 llama.cpp 推理引擎，支持 CPU/GPU 加速
- 零依赖设计，无需 Python、Docker 或其他运行时

## 使用场景

- 向非技术用户分发可直接运行的 AI 模型
- 离线环境或受限网络中部署 LLM
- 快速体验和评估不同开源模型

## 相关链接

- GitHub: https://github.com/Mozilla-Ocho/llamafile
