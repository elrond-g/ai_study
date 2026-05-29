# VoxCPM

OpenBMB 开源的**无分词器**（Tokenizer-Free）语音合成系统，通过端到端**扩散自回归架构**直接生成连续语音表征，绕过音频离散编码，实现高度自然且富有表现力的语音合成。当前主推 **VoxCPM2**（2B 参数，200 万+ 小时多语种训练，支持 30 种语言 + 9 种中文方言，48kHz 输出，Apache-2.0 开源商用）。

## 核心特性

### 多语言语音合成
支持 30 种全球语言（中/英/日/韩/阿/法/德/西/葡/俄/泰/越等）和 9 种中文方言（四川话/粤语/吴语/东北话等），无需语言标签，直接输入原始文本即可合成。

### 音色设计（Voice Design）
用自然语言描述（性别、年龄、音色、情绪、语速）凭空创建全新音色，无需任何参考音频。VoxCPM2 支持文本指令和特征向量两种控制方式。

### 可控声音克隆
从短参考音频片段克隆任意声音，同时可叠加风格指令（语速调整、情绪变化、表现力控制），在保持原始音色基础上灵活调节输出风格。

### 极致克隆（Ultimate Cloning）
提供参考音频及对应文本，模型接续参考音频进行无缝续写，精准还原声音细节——音色、节奏、情感和风格完全保持（与 VoxCPM1.5 一致）。

### 48kHz 高保真音频
基于 AudioVAE V2 非对称编解码设计：输入 16kHz 参考音频，直接输出 48kHz 演播室级音频，内置超分能力，无需外接上采样器。

### 语境感知合成
根据文本语义内容自动推断合适的韵律和表现力，生成符合语境的自然语音。

### 实时流式合成
NVIDIA RTX 4090 上 RTF 低至 ~0.3；通过 [Nano-vLLM](https://github.com/a710128/nanovllm-voxcpm) 或 [vLLM-Omni](https://github.com/vllm-project/vllm-omni)（基于 PagedAttention + OpenAI 兼容 API）加速后可达 ~0.13。

## 技术架构

- **架构**: 扩散自回归（Diffusion Autoregressive），无离散音频分词器，端到端连续表征生成
- **基座模型**: MiniCPM-4 LLM 作为文本理解 backbone
- **音频编码**: AudioVAE V2 — 非对称编解码（16kHz 输入 → 48kHz 输出），内置超分辨率
- **参数量**: VoxCPM2 2B（20 亿），VoxCPM1.5 1.5B，VoxCPM-0.5B 0.5B
- **训练数据**: 200 万+ 小时多语种音频
- **推理加速**: 支持 vLLM-Omni 官方全模态服务（PagedAttention + 连续批处理）

## 版本演进

| 版本 | 发布日期 | 参数量 | 关键能力 |
|------|---------|--------|---------|
| VoxCPM-0.5B | 2025.09 | 0.5B | 基础 TTS，Tokenizer-Free |
| VoxCPM1.5 | 2025.12 | 1.5B | SFT/LoRA 微调，Ultimate Cloning |
| VoxCPM2 | 2026.04 | 2B | 30 语言、Voice Design、Controllable Cloning、48kHz |

## 安装与使用

```bash
pip install voxcpm
```

要求: Python ≥ 3.10 (<3.13), PyTorch ≥ 2.5.0, CUDA ≥ 12.0

```python
from voxcpm import VoxCPM
import soundfile as sf

model = VoxCPM.from_pretrained("openbmb/VoxCPM2", load_denoiser=False)

# 基本 TTS
wav = model.generate(text="你好，世界！", cfg_value=2.0, inference_timesteps=10)
sf.write("output.wav", wav, model.tts_model.sample_rate)

# 音色设计
wav = model.generate(
    text="(年轻女性，声音温柔甜美)你好，欢迎使用VoxCPM2！",
    cfg_value=2.0, inference_timesteps=10
)

# 声音克隆
wav = model.generate(
    text="这是 VoxCPM2 生成的克隆声音。",
    reference_wav_path="path/to/voice.wav"
)
```

## 生态与部署

- **在线体验**: [HuggingFace Demo](https://huggingface.co/spaces/OpenBMB/VoxCPM-Demo) | [官网](https://voxcpm.modelbest.cn/)
- **生产部署**: 支持 vLLM-Omni（OpenAI 兼容 API，PagedAttention 加速），Nano-vLLM 社区加速方案
- **微调**: VoxCPM1.5 起支持 SFT 和 LoRA 微调
- **模型下载**: [HuggingFace](https://huggingface.co/openbmb/VoxCPM2) | [ModelScope](https://modelscope.cn/models/OpenBMB/VoxCPM2)
- **文档**: [ReadTheDocs](https://voxcpm.readthedocs.io/)
- **论文**: [VoxCPM Technical Report](https://arxiv.org/abs/2509.24650)

## GitHub

https://github.com/OpenBMB/VoxCPM
