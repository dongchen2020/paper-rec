# paper-rec

English | [中文说明](#中文说明)

`paper-rec` is a Codex skill for academic paper search and recommendation. It turns a natural-language research question into a structured list of relevant papers. It is useful for related-work discovery, recent-paper search, top-conference filtering, and finding papers with public implementations.

## What It Does

- Recommends papers for a research topic
- Finds recent work within a given year range
- Filters papers by venue, domain, or method family
- Distinguishes peer-reviewed papers from preprints
- Highlights whether code, models, or benchmark artifacts are available

## How It Works

The skill first extracts the retrieval goal from the user request, then rewrites it into search-friendly queries, and finally searches, deduplicates, filters, and ranks papers from current web sources.

It prioritizes relatively authoritative sources such as:

- arXiv
- OpenReview
- PMLR
- ACL Anthology
- CVF Open Access
- Papers With Code
- Semantic Scholar
- DBLP

## Output

The default output usually includes:

- Query summary
- Search strategy
- Top recommendations
- Gaps, cautions, or follow-up notes

Each recommended paper may include:

- Title
- Year
- Venue or source
- Why it matters
- Link
- Core idea, strengths, weaknesses, and code availability when needed

## Example Requests

- Find representative papers on multimodal alignment since 2025.
- Recommend time-series anomaly detection papers with public code.
- Build a paper list for the related work section of an APT detection study.

## Notes

- This is a Codex skill, not a standalone application.
- It relies on live web retrieval, especially for recent-paper requests.
- It does not fabricate citation counts, benchmark numbers, venue status, or code availability.

---

## 中文说明

`paper-rec` 是一个面向 Codex 的论文检索与推荐 skill，用于把自然语言研究问题转化为结构化的论文推荐结果。它适合用在找相关工作、找最新论文、找顶会论文、找带代码论文，或快速建立某个方向的阅读清单。

## 功能说明

- 根据研究主题推荐相关论文
- 检索近两年或指定时间范围内的最新工作
- 按顶会、领域或方法路线筛选论文
- 区分正式发表论文与预印本
- 标出是否有公开代码、模型或基准链接

## 工作方式

这个 skill 会先从用户问题中提炼检索目标，再生成更适合检索的查询表达，然后基于当前网页来源进行论文搜索、去重、筛选和排序。

它优先参考以下较权威来源：

- arXiv
- OpenReview
- PMLR
- ACL Anthology
- CVF Open Access
- Papers With Code
- Semantic Scholar
- DBLP

## 输出内容

默认输出通常包括：

- 检索主题摘要
- 检索策略
- 重点推荐论文
- 风险、缺口或补充说明

每篇推荐论文可包含：

- 题目
- 年份
- 来源
- 推荐理由
- 链接
- 在需要时补充核心思想、优点、局限和代码可用性

## 使用示例

- 帮我找 2025 年以来多模态对齐的代表论文
- 给我推荐带代码的时间序列异常检测论文
- 整理一份适合写 APT 检测 related work 的论文清单

## 说明

- 这是一个 Codex skill，不是独立应用程序。
- 它依赖实时网页检索，尤其适用于“最新论文”类请求。
- 它不会编造引用数、基准结果、会议级别或代码可用性。
