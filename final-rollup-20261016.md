# Final rollup — AI-generated text in U.S. public comments (2026-10-16)

Caveat: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output.

## Coverage
- All 3,235 counties/county-equivalents searched (100% search coverage).
- 1,883 (58%) publish obtainable public-comment corpora; 1,352 publish nothing machine-readable.
- Every scoreable verbatim comment in the obtained corpora was scored whole (one comment = one row, one Pangram chunk), or the document was documented as containing no separable verbatim comments / unverifiable after two attempts.

## County closeout (233 set-aside documents re-attempted)
| Outcome | n |
|---|---|
| Scored and synced (incl. resync from saved results, no rescoring) | 35 |
| Verified zero separable verbatim comments | 92 |
| Unverifiable after two attempts | 106 |

## Scored results (D1 `minntelligence-research-db`, R2 `minntelligence-research`)
| Track | Scored | AI | Mixed | Human | Flagged (AI+Mixed) |
|---|---|---|---|---|---|
| County/local comments | 3,565 comments (221 studies) | 141 | 61 | 3,363 | 5.7% |
| County whole-document scans | 58 documents | — | — | — | doc-level only |
| Federal (SEC) | 625 comments | 5 | 2 | 618 | 1.1% |
| Peer review (ICLR) | 369 reviews | — | 29 post-ChatGPT vs 0 pre | — | 0% pre → 15.8% post |
| arXiv pilot | 12 papers | 1 | 4 | 7 | pilot only |

14,887 county comment rows are stored (scored + too-short/unscored), each linked to its study, source, and raw Pangram JSON in R2.

## Spend and remaining credits
Internal ledger: county $580.65 / $2,300; federal $174.00; peer review $94.90 / $100; arXiv $85.90 / $100; laws $0 / $500 reserved. Total ledger spend $935.45. Last dashboard balance $4,251.83; estimated remaining ~$4,230.

## Method limits
Verbatim extraction only; an LLM proposes boundaries and a machine verifier rejects non-verbatim text. Staff summaries, form letters, OCR error, the >=50-word floor, and obtainable-corpus bias (urban/PDF-publishing bodies) all limit inference. Flagged != AI-written.
