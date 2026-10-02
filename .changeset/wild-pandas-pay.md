---
'@routedock/routedock': patch
---

A 200 manifest response with a non-JSON body now rejects with a non-retryable `RouteDockManifestError`. A malformed 402 `X-Payment-Requirements` header now rejects with `RouteDockManifestError` carrying the decode error as `cause`. `ProviderRegistry` filters Supabase providers by its configured network.
