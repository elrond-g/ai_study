# Scrapling

🕷️ 自适应 Web 抓取框架，从单次请求到全规模爬虫覆盖全场景。智能解析器能在网站改版后自动重定位元素，内置反爬绕过（Cloudflare Turnstile 开箱即用），支持并发多会话爬虫 + 暂停恢复 + 代理轮换。

## 核心特性

### 爬虫框架 (Spiders)

- 🕷️ **类 Scrapy API**：定义 `start_urls`、async `parse` 回调、`Request`/`Response` 对象
- ⚡ **并发抓取**：可配置并发数、按域名限速、下载延迟
- 🔄 **多会话支持**：HTTP / 隐身浏览器（Playwright/Chrome）统一接口，按 session ID 路由请求
- 💾 **暂停与恢复**：基于 checkpoint 的持久化，Ctrl+C 优雅停止后重启即可从断点继续
- 📡 **流式模式**：`async for item in spider.stream()` 实时输出 + 统计，适合长任务和 UI 集成
- 🛡️ **封锁检测**：自动检测被屏蔽请求并重试
- 🤖 **robots.txt 遵从**：可选遵守 Disallow / Crawl-delay / Request-rate
- 🧪 **开发模式**：首次抓取缓存响应到磁盘，后续运行直接回放，不反复请求目标站

### 高级页面抓取 (Fetchers)

- **HTTP 请求**：`Fetcher` 类，支持 TLS 指纹伪装、HTTP/3、浏览器 header 伪造
- **动态加载**：`DynamicFetcher` 基于 Playwright Chromium / Google Chrome 的浏览器自动化
- **反爬绕过**：`StealthyFetcher` 高级隐身，可绕过 Cloudflare Turnstile / Interstitial
- **会话管理**：`FetcherSession` / `StealthySession` / `DynamicSession` 持久会话 + Cookie/状态管理
- **代理轮换**：内置 `ProxyRotator`，支持循环/自定义策略，可逐请求覆盖代理
- **域名/广告屏蔽**：阻止特定域名请求，内置 ~3500 广告追踪域名列表
- **DNS 防泄漏**：可选 DNS-over-HTTPS，防止代理场景下的 DNS 泄漏
- **完整 Async 支持**：所有 Fetcher 均有异步版本

### 自适应抓取与 AI 集成

- 🔄 **智能元素追踪**：网站改版后通过相似度算法自动重定位目标元素
- 🎯 **灵活选择器**：CSS 选择器、XPath、过滤器搜索、文本搜索、正则搜索
- 🔍 **相似元素查找**：自动定位与已找到元素相似的兄弟元素
- 🤖 **MCP 服务器**：内置 MCP server，供 Claude/Cursor 等 AI 使用，可预提取内容后传给 AI 以降低 token 消耗

### 高性能架构

- 🚀 **极致性能**：文本提取速度远超 BS4（~784x）、MechanicalSoup（~767x）
- 🔋 **内存高效**：优化数据结构 + 懒加载，最小化内存占用
- ⚡ **快速序列化**：JSON 序列化比标准库快 10 倍
- 🏗️ **久经考验**：92% 测试覆盖率，完整 type hints，日常数百名爬虫工程师使用

### 开发者友好体验

- 🎯 **交互式 Shell**：内置 IPython Shell，集成 Scrapling 快捷操作和工具
- 🚀 **CLI 工具**：无需写代码即可从终端抓取网页内容
- 🧬 **增强文本处理**：内置正则、清洗方法、优化字符串操作
- 📝 **自动选择器生成**：为任意元素自动生成鲁棒 CSS/XPath 选择器
- 📘 **完整类型覆盖**：全 type hints，PyRight + MyPy 自动扫描
- 🔋 **Docker 镜像**：每次发布自动构建含全部浏览器的 Docker 镜像

## 性能基准

| 库 | 耗时 (ms) | 相对 Scrapling |
|---|---|---|
| **Scrapling** | 2.02 | 1.0x |
| Parsel/Scrapy | 2.04 | 1.01x |
| Raw Lxml | 2.54 | 1.26x |
| PyQuery | 24.17 | ~12x |
| Selectolax | 82.63 | ~41x |
| MechanicalSoup | 1549.71 | ~767x |
| BS4 + Lxml | 1584.31 | ~784x |
| BS4 + html5lib | 3391.91 | ~1679x |

*元素相似度搜索：Scrapling 2.39ms vs AutoScraper 12.45ms（5.2x 差距）*

## 技术架构

- **语言**：Python 3.10+
- **解析引擎**：基于 lxml 的高性能 HTML 解析
- **浏览器自动化**：Playwright（Chromium）+ Google Chrome
- **网络**：HTTP/1.1、HTTP/2、HTTP/3（QUIC），TLS 指纹伪装
- **AI 集成**：MCP (Model Context Protocol) 服务器

## 安装与使用

```bash
# 基础安装（仅解析器）
pip install scrapling

# 含 Fetchers 及浏览器依赖
pip install "scrapling[fetchers]"

# 完整安装（含 CLI 工具）
pip install "scrapling[all]"

# CLI 快速抓取（无需写代码）
scrapling extract get 'https://example.com' content.md

# 交互式 Shell
scrapling shell
```

## GitHub

https://github.com/D4Vinci/Scrapling
