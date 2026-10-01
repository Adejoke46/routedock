---
'@routedock/routedock': patch
---

Trustline onboarding and trustline remediation now share one source of truth for USDC issuers. `USDC_ISSUERS` is exported from `internal/usdc.ts` and the client's preflight reads it instead of keeping a second copy, so the `change-trust` command inside a `RouteDockTrustlineError` can no longer drift from the issuer the client actually accepts. The `agent-to-agent`, `inference-agent` and `price-oracle-agent` READMEs now include the missing trustline step (and Circle's testnet faucet) that the payment paths require before the first run.
