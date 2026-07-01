# Leo Daily

> 个人日常记录知识库，基于 LLM Wiki 模式构建，由 AI 持续维护。

## 构建工具

### LLM Wiki Pattern

本知识库采用 [LLM Wiki Pattern](https://gist.github.com/karpathy/442a6bf5559148931c11519de94f)（由 Andrej Karpathy 提出）构建。核心理念：**LLM 充当图书管理员，用户充当策展人**。知识被增量编译到持久 wiki 中，而非每次查询时重新检索——区别于传统 RAG 的"查完即忘"，wiki 是一个持续增值的复利式产物。

### Second Brain

具体实现使用 [Second Brain](https://github.com/NicholasSpisak/second-brain)（由 Nicholas Spisak 开发），提供完整的工具链：

| Skill | 功能 | 触发命令 |
| --- | --- | --- |
| Onboarding | 初始化知识库（目录结构、配置） | `/second-brain` |
| Ingest | 将原始素材编译为 wiki 页面 | `/second-brain-ingest` |
| Query | 搜索 wiki 并综合回答问题 | `/second-brain-query` |
| Lint | 健康检查（矛盾、孤立页、缺失引用） | `/second-brain-lint` |

### AI Agent

- **Claude Code** — 作为主要的 AI agent，通过 `CLAUDE.md` 配置文件定义 wiki 的结构和行为规则
- 支持 MCP Protocol 扩展（如 [Chrome DevTools MCP](https://github.com/ChromeDevTools/chrome-devtools-mcp) 进行浏览器自动化）

### 浏览与编辑

- **[Obsidian](https://obsidian.md/)** — 作为 wiki 的浏览界面，支持 `[[wikilink]]` 语法、图视图、Dataview 插件
- **Obsidian Web Clipper** — 浏览器扩展，将网页文章保存为 markdown 到 `raw/` 目录

## 目录结构

```
leo-daily/
├── raw/                    # 原始素材（只读，不可修改）
│   └── assets/             # 图片和附件
├── wiki/                   # AI 维护的 wiki
│   ├── sources/            # 每个素材的摘要页
│   ├── entities/           # 人物、组织、产品、工具
│   ├── concepts/           # 概念、框架、理论
│   ├── synthesis/          # 比较、分析、主题
│   ├── index.md            # 主目录（所有 wiki 页面的索引）
│   └── log.md              # 操作日志（按时间记录）
├── output/                 # 查询结果、报告等生成物
├── CLAUDE.md               # Claude Code agent 配置（wiki 规则）
└── README.md               # 本文件
```

## 核心概念

### 三层架构

知识库分为三层：

1. **Raw（原始素材层）** — 不可变的源文档，是真相的来源
2. **Wiki（wiki 层）** — LLM 维护的结构化知识，包含摘要、实体页、概念页、综合分析
3. **Schema（规则层）** — 定义 wiki 结构、约定和工作流程的配置文档（`CLAUDE.md`）

### 主要操作

- **Ingest（摄入）** — 将新素材编译到 wiki，更新相关实体和概念页，单个素材通常影响 10-15 个 wiki 页面
- **Query（查询）** — 基于 wiki 回答问题，好的答案可归档回 wiki 作为新页面继续积累
- **Lint（健康检查）** — 定期检查矛盾、过时内容、孤立页面、缺失引用，建议每 10 次摄入或每月运行一次

## 使用方式

### 日常流程

1. 用 **Obsidian Web Clipper** 将感兴趣的文章保存到 `raw/`
2. 在 Claude Code 中运行 `/second-brain-ingest`，AI 会讨论关键要点并创建 wiki 页面
3. 随时运行 `/second-brain-query` 向知识库提问
4. 定期运行 `/second-brain-lint` 保持 wiki 健康

### 关键原则

- `raw/` 中的文件是**不可变**的——AI 只读取，从不修改
- 每个素材都会提取实体和概念，创建或更新对应的 wiki 页面
- 所有内部引用使用 `[[wikilink]]` 语法，便于在 Obsidian 中浏览
- 知识随时间**复利积累**——每次摄入都让 wiki 更丰富
