# opencli-rs

opencli 的 Rust 重写版本，极快、内存安全的命令行工具，从 55+ 网站和应用中快速获取信息，支持 Electron 桌面应用控制和本地 CLI 工具集成。

## 核心特性

- **55 个网站 + 333 条命令**：覆盖 Twitter/X、Reddit、YouTube、HackerNews、Bilibili、知乎、小红书等
- **Electron 应用 CLI 化**：将 Cursor、ChatGPT、Notion、Discord 等桌面应用转为命令行操作
- **浏览器登录态复用**：无需管理 token，直接复用浏览器已有登录状态
- **极致性能**：单个 4.7MB 二进制文件，零运行时依赖，比 JS 版快 12 倍，内存占用减少 10 倍

## 与 opencli（JS 版）对比

| 指标 | opencli (JS) | opencli-rs (Rust) |
|------|-------------|-------------------|
| 速度 | 基准 | 快 12 倍 |
| 内存 | 基准 | 减少 10 倍 |
| 体积 | 需要 Node.js | 单文件 4.7MB |

## 链接

- GitHub: https://github.com/nashsu/opencli-rs
