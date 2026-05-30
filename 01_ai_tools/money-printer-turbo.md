# MoneyPrinterTurbo

国产 AI 短视频一键生成工具。只需提供视频主题或关键词，即可全自动生成视频文案、素材、字幕、背景音乐，最终合成高清短视频。支持 Web 界面和 API 两种使用方式。

## 核心特性

### 全自动视频生成
AI 自动撰写文案 → 匹配视频素材 → 语音合成 → 字幕生成 → 背景音乐 → 合成输出，全程自动化。

### 多模型支持
支持 OpenAI、Moonshot、Azure、DeepSeek、通义千问、文心一言、Google Gemini、Ollama 等多种 LLM 提供商。

### 灵活的视频格式
- 竖屏 9:16（1080x1920）
- 横屏 16:9（1920x1080）
- 支持批量生成，一次生成多个视频供挑选

### 完整的 MVC 架构
代码结构清晰，支持 Web 界面和 API 两种方式，方便集成和二次开发。

## 技术架构

- **后端**：Python，MVC 架构
- **LLM**：可插拔式多模型支持
- **素材**：高清无版权素材，支持本地素材
- **部署**：支持本地运行

## 安装与使用

```bash
git clone https://github.com/harry0703/MoneyPrinterTurbo.git
cd MoneyPrinterTurbo
pip install -r requirements.txt
python webui.py
```

## GitHub

https://github.com/harry0703/MoneyPrinterTurbo
