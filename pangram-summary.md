# Summary for Pangram — AI-generated text in U.S. public comments

Hi Pangram team — final summary of the research your $5,000 credit funded. Everything below is reproducible from public data.

## What I did
I searched all 3,235 U.S. counties and county-equivalents for obtainable public-comment corpora. 1,883 counties (58%) publish them; 1,352 publish nothing machine-readable. Every scoreable verbatim comment was scored whole with Pangram 4 (one comment = one row, one chunk — Pangram windows never split a comment). An LLM proposed comment boundaries in each PDF and a machine verifier rejected any non-verbatim text before scoring.

## Headline results
- County/local comments: 3,565 comments scored across 221 studies — 141 AI, 61 Mixed, 3,363 Human = 5.7% flagged AI+Mixed. 14,887 comment rows stored in a public dataset.
- Federal (SEC): 625 comments, 1.1% flagged.
- Peer review (ICLR): 0% flagged before ChatGPT vs 15.8% after (369 reviews).
- Laws (new): 141 enacted federal public laws scored whole — 0 AI, 1 Mixed.
- arXiv: 12-paper pilot (7 Human, 4 Mixed, 1 AI).

Full report and per-study table: https://github.com/aminamos/public-comment-ai-study
Study page: https://minntelligence.fyi/research/public-comment-ai-2026/
Data: Cloudflare D1 + R2, every score linked to its verbatim comment and source document.

Caveat I use everywhere: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output.

## Credits
Internal ledger spend to date is about $1,006 (county $581, federal $174, peer review $95, arXiv $86, laws $71). Last dashboard balance was $4,251.83; I estimate roughly $4,160 in credit remains.

## Ideas for a next round, if you want to fund more
- Expand arXiv from the 12-paper pilot to n=300 whole papers (about $2,148).
- Federal expansion beyond SEC dockets (about $750).
- China arXiv / non-English corpora, to test whether the U.S. pattern generalizes across languages.
- Wikipedia Articles for Creation, international consultations (UK/EU/CA/AU/NZ), NGO reports, and state-legislature testimony — each is collected-but-unscored backlog so far; $50 pilots for Wikipedia and NGO reports are allocated next.
- Laws, phase 2: one enacted ordinance per county/city nationwide (about $1,400).

Full program estimate: about $13,100.

My workflow/harness is muse-wonder-1.0 (not Muse Wonder Full). If you or Meta want to partner on a larger run, I am open to that as well.

Thank you for the research credit — it turned a one-city pilot into a national dataset.

— Amin Amos, minntelligence.fyi
