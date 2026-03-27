# read-in-cli (RICLI)

终端电子书阅读器，在命令行中阅读 EPUB 和 TXT 格式书籍。

## 核心功能

- **格式支持** — EPUB 和 TXT（TXT 自动检测章节）
- **书架管理** — 打开过的书自动记录，启动时直接选择，支持删除记录
- **进度记忆** — 阅读位置自动保存，下次打开同一本书自动恢复
- **目录跳转** — 按 `t` 打开目录，快速切换章节
- **Vi 风格快捷键** — hjkl 导航、翻页、跳转章首/章尾
- **主题配置** — 支持自定义前景/背景色、边距、每页行数等，颜色支持命名色和十六进制

## 安装与使用

```bash
npm install -g @alfxjx/ricli

ricli book.epub       # 直接打开
ricli                 # 进入书架选择
ricli config          # 查看/修改配置
```

## 技术栈

- JavaScript (Node.js)
- 配置文件存储在 `~/.ricli/config.json`

## 链接

- GitHub: https://github.com/Alfxjx/read-in-cli
