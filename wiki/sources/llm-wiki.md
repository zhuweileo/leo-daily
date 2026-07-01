---
tags: [clippings, llm-wiki, knowledge-base, pattern]
sources: [llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# LLM Wiki

**Source:** llm-wiki.md
**Date ingested:** 2026-07-01
**Type:** documentation (GitHub Gist)

## Summary

[[Andrej Karpathy]] 提出的 [[LLM Wiki Pattern]] 的原始定义文档。阐述了用 LLM 增量构建和维护持久 wiki 的核心理念，区别于传统 RAG 模式。wiki 是一个持久的、复利式的产物——交叉引用已经建好，矛盾已被标记，综合分析已反映所有已读内容。每次添加新素材，wiki 都会变得更丰富。

LLM 负责所有维护工作（摘要、交叉引用、归档），用户负责策源、探索和提问。灵感来源于 [[Vannevar Bush]] 1945 年的 [[Memex]] 概念。适用于个人记录、深度研究、读书笔记、团队知识管理等多种场景。

## Key Claims

- 传统 RAG 每次查询时重新发现知识，而 wiki 将知识编译一次并持续更新
- wiki 是持久、复利式的产物——随着素材积累不断增值
- 维护知识库最繁琐的部分不是阅读和思考，而是维护交叉引用和一致性
- LLM 不会厌倦、不会忘记更新引用，一次可以处理 15 个文件
- 人类的工作是策源和思考，LLM 的工作是其余一切
- 与 [[Vannevar Bush]] 的 Memex 理念一脉相承，LLM 解决了"谁来维护"的问题

## Entities Mentioned

- [[Andrej Karpathy]] — 作者，LLM Wiki 模式的提出者
- [[Obsidian]] — 推荐的 wiki 浏览工具
- [[Vannevar Bush]] — Memex 概念的提出者（1945）
- [[Tolkien Gateway]] — 作为粉丝 wiki 的类比案例

## Concepts Covered

- [[LLM Wiki Pattern]] — 核心模式定义
- [[RAG vs Wiki]] — 与传统 RAG 的对比
- [[Three-layer Architecture]] — raw/wiki/schema 架构
- [[Persistent Compounding Artifact]] — 持久复利式产物理念
- [[Memex]] — 灵感来源
- [[Ingest Operation]] — 摄入操作
- [[Query Operation]] — 查询操作
- [[Lint Operation]] — 健康检查操作
