---
tags: [concept, operation, workflow]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# Lint Operation

[[LLM Wiki Pattern]] 中的健康检查操作——定期检查 wiki 的完整性和一致性。

## 检查项

1. 页面之间的矛盾
2. 被新素材取代的过时声明
3. 没有入链的孤立页面
4. 被提及但缺少独立页面的重要概念
5. 缺失的交叉引用
6. 可通过 web 搜索填补的数据缺口
7. 索引与实际页面的一致性

## 频率

- 每摄入 **10 篇素材** 后——趁交叉引用差距还新鲜时捕捉
- **每月至少一次**——捕捉随时间积累的过时声明和孤立页面
- **重大查询或综合分析之前**——确保依赖的 wiki 健康

## 在 Second Brain 中的实现

通过 `/second-brain-lint` slash command 触发。
