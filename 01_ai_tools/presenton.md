# Presenton

开源 AI PPT 生成器和 API，Gamma、Beautiful.ai、Decktopus 的开源替代品。支持 Docker 自托管和桌面应用（Mac/Windows/Linux），可导出完全可编辑的 PPTX 文件。

## 核心特性

### 完全自托管
- Docker 容器化部署，无 SaaS 锁定
- 桌面应用支持 macOS、Windows、Linux

### 多模型支持
兼容 OpenAI、Gemini、Vertex AI、Azure OpenAI、Amazon Bedrock、Fireworks、Together AI、Anthropic、Ollama 等，支持本地模型。

### 可编辑导出
导出为完全可编辑的 PPTX 格式，不是死板的图片或不可修改的模板。

### API 接口
提供 AI 演示文稿生成 API，可集成到自动化工作流中。

### 自定义模板
支持使用自有设计/模板，保持品牌一致性。

## 技术架构

- **许可**：Apache 2.0
- **前端**：Web UI + 桌面应用
- **部署**：Docker / Windows / macOS / Linux
- **模型**：可插拔式多提供商

## 安装与使用

```bash
# Docker 部署
docker compose up -d
```

桌面应用下载：https://presenton.ai/download

## GitHub

https://github.com/presenton/presenton
