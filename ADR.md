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

## ADR-003: This stack is not a stealth stack
Status: accepted (2026-10-18)
Context: Measured with CreepJS: 50% like headless, `stealth: 0%`, renderer string names SwiftShader, timezone UTC while the human is in Africa/Tunis. Naive checks (webdriver, UA, Chrome object, plugin array, WebGL presence) all pass.
Decision: Do not chase fingerprint evasion here. Take only changes that cannot trade one signal for another or break function. Stealth is delegated to Camoufox, tracked in ROADMAP.md under the human's ownership.
Consequences: This browser is fit for ordinary automation and for sites that only grep for headless markers. A bot-resistant site is expected to challenge it, and that is Camoufox's job. Spoofing the renderer string is explicitly rejected: `stealth` counters exist to catch patches, so patching raises the score instead of lowering it.
