# macpow

> GitHub | https://github.com/k06a/macpow

## 项目简介

macpow 是 Apple Silicon Mac（M1–M5+）的实时功耗监控 TUI 工具，直接从 macOS 硬件接口（IOReport、SMC、IORegistry、CoreAudio、Mach/Kernel API）读取数据，显示每个组件的功耗、温度、频率、CPU 利用率和进程级能耗归因。无需 sudo。Rust 实现。

## 核心功能

- **SoC 分解**：CPU（E/P 核逐核功耗、利用率条、温度）、GPU、ANE、DRAM、GPU SRAM、Media Engine、Camera（ISP）、Fabric
- **CPU 利用率**：逐核使用率 % + 可视化条形图
- **实时频率**：CPU 和 GPU 真实 MHz（来自 DVFS 电压状态表）
- **温度**：逐组件逐核 SMC 传感器（CPU/GPU/ANE/DRAM/SSD/电池），自适应 M1-M3 和 M4+ 不同 Key 映射
- **内存**：已用/总量 GB
- **显示器**：亮度 + SoC 显示控制器功耗 + 外接显示器功耗
- **电池**：电压/电流/电量/剩余时间/温度/充放电速率
- **外设**：Thunderbolt/PCIe、以太网、WiFi、蓝牙设备电量、USB 设备
- **进程级能耗**：按会话能耗排序的 Top 进程，含磁盘 I/O、网络流量、RAM 占用
- **风扇**：RPM + 三次方功耗模型
- **可折叠树形视图**：方向键折叠/展开
- **火花线图表**：Space 键固定任意资源，宽终端显示内联历史
- **JSON 模式**：管道输出结构化数据

## 安装

```bash
cargo install macpow
# 或
brew tap k06a/tap && brew install macpow
```

## 技术规格

- **语言**：Rust
- **平台**：Apple Silicon（M1–M5+）
- **权限**：无需 sudo
- **Stars**：236
- **许可证**：MIT

## 相关链接

- GitHub: https://github.com/k06a/macpow
- Crates.io: https://crates.io/crates/macpow
