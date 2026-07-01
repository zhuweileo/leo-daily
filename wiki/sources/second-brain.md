---
tags: [clippings, second-brain, knowledge-base, obsidian]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md]
created: 2026-07-01
updated: 2026-07-01
---

# Second Brain

**Source:** NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md
**Date ingested:** 2026-07-01
**Type:** documentation (GitHub README)

## Summary

Second Brain 是一个基于 [[Andrej Karpathy]] 的 [[LLM Wiki Pattern]] 构建的 LLM 维护的个人知识库项目。它提供了完整的 skill 工具链，让用户可以在 [[Obsidian]] 中浏览结构化的 wiki。核心理念是"LLM 是图书管理员，用户是策展人"——用户负责收集素材，LLM 负责编译、交叉引用和维护。

项目支持多种 AI agent（[[Claude Code]]、Codex、Cursor、Gemini CLI），通过 [[Agent Skills]] 开放标准统一接口。安装后提供四个核心 skill：onboarding（初始化 vault）、ingest（处理素材）、query（查询）、lint（健康检查）。

## Key Claims

- LLM 维护的 wiki 比传统 RAG 更有效——知识是增量编译的，不是每次查询时重新检索
- 知识库的维护成本接近为零，因为 LLM 不会忘记更新交叉引用
- 支持多种 AI agent 协同工作在同一 vault 上
- wiki 可以作为 git repo 来获得版本控制和协作能力

## Entities Mentioned

- [[Andrej Karpathy]] — [[LLM Wiki Pattern]] 的原创者
- [[Nicholas Spisak]] — Second Brain 项目的创建者
- [[Obsidian]] — 用于浏览 wiki 的 markdown 编辑器
- [[Claude Code]] — 支持的 AI agent 之一
- [[Agent Skills]] — 开放标准，统一不同 AI agent 的 skill 接口

## Concepts Covered

- [[LLM Wiki Pattern]] — 核心设计模式
- [[Three-layer Architecture]] — raw/wiki/schema 三层架构
- [[Ingest Operation]] — 素材摄入流程
- [[Query Operation]] — 查询流程
- [[Lint Operation]] — 健康检查流程
