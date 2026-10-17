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

## Expansion (2026-10-17, after local-government corpora were exhausted)
Dashboard at expansion start: $1,023.05 spent, $4,165.47 balance.
- Laws (cap raised to $1,200): 256 federal public laws total scored whole — 255 Human, 1 Mixed, 0 AI. Spend $1,118.05. Two over-cap omnibus laws deferred; ordinance slice still collection-bound.
- arXiv (cap $2,250): expanded to n=300 whole papers — Human 158, Mixed 133, AI 9 (47.3% flagged, mostly Mixed). Spend $2,001.05 total.
- Peer review (cap $600): 2,269 ICLR reviews total — pre-ChatGPT 0/1,135 flagged (0.0%), post-ChatGPT 142/1,134 flagged (12.5%). Spend $572.65.
- Wikipedia AfC ($500): 3,330 Draft-namespace drafts scored (3,271 with prediction) — AI 620, Mixed 405, Human 2,246 (31.3% flagged; highest of any track). Most AfC drafts are under the 50-word floor and stored unscored. Spend $477.90.
- NGO reports ($500): 11 reports (MSF, UNICEF, ICRC, IRC, Save the Children, WHO) scored whole — 11/11 Human, max fraction_ai 0.024. Spend $73.80 (availability-bound, not credit-bound).
- ChinaXiv ($500): 55 valid 2026-Q2 papers enumerated; host then returned 403 for all requests from this host. 0 scored, $0 spent; ID list saved for a later retry.
Estimated remaining Pangram credit after expansion: ~$170 (dashboard balance minus expansion spend).
