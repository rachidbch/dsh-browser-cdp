# Tool surface notes

38 tools, four tiers; only `core` is resident under `toolInjection: lazy`.

- core: status, doctor, help, space_open, navigate, snapshot
- browse: click, fill, key, hover, scroll, select, check, screenshot, page_info, read_element, js, wait, wait_for_selector
- extended: drag, upload, download, dialog, cdp, http, cli, script, captcha, auth_flush, login_import, wait_for_url, wait_for_response
- judge: jev_*

Sealed tools disappear from the list (deregistered, not erroring). Any browser activity re-opens them; `bcdp_status` and `bcdp_doctor` count.

Overlapping names: `js` (eval expr), `cdp` (raw CDP), `cli` and `script` (same heredoc runtime, different envelope), `http` (fetch, browser or server context).
