---
tags: [tool, ai-agent, claude]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md]
created: 2026-07-01
updated: 2026-07-01
---

# Claude Code

Anthropic 推出的 AI 编程 agent（CLI 工具）。是 [[Second Brain]] 项目支持的主要 AI agent 之一，通过 `CLAUDE.md` 配置文件定义 [[Three-layer Architecture]] 中的 schema 层。

在 [[LLM Wiki Pattern]] 的工作流中，Claude Code 扮演"图书管理员"角色，负责读取原始素材、编译 wiki 页面、维护交叉引用和索引。用户通过 slash command（如 `/second-brain-ingest`）与 agent 交互。

Claude Code 也支持 [[MCP Protocol]]，可作为 MCP Client 连接 [[Chrome DevTools MCP]] 等 MCP Server，获得浏览器控制、性能分析等扩展能力。安装方式：`claude mcp add chrome-devtools --scope user npx chrome-devtools-mcp@latest`。
