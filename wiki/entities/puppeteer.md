---
tags: [tool, automation, browser, nodejs]
sources: [ChromeDevToolschrome-devtools-mcp Chrome DevTools for coding agents.md]
created: 2026-07-01
updated: 2026-07-01
---

# Puppeteer

Google 维护的 Node.js 浏览器自动化库（github.com/puppeteer/puppeteer）。提供控制 Chrome/Chromium 的高级 API，支持无头模式、页面截图、网络拦截、PDF 生成等。

在 [[Chrome DevTools MCP]] 项目中，Puppeteer 作为底层实现，负责浏览器自动化操作（如点击、填充表单、导航、截图等），并提供自动等待操作结果的机制，使 AI agent 驱动的浏览器操作更加可靠。
