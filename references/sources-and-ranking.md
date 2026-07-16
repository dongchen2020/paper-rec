# Sources And Ranking

Use this file when the request needs more explicit source selection or stronger ranking judgment.

## Primary sources

- `arXiv`: fastest source for new ML and AI papers
- `OpenReview`: ICLR and some workshop or review metadata
- `PMLR`: ICML, AISTATS, CoLT and related proceedings
- `ACL Anthology`: ACL, EMNLP, NAACL, COLING and related NLP venues
- `CVF Open Access`: CVPR, ICCV, ECCV
- `Papers With Code`: tasks, benchmarks, linked implementations
- `Semantic Scholar`: metadata, citations, related papers
- `DBLP`: clean computer science bibliography

## Venue heuristics

Use venue status as one signal, not the whole answer.

- `Tier 1`: NeurIPS, ICML, ICLR, CVPR, ICCV, ACL, AAAI, KDD, SIGIR
- `Tier 2`: EMNLP, NAACL, ECCV, COLING, WSDM, CIKM, BMVC
- `Preprint`: arXiv without peer-reviewed venue

If the user asks for Chinese academic grading norms, CCF-style venue framing is reasonable, but do not force it when the user did not ask.

## Ranking heuristics

Prioritize:

- direct task match
- method relevance
- recency when the user asks for latest work
- venue quality
- code, model, or dataset availability

Possible warning flags:

- only secondary summaries available
- missing paper PDF or unclear authorship
- benchmark claims repeated on GitHub but not traceable to the paper
- title match but wrong task setting

## Reporting rules

- Mark `preprint` versus `peer-reviewed` explicitly.
- Give exact year, and month if the source makes it easy.
- Provide links for every recommended paper.
- If multiple variants of the same work exist, prefer the most authoritative public version.
