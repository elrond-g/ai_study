# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a **pure documentation repository** — a curated index of AI tools, frameworks, and learning resources written in Chinese. There is no executable code, build system, or test suite. All content lives in Markdown files.

## File Structure

- `100.ai_study_index.md` — Main comprehensive index (the authoritative content file)
- `INDEX.md` — Navigation guide
- `SUMMARY.md` — Quick overview
- `README.md` — Entry point (minimal)

Individual topic notes live in numbered subdirectories mirroring the six sections:

- `01_ai_tools/` — Detailed notes on AI tools and agents
- `02_dev_frameworks/` — Dev framework deep-dives
- `03_model_resources/` — Model implementation notes
- `04_context_memory/` — Context/memory system notes
- `05_claude_code_ecosystem/` — Claude Code skills and ecosystem
- `06_learning_resources/` — Tutorials, courses, notable developers

Each subdirectory file follows the same template: project name as H1, a brief intro, core features, technical notes, and a GitHub link.

## Content Organization

The main index (`100.ai_study_index.md`) is divided into six sections:

1. **AI 工具与应用** — Agent frameworks, browser automation, coding assistance, vertical apps, CLI tools
2. **开发框架与基建** — Model integration (LiteLLM, LangChain, CrewAI), infra services, MCP
3. **模型资源** — Model implementations and performance tools
4. **Context 与记忆管理** — Knowledge storage, long-term memory, RAG systems
5. **Claude Code 生态** — Skills (general/design/science), prompt engineering, cost optimization
6. **学习资源** — Tutorials and notable developers

## Editing Conventions

- Each section uses Markdown tables with two columns: project link and Chinese description
- Links use `[name](url)` format pointing to GitHub repos or external pages
- Bold table rows (e.g., `**LangChain 系列**`) group related items without individual links
- Section separators use `---`
- Keep descriptions concise — one line per entry
- Maintain table alignment when adding rows
