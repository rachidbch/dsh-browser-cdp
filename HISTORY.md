# HISTORY

2026-10-18 — Fork created at v1.2.2; remotes set (origin ours, upstream OG). ADR-001, ADR-002.
2026-10-18 — `bcdp_script`/`bcdp_cli` no longer report failure when a script prints output without the `@@DSH_RESULT@@` sentinel; exit code is the authority. The parameter doc had invited plain `console.log`, which always failed the run.
