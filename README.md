# AI-Generated Text in U.S. Public Comments

National measurement of AI-flagged text in U.S. government public comments, using Pangram 4.

Caveat: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output.

## Contents
- `final-rollup-20261016.md` — final report (coverage, closeout, scored results, spend, method limits)
- `per-study-table.csv` — per-study scored counts (AI / Mixed / Human, % flagged)
- `pangram-executive-summary.png` — one-page executive summary

## Data
Full comment-level data is in Cloudflare D1 (`minntelligence-research-db`) and R2 (`minntelligence-research`, one prefix per study), so every score links back to its verbatim comment and source document. Study page: https://minntelligence.fyi/research/public-comment-ai-2026/

Method: verbatim extraction only. An LLM proposes comment boundaries; a machine verifier rejects any non-verbatim text; each comment is scored whole as one Pangram chunk (one comment = one row). Documents with no separable verbatim comments are documented, not guessed.

Workflow harness: muse-wonder-1.0 (Meta models). Funded in part by a Pangram research credit; the vendor funded measurement of its own detector's flags.
