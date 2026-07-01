---
tags: [concept, tool, mcp, browser-automation]
sources: [ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md]
created: 2026-07-01
updated: 2026-07-01
---

# Chrome DevTools MCP

通过 [[MCP Protocol]] 将 Chrome DevTools 的完整能力暴露给 AI coding agent 的具体实现。由 Google Chrome DevTools 团队开发维护。

## 核心能力

- **性能分析** — 录制 trace，提取可操作的性能洞察，支持 CrUX 真实用户数据对比
- **高级调试** — 分析网络请求、截图、查看控制台消息（含 source-mapped 堆栈）
- **可靠自动化** — 基于 [[Puppeteer]]，自动等待操作结果

## 工具覆盖

提供 49+ 个工具，分 8 大类别：
- 输入自动化（10）：click、drag、fill、type_text 等
- 导航（6）：navigate_page、new_page、list_pages 等
- 模拟（2）：emulate 设备、resize_page
- 性能（3）：录制/停止 trace、分析洞察
- 网络（2）：列出/获取网络请求
- 调试（8）：截图、控制台消息、脚本执行、lighthouse 审计
- 内存（11）：堆快照、比较、支配者分析
- 扩展（5）：安装/卸载/重载/触发扩展

## 连接模式

1. **默认模式** — MCP Server 自动启动新的 Chrome 实例（专用 profile）
2. **Auto-connect（Chrome 144+）** — 自动连接到用户已运行的 Chrome，适合手动测试与 agent 测试共享状态
3. **Remote debugging 端口** — 通过 `--browser-url` 连接已有实例，适合沙箱环境

## 支持的 AI 客户端

[[Claude Code]]、Cursor、Copilot/VS Code、Gemini CLI、Codex、Cline、Amp、Windsurf 等 20+ 种。
