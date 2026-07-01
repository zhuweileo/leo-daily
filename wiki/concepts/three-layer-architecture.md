---
tags: [concept, architecture, design]
sources: [NicholasSpisaksecond-brain LLM-maintained personal knowledge base for Obsidian. Based on Andrej Karpathy's LLM Wiki pattern..md, llm-wiki.md]
created: 2026-07-01
updated: 2026-07-01
---

# Three-layer Architecture

[[LLM Wiki Pattern]] 的三层架构设计。

## 三层结构

1. **Raw Sources（原始素材层）** — 用户策展的原始文档集合（文章、论文、笔记、转录等）。**不可变**——LLM 只读取，从不修改。这是真相的来源。

2. **Wiki（wiki 层）** — LLM 生成的 markdown 文件目录，包含摘要、实体页、概念页、综合分析、概览。LLM 完全拥有这一层——创建页面、在素材到来时更新、维护交叉引用。用户阅读，LLM 编写。

3. **Schema（规则层）** — 配置文档（如 [[Claude Code]] 的 `CLAUDE.md`），告诉 LLM wiki 的结构、约定和工作流程。这是让 LLM 成为有纪律的 wiki 维护者（而非通用聊天机器人）的关键配置。用户和 LLM 随时间共同演进此配置。

## 目录结构

```
vault/
├── raw/                    # 原始素材（不可变）
│   └── assets/             # 图片和附件
├── wiki/                   # LLM 维护的 wiki
│   ├── sources/            # 每个素材的摘要页
│   ├── entities/           # 人物、组织、产品、工具
│   ├── concepts/           # 概念、框架、理论
│   ├── synthesis/          # 比较、分析、主题
│   ├── index.md            # 主目录
│   └── log.md              # 操作日志
└── output/                 # 报告和生成物
```
