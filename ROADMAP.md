# ROADMAP

## Camoufox / MCP track

CDP is the wrong tool against bot-resistant sites: detection looks for the protocol itself, not only for headless tells. That is why a second, protocol-different path is planned.

- **Why Camoufox**: a Firefox fork with anti-fingerprinting in the C++ source, driven over Juggler/BiDi, so no CDP surface exists to detect.
- **Why it cannot join this stack**: no CDP endpoint, so `dsh-sidebar-cdp-browser`, `dsh-browser-cdp`, and the sidebar tab cannot drive or show it. It needs its own provider and its own tools.
- **Shape**: `dsh-browser-use` plus a Camoufox provider, or a stealth MCP server (Camoufox MCP / `invisible_playwright_mcp`). Separate tool namespace, no shared tab.
- **Open question**: whether a sidebar live view is achievable at all without CDP; today the honest answer is no, unless a bridge (e.g. `foxbridge`, CDP->BiDi) proves reliable.
- **Fallback already in place**: Chrome under Xvfb with `--disable-blink-features=AutomationControlled` and a real UA, which defeats the headless fingerprint but not CDP-aware detection.
