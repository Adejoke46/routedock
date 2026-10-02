---
"@routedock/mcp-server": patch
---

`stream_session` now returns the messages it already paid for when a later voucher in the batch fails (local spend cap reached, provider 4xx/5xx) instead of replacing the whole result with a bare error, and reports `count` and `stats` alongside them. `max_messages` is bounded to an integer from 1 to 50, and the per-call stream generator is closed so it does not linger between calls.
