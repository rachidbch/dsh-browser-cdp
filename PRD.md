# PRD

Local fork of `dsh-browser-cdp` (upstream: drscrewdriver), pinned at v1.2.2.

## Why we forked

Give the agent a stealth-capable browser it can drive, sharing one Chromium with the human's sidebar view.

## Scope of our divergence

- Tool descriptions must name the capability in words, not abbreviations (`bcdp_js` -> state it evaluates page JS).
- `bcdp_help` must explain sealing, the failure mode it causes, and the remedy.
- Nothing else. API, behaviour, and tool names stay upstream's.

## Non-goals

- Renaming `bcdp_*` tools (breaks scripts, forks the docs).
- Rewriting tiering logic.
