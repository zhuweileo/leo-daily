---
tags: [concept, operation, workflow]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# Query Operation

[[LLM Wiki Pattern]] 中的查询操作——基于 wiki 回答用户问题的流程。

## 流程

1. 读取 `wiki/index.md` 找到相关页面
2. 阅读相关 wiki 页面
3. 用 `[[wikilink]]` 引用综合出答案
4. 如果答案产出有价值的产物（比较、分析、新关联），提议保存为 `wiki/synthesis/` 中的新页面
5. 如果保存了新页面，更新 index 和 log

## 关键洞察

好的查询答案可以**归档回 wiki** 作为新页面——比较、分析、发现的关联都是有价值的，不应消失在聊天历史中。这使得探索成果和摄入的素材一样能复利积累。

## 输出形式

答案可以采用不同格式：markdown 页面、比较表格、幻灯片（Marp）、图表（matplotlib）、canvas 等。

## 在 Second Brain 中的实现

通过 `/second-brain-query` slash command 触发。
