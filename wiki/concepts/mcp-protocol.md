---
tags: [concept, protocol, standard, ai]
sources: [ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md]
created: 2026-07-01
updated: 2026-07-01
---

# MCP Protocol

Model Context Protocol（模型上下文协议）——一种让 AI agent 与外部工具和服务通信的标准协议。MCP Server 暴露一组工具（tools），MCP Client（AI coding agent）通过标准化的 JSON-RPC 接口调用这些工具。

## 应用实例

[[Chrome DevTools MCP]] 是 MCP 的一个典型应用：通过 MCP Server 将 Chrome DevTools 的完整能力（49+ 个工具）暴露给 20+ 种 AI coding agent（包括 [[Claude Code]]、Cursor、Copilot、Gemini CLI 等）。用户只需在 MCP 客户端配置中添加一行 `npx chrome-devtools-mcp@latest` 即可启用。

## 价值

MCP 标准化解决了 AI agent 与工具之间的互操作性问题——同一个 MCP Server 可以被任何支持 MCP 协议的 agent 使用，无需为每个 agent 单独开发集成。
