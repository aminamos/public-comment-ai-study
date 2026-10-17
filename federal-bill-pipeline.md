# Federal bill pipeline (daily, Cloudflare)

Worker: `federal-bill-pipeline` — https://federal-bill-pipeline.a-8c6.workers.dev
Cron: `0 13 * * *` UTC (daily).

## What it does

1. Fetches GovInfo's current-year BILLS sitemap
   (`/sitemap/BILLS_<year>_sitemap.xml`), newest packages first.
2. Skips packages already in D1 `federal_bills`.
3. Fetches each bill's HTML text from GovInfo, strips tags mechanically.
4. Scores each whole bill (one bill = one row) via Pangram bulk `pangram-4`.
5. Stores text in R2 `federal-bills/<pkg>/bill.txt`, score row in D1
   `federal_bills`, and a run log in D1 `pipeline_runs`.

## Guards (wrangler vars)

- `RUN_LIMIT=5` bills/day (manual `/run?limit=` max 10)
- `MIN_WORDS=50`, `MAX_WORDS=15000` (outside → logged as skipped, unscored)
- `DAILY_UNIT_CAP=400` units ≈ $20/day max at $0.05/unit

## Endpoints

- `GET /` health
- `GET /run?limit=2` manual run
- `GET /recent` latest 50 rows

Secret: `PANGRAM_API_KEY` (Worker secret, set 2026-10-17).
Verified live 2026-10-17: 2 newest bills scored (both Human), D1+R2 confirmed.
Ongoing spend draws on the Pangram account balance; it is not in the
`budgets.json` caps (test run $0.55 was recorded under laws-scan).
