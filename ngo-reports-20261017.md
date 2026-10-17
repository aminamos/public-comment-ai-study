# NGO reports (2026-10-17)

Caveat: AI detection is probabilistic, not proof; a flag means the text statistically resembles AI output. Whole-report flags on templated institutional writing measure template resemblance as much as authorship.

Sample: 11 public reports (2023-2024) from MSF (3), UNICEF (4), ICRC, IRC UK, Save the Children, WHO, downloaded as PDFs, extracted verbatim with pdftotext, one report = one row scored whole (Pangram bulk, pangram-4). Word counts 2,260-42,084.

Results: 11 of 11 Human, 0 AI, 0 Mixed. Highest fraction_ai was 0.024 (MSF India; WHO Results Report 0.023). Data in D1 `ngo_reports` and R2 `ngo-reports/<report_id>/`. Spend $73.80 / $500 cap; the binding constraint was report availability in directly downloadable PDF form (ReliefWeb's API requires an approved appname), not credits.

## Extension (2026-10-17)
Added 7 reports (UNICEF Uganda, Algeria, Core Resources, GRASSP Angola; WHO A79_8, A79_16, A79_18), scored whole for $61.30. Combined NGO totals (D1 `ngo_reports`, n=18): Human 17, Mixed 1, AI 0. The Mixed report is WHO A79_16 (health emergencies results, fraction_ai 0.269); next-highest fraction_ai is 0.052 (UNICEF Core Resources). Total NGO spend $135.10 / $500 cap; remaining cap is availability-bound (directly downloadable PDFs), not credit-bound.
