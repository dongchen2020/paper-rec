---
name: paper-rec
description: Search for and recommend academic papers using current web sources, query rewriting, lightweight ranking, and structured summaries. Use when the user asks for literature search, related work, recent papers, survey seeds, arXiv recommendations, conference papers, implementation-linked papers, or Chinese requests such as 论文推荐、论文检索、相关工作、找最新论文、找顶会论文.
---

# Paper Recommendation

Use this skill when the user wants papers rather than a general explanation.

## Workflow

### 1. Detect the retrieval brief

Extract the minimum retrieval brief before searching:

- topic or research question
- subfield or application domain
- constraints such as year range, venue, method family, benchmark, code availability, or language

If the request is broad, rewrite it into `2-4` search queries:

- `broad` for recall
- `specific` for method-task alignment
- `recent` if the user wants latest work
- `implementation` if code or reproducibility matters

If the user writes in Chinese, you may answer in Chinese, but still search with English terms for international sources.

### 2. Search current primary sources

This skill depends on current information. Always browse the web for retrieval.

Prioritize primary or near-primary sources:

- arXiv
- official conference proceedings or OpenReview
- ACL Anthology / CVF Open Access / PMLR
- Papers With Code
- Semantic Scholar or DBLP for metadata cross-checking
- GitHub only as implementation evidence, not as the paper authority

Read [references/sources-and-ranking.md](references/sources-and-ranking.md) when you need source choices, venue examples, or ranking heuristics.

### 3. Filter and rank

Deduplicate by title, arXiv ID, DOI, or canonical URL.

Score candidates with lightweight judgment on:

- `similarity`: how directly the paper matches the user's topic
- `relevance`: whether the task, method, and setting align
- `importance`: venue quality, recency, citations or traction, and code availability

Do not fabricate citation counts, benchmark numbers, venue status, or code availability.

### 4. Produce a practical report

Default output:

1. `Query summary`
2. `Search strategy`
3. `Top recommendations`
4. `Gaps or cautions`

For each recommended paper, include:

- title
- year
- venue or source
- one short reason it matters here
- link

If the user asks for depth, add:

- core idea
- strengths
- weaknesses or boundary
- whether code or benchmark artifacts are available

Keep each paper summary short. A recommendation report is more useful than a long mini-survey.

### 5. Match report style to the user

- If the user asks for `latest`, prioritize very recent papers and state exact years.
- If the user asks for `classic` or `seminal`, allow older foundational papers.
- If the user asks for `top conference`, weight venue quality more heavily.
- If the user asks for `with code`, explicitly separate papers with official or clear public implementations from papers without them.
- If the user asks for `related work`, group papers by approach rather than by score alone.

## Quality bar

- Prefer primary sources over blog summaries.
- State uncertainty when metadata conflict across sources.
- Clearly mark preprints versus peer-reviewed papers.
- Do not pretend a fast search is exhaustive.
- If the query is underspecified and materially ambiguous, ask one short clarifying question. Otherwise, make a reasonable assumption and continue.
