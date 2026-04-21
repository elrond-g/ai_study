# Ground Station

> ⭐ 4.2k | GPL-3.0 | https://github.com/sgoudelis/ground-station

## 项目简介

面向业余无线电爱好者和卫星发烧友的开源卫星监测与无线电通信平台，融合 SDR 硬件、自动化天线控制和 AI 转录能力，让个人也能运行一个完整的小型地面站。

## 核心特性

- **实时卫星追踪**：自动更新 TLE 数据
- **SDR 支持**：RTL-SDR / SoapySDR / UHD/USRP
- **自动化控制**：天线旋转器、收发机控制 + 多普勒补偿
- **信号解码**：SSTV / FSK / GMSK / BPSK
- **IQ 录制/回放**：SigMF 格式
- **AI 转录**：Gemini Live 或 Deepgram 语音识别
- **计划观测**：定时自动任务
- **气象卫星图像**：SatDump 集成解码

## 技术栈

- **前端**：React + Redux Toolkit + Material-UI
- **后端**：FastAPI + Socket.IO
- **关键库**：Skyfield、SGP4、SoapySDR、gr-satellites

## 使用场景

- 业余卫星通信爱好者
- 无线电教育实验
- 气象卫星图像接收
- SIGINT 研究和 SDR 学习

## 相关链接

- GitHub: https://github.com/sgoudelis/ground-station
