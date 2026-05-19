# Audiblez

将电子书（.epub）自动转为有声书（.m4b）的开源工具，基于 Kokoro-82M 高质量语音合成模型，支持多语言多音色，GPU 加速。

## 核心特性

### 电子书 → 有声书一键转换
输入 `.epub` 电子书文件，自动按章节拆分并用 AI 语音朗读，最终合成 `.m4b` 有声书文件，可用 VLC 或任意有声书播放器播放。

### Kokoro-82M 语音合成
基于 [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) 模型（8200 万参数、Apache 开源协议、训练数据 < 100 小时），输出语音自然流畅，支持 9 种语言：

| 语言 | 示例音色 |
|------|----------|
| 🇺🇸 美式英语 | `af_sky`, `af_bella`, `am_adam`, `am_liam` 等 20 种 |
| 🇬🇧 英式英语 | `bf_emma`, `bm_george` 等 8 种 |
| 🇪🇸 西班牙语 | `ef_dora`, `em_alex` |
| 🇫🇷 法语 | `ff_siwis` |
| 🇮🇳 印地语 | `hf_alpha`, `hm_omega` |
| 🇮🇹 意大利语 | `if_sara`, `im_nicola` |
| 🇯🇵 日语 | `jf_alpha`, `jm_kumo` 等 5 种 |
| 🇧🇷 葡萄牙语 | `pf_dora`, `pm_alex` |
| 🇨🇳 中文普通话 | `zf_xiaobei`, `zf_xiaoxiao`, `zm_yunjian`, `zm_yunyang` 等 8 种 |

### GPU 加速 (CUDA)
支持 `--cuda` 参数启用 GPU 推理。Google Colab T4 上转换《动物农场》（约 16 万字符）仅需 5 分钟，约 600 字符/秒；M2 MacBook Pro CPU 约 1 小时，约 60 字符/秒。

### 图形界面 (GUI)
提供基于 wxPython 的桌面 GUI (`audiblez-ui`)，可视化选择电子书文件、音色、语速等参数。

### 语速调节
支持 0.5x 到 2.0x 语速调节（`-s` 参数），可生成加速或减速版有声书。

### 章节选择
`--pick` 参数可交互式选择需要朗读的章节，跳过不感兴趣的部分。

## 技术架构

- **语音引擎**: Kokoro-82M (ONNX 模型，Apache 2.0 协议)
- **加速**: PyTorch + CUDA (GPU)，CPU 模式兜底
- **音频处理**: ffmpeg（WAV 合并 → M4B 封装）
- **文本处理**: espeak-ng（音素转换）
- **电子书解析**: ebooklib（EPUB 文件解析）
- **GUI**: wxPython + Pillow
- **打包管理**: Poetry (pyproject.toml)

## 安装与使用

```bash
# 安装依赖
sudo apt install ffmpeg espeak-ng       # Ubuntu/Debian
brew install ffmpeg espeak-ng           # macOS

# 安装 audiblez
pip install audiblez

# CLI 使用
audiblez book.epub -v af_sky            # 美式英语女声
audiblez book.epub -v zf_xiaoxiao       # 中文女声
audiblez book.epub -v af_sky -s 1.5     # 1.5 倍速
audiblez book.epub -v af_sky --cuda     # GPU 加速
audiblez book.epub -v af_sky --pick     # 交互式选章节

# GUI
audiblez-ui
```

## 性能参考

| 环境 | 速度 | 转换《动物农场》(16万字符) |
|------|------|---------------------------|
| Google Colab T4 (CUDA) | ~600 chars/s | ~5 分钟 |
| M2 MacBook Pro (CPU) | ~60 chars/s | ~1 小时 |

## GitHub

https://github.com/santinic/audiblez
