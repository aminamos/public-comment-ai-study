# SovietRxiv scan — 2026-10-17 ($20 pilot)

Via the unified ChinaRxiv/SovietRxiv API (`source=russiarxiv`): translated
Soviet-era scientific papers, full text.

## Method

- Frame: first 400 listing entries with full text (listing runs oldest-first;
  the frame is 1976–1977 papers). Seed-42 shuffle, fit-to-cap selection.
- 26 papers scored whole, one paper = one row (`pangram-4` bulk).
- Spend: $18.85 of $20 cap (377 units). Cap funded by $20 reallocation from
  chinarxiv-scan.

## Result (n=26, all 1976–1977)

25 Human, 1 Mixed, 0 AI → 3.8% AI+Mixed.

## Interpretation

These are pre-AI-era texts in machine translation — a false-positive
baseline. The near-zero flag rate says translation alone does not explain
ChinaXiv's 88.7% AI+Mixed (53 papers, 2026): the same translation pipeline
scores 1970s Soviet technical prose as almost entirely Human. Caveats:
small n, one era (1976–77), technical subject matter, and the two corpora
differ in field and writing conventions, not only in date.

Data: D1 `sovietrxiv_papers` (26 rows), R2 `sovietrxiv-scan/<paper_id>/paper.txt`,
registry `registry/papers.csv`.
