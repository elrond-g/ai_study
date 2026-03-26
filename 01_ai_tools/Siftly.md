# Siftly

本地运行的 Twitter/X 书签组织工具，使用 AI 自动分类和标签化保存的推文，生成交互式思维导图可视化。完全离线，无需云服务、订阅或浏览器扩展。

## 核心特性

- **本地优先**：所有处理在本机运行，无云依赖
- **AI 自动分类**：使用 Claude AI 自动为推文分类打标签
- **丰富元数据提取**：挖掘 hashtag、URL、@提及、工具/产品名称
- **图片高级分析**：OCR 文字识别、物体/场景检测、情绪分析、meme 模板识别
- **思维导图可视化**：生成交互式知识图谱探索保存内容
- **全文可搜索**：将书签转化为可搜索的知识库
- **零配置**：克隆后运行启动脚本，自动打开 localhost:3000

## 技术栈

- TypeScript
- 自动检测 macOS Keychain 中的 Claude CLI 认证
- 使用 Claude 订阅额度

## 链接

- GitHub: https://github.com/viperrcrypto/Siftly
