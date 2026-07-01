---
tags: [clippings, chrome-devtools, mcp, browser-automation]
sources: [ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md]
created: 2026-07-01
updated: 2026-07-01
---

# Chrome DevTools MCP

**Source:** ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md
**Date ingested:** 2026-07-01
**Type:** documentation (GitHub README)

## Summary

Google Chrome DevTools 团队推出的 MCP Server（`chrome-devtools-mcp`），让 AI coding agent 能够控制和检查实时 Chrome 浏览器。基于 [[MCP Protocol]] 标准实现，暴露完整的 Chrome DevTools 能力，包括性能分析、高级调试和可靠浏览器自动化。

提供 49+ 个工具，覆盖输入自动化、导航、设备模拟、性能分析、网络请求、调试、内存分析、扩展管理等类别。支持 20+ 种 AI 客户端（包括 [[Claude Code]]、Cursor、Copilot、Gemini CLI、Codex 等）。底层基于 [[Puppeteer]] 实现浏览器自动化。

## Key Claims

- AI agent 可通过 MCP 协议获得 Chrome DevTools 的完整能力——性能录制、网络分析、截图、控制台消息（含 source-mapped 堆栈）
- 基于 Puppeteer 的自动化比脚本更可靠——自动等待操作结果
- 支持 auto-connect（Chrome 144+）或 remote debugging 端口连接已有 Chrome 实例
- 提供 slim 模式（仅导航、脚本执行、截图 3 个工具）用于基础浏览器任务
- Google 默认收集使用统计数据，可通过 `--no-usage-statistics` 退出

## Entities Mentioned

- [[Chrome DevTools]] — Google 的浏览器开发者工具，MCP Server 的能力来源
- [[Puppeteer]] — Node.js 浏览器自动化库，MCP Server 的底层实现
- [[MCP Protocol]] — Model Context Protocol，连接 AI agent 和工具的标准协议
- [[Claude Code]] — 支持的 AI 客户端之一

## Concepts Covered

- [[MCP Protocol]] — AI agent 与工具通信的标准协议
- [[Chrome DevTools MCP]] — 通过 MCP 将 DevTools 能力暴露给 AI agent 的具体实现
