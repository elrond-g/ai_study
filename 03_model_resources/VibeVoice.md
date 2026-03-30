# VibeVoice

> 微软 | PyTorch | https://github.com/microsoft/VibeVoice

## 项目简介

VibeVoice 是微软开源的前沿语音 AI 模型系列，包含文本转语音（TTS）、自动语音识别（ASR）和实时流式 TTS 三大组件。核心创新是 Next-Token Diffusion 框架，融合 LLM 理解能力和扩散模型的高保真生成能力。

## 三大组件

### VibeVoice-TTS（文本转语音）
- 支持长达 90 分钟连续语音合成
- 最多 4 个不同说话人
- 自然处理转换、停顿、呼吸等非词汇细节
- 1.5B 参数规模

### VibeVoice-ASR（语音识别）
- 单次处理长达 60 分钟连续音频（64K token）
- 统一实现语音识别 + 说话人分段 + 时间戳
- 50+ 语言支持，原生代码转换
- 自定义热词提升领域识别准确率
- 输出结构化转录：Who + When + What

### VibeVoice-Realtime-0.5B（实时流式 TTS）
- 初始延迟仅 ~300ms
- 流式文本输入，文本 token 到达即开始合成
- 0.5B 轻量级，支持 LLM "边思考边说话"
- 当前仅支持英文单说话人

## 核心技术创新

- **连续语音分词器**：超低帧率 7.5Hz，声学（VAE）+ 语义（分层编码器）双分词器
- **Next-Token Diffusion**：自回归生成语音 token + DPM-Solver 扩散头转换为高质量音频

## 平台支持

CUDA GPU、Apple Silicon (MPS)、CPU 多平台；支持 bfloat16 + flash_attention_2 加速；Hugging Face Transformers 集成

## 注意事项

微软因负责任 AI 原则，已从官方仓库移除 TTS 部分代码（发现被用于虚假音频等场景）。ASR 和 Realtime 组件仍正常维护。

## 相关链接

- GitHub: https://github.com/microsoft/VibeVoice
- 官网: https://microsoft.github.io/VibeVoice/
- TTS 论文: https://arxiv.org/abs/2508.19205
- ASR 论文: https://arxiv.org/abs/2601.18184
- HuggingFace: https://huggingface.co/microsoft/VibeVoice-1.5B
