---
tags: [concept, principle, knowledge-base]
sources: [llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# Persistent Compounding Artifact

[[LLM Wiki Pattern]] 中 wiki 的核心特征——一个持久的、复利式的产物。

## 含义

wiki 不是一个临时查询结果，而是一个**随着时间不断增值**的持久化资产：
- 交叉引用已建好
- 矛盾已被标记
- 综合分析已反映所有已读内容
- 每添加一个新素材，wiki 都变得更丰富

## 与传统 RAG 的对比

参见 [[RAG vs Wiki]]。在 RAG 中，查询结束后知识就"消失"了——下次问类似问题，LLM 要重新检索和拼接。而在 LLM Wiki 中，好的查询答案可以被**归档回 wiki** 作为新页面（比较、分析、发现的关联），这样探索成果和摄入的素材一样会复利积累。

## 为什么可行

维护知识库最繁琐的部分不是阅读和思考，而是维护交叉引用和一致性。人类放弃 wiki 是因为维护成本的增长快于价值增长。LLM 不会厌倦、不会忘记、一次可以处理 15 个文件，使得维护成本接近为零。
