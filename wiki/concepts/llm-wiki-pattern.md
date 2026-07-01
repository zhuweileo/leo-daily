---
tags: [concept, pattern, knowledge-base]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# LLM Wiki Pattern

一种用 LLM 增量构建和维护持久个人知识库的设计模式，由 [[Andrej Karpathy]] 提出，[[Nicholas Spisak]] 通过 [[Second Brain]] 项目实现。

## 核心思想

区别于传统 RAG 模式（每次查询时重新检索原始文档），LLM Wiki 将知识**编译一次并持续更新**。LLM 充当"图书管理员"，负责读取素材、提取信息、创建和更新 wiki 页面、维护交叉引用。用户充当"策展人"，负责收集素材和提出问题。

wiki 是一个**持久、复利式的产物**——交叉引用已建好，矛盾已标记，综合分析已反映所有已读内容。每次添加新素材，wiki 都变得更丰富，而不是每次从零开始。

## 适用场景

- 个人记录和自我提升
- 深度研究和长期项目
- 读书笔记（类 Wiki 模式）
- 团队知识管理
- 竞品分析、尽职调查、旅行规划、课程笔记等

## 灵感来源

与 [[Vannevar Bush]] 1945 年的 [[Memex]] 概念一脉相承。Bush 提出个人化知识存储的愿景，但无法解决"谁来维护"的问题。LLM 正好填补了这个角色。

## 相关概念

- [[RAG vs Wiki]] — 与传统 RAG 的对比
- [[Three-layer Architecture]] — 实现架构
- [[Persistent Compounding Artifact]] — 复利式积累理念
