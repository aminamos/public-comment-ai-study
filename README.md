# AI-Generated Text in U.S. Public Comments

National measurement of AI-flagged text in U.S. government public comments, using Pangram 4.

Caveat: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output.

## Contents
- `final-rollup-20261016.md` — final report (coverage, closeout, scored results, spend, method limits)
- `per-study-table.csv` — per-study scored counts (AI / Mixed / Human, % flagged)
- `pangram-executive-summary.png` — one-page executive summary
- `chart-by-corpus.png` — share flagged AI+Mixed by Pangram 4, by corpus (all tracks)
- `chart-peer-review.png` — ICLR peer reviews flagged AI+Mixed, before vs after ChatGPT
- Companion-track reports: `chinarxiv-20261017.md`, `sovietrxiv-20261017.md` (1976–77 translated baseline, 3.8% of 26), `arxiv-expansion-20261017.md`, `peer-expansion-20261017.md`, `laws-phase1-20261016.md`, `mn-laws-20261017.md`, `ngo-reports-20261017.md`, `wikipedia-afc-20261017.md`, `federal-bill-pipeline.md`

## Data
Full comment-level data is in Cloudflare D1 (`minntelligence-research-db`) and R2 (`minntelligence-research`, one prefix per study), so every score links back to its verbatim comment and source document. Study page: https://minntelligence.fyi/research/public-comment-ai-2026/

Method: verbatim extraction only. An LLM proposes comment boundaries; a machine verifier rejects any non-verbatim text; each comment is scored whole as one Pangram chunk (one comment = one row). Documents with no separable verbatim comments are documented, not guessed.

Workflow harness: muse-wonder-1.0 (Meta models). Funded in part by a Pangram research credit; the vendor funded measurement of its own detector's flags.
