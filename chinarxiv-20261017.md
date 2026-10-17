# ChinaXiv (2026-10-17) — download subsystem in maintenance, 0 scored

Caveat: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output.

Enumeration succeeded: 55 valid ChinaXiv papers identified for 2026 Q2 (IDs validated by the presence of a PDF download link on each abstract page; registry in `registry/listing-2026q2.txt`).

Retry after cooldown (2026-10-17): this host still receives HTTP 403 for chinaxiv.org. Two alternate network paths were tried: the DigitalOcean droplet and the Windows machine were both unreachable by SSH, and a temporary Cloudflare Worker fetch proxy (created for this retry, deleted afterward) could load abstract pages but every PDF view/download request returned HTTP 403 with a page stating 系统正在维护中 ("system under maintenance"). Scoring abstracts instead would break the whole-paper rule, so no papers were scored and no workaround was forced. Abstract-only scoring was rejected.

Scored: 0 papers. Spend $0 / $500 cap (budget check not reached; no paid submission made). The 55-ID list is saved so collection can resume directly at download once the ChinaXiv download subsystem is back.
