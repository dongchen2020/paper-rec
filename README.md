# paper-rec

English | [中文说明](#中文说明)

`paper-rec` is a Codex skill for academic paper search and recommendation. It turns a natural-language research question into a structured list of relevant papers.

## What It Does

- Recommends papers for a research topic
- Finds recent work within a given year range
- Filters papers by venue, domain, or method family
- Distinguishes peer-reviewed papers from preprints
- Highlights whether code, models, or benchmark artifacts are available

## How It Works

The skill extracts the retrieval goal, rewrites it into search-friendly queries, then searches, deduplicates, filters, and ranks papers from current web sources.

It prioritizes sources such as:

- arXiv
- OpenReview
- PMLR
- ACL Anthology
- CVF Open Access
- Papers With Code
- Semantic Scholar
- DBLP

## Output

- Query summary
- Search strategy
- Top recommendations
- Gaps or cautions

## Notes

- This is a Codex skill, not a standalone application.
- It relies on live web retrieval.
- It does not fabricate citation counts, benchmark numbers, venue status, or code availability.

---

## 中文说明

`paper-rec` 是一个面向 Codex 的论文检索与推荐 skill，用于把自然语言研究问题转化为结构化的论文推荐结果。

## 功能

- 根据研究主题推荐相关论文
- 检索近两年或指定时间范围内的最新工作
- 按顶会、领域或方法路线筛选论文
- 区分正式发表论文与预印本
- 标出是否有公开代码、模型或基准链接

## 工作方式

这个 skill 会先提炼检索目标，再生成检索式，然后基于当前网页来源进行搜索、去重、筛选和排序。

优先参考：

- arXiv
- OpenReview
- PMLR
- ACL Anthology
- CVF Open Access
- Papers With Code
- Semantic Scholar
- DBLP

## 输出

- 检索主题摘要
- 检索策略
- 重点推荐论文
- 风险、缺口或补充说明

## 说明

- 这是 Codex skill，不是独立应用程序。
- 它依赖实时网页检索。
- 它不会编造引用数、基准结果、会议级别或代码可用性。
