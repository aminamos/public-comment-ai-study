# ChinaXiv scan — 2026-10-17 (via ChinaRxiv API)

Original chinaxiv.org host returned 403 "system under maintenance" for all PDF
downloads (six checks). Completed via the ChinaRxiv public API
(`https://chinarxiv.org/api/v1`, `source=chinaxiv`), which serves the same
corpus with full text.

## Method

- IDs: the 55 valid 2026-Q2 ChinaXiv IDs saved in
  `registry/listing-2026q2.txt` (enumerated before the host block).
- Text: `GET /api/v1/papers/{id}/text` (`body_md`), markdown markers stripped
  mechanically. 53/55 had full text ≥50 words; 2 returned HTTP errors.
- One paper = one row, whole text as one Pangram chunk (`pangram-4` bulk).
- Spend: $208.05 of $500 cap (4,161 units at $0.05).

## Result (n=53)

| Prediction | n |
|---|---|
| Human | 6 |
| Mixed | 40 |
| AI | 7 |

AI+Mixed = 47/53 (88.7%).

## Critical caveat

ChinaRxiv texts are mostly **machine-translated** (Chinese → English;
`source_language: mixed`). Machine translation produces statistically regular
English, which plausibly inflates Mixed/AI-like scores. This number measures
the translated text as served, **not** the Chinese originals, and is not
comparable to the arXiv result (47.3% AI+Mixed, native English) without that
qualification. AI detection is probabilistic, not proof; a flag means the
text statistically resembles AI output.

Data: D1 `chinarxiv_papers` (53 rows), R2 `chinarxiv-scan/<paper_id>/paper.txt`,
registry `registry/papers.csv`.
