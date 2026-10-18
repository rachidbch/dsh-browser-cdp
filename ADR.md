# ADR

## ADR-001: Fork at the release tag, not HEAD
Status: accepted (2026-10-18)
Context: The registry serves 1.2.2; upstream HEAD is 0.18.19 and drifts.
Decision: Clone `v1.2.2` and diverge from it.
Consequences: Our patches apply to exactly what runs. Upstream upgrades arrive via `git fetch upstream --tags` and a rebase of our few description commits.

## ADR-002: Patch descriptions only, never tool names
Status: accepted (2026-10-18)
Context: Names are abbreviated (`bcdp_js`), but renaming breaks scripts and the upstream docs.
Decision: Fix the description text; keep every tool name.
Consequences: Discoverability improves without a migration. The naming complaint goes upstream instead.
