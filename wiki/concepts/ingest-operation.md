---
tags: [concept, operation, workflow]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# Ingest Operation

[[LLM Wiki Pattern]] 中的素材摄入操作——将原始文档编译到 wiki 中的流程。

## 流程

1. 用户将新素材放入 `raw/` 目录
2. LLM 完整阅读素材
3. 与用户讨论关键要点
4. 在 `wiki/sources/` 创建摘要页
5. 识别素材中提到的所有实体和概念，更新或创建对应 wiki 页面
6. 添加 `[[wikilinks]]` 交叉引用
7. 更新 `wiki/index.md`
8. 在 `wiki/log.md` 追加记录

## 特点

- 单个素材通常会影响 **10-15 个 wiki 页面**，这是正常的
- 建议逐个摄入并在过程中保持参与——阅读摘要、检查更新、指导 LLM 强调重点
- 也可以批量摄入多个素材，减少监督

## 在 Second Brain 中的实现

通过 `/second-brain-ingest` slash command 触发，自动检测 `raw/` 中未处理的文件。
