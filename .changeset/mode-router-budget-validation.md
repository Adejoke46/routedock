---
"@routedock/routedock": patch
---

Reject a malformed `budget_per_request` with `RouteDockPolicyRejectError('invalid_budget_per_request')` instead of treating it as no ceiling, and compare the ceiling against mode prices as integer stroops rather than floats. A value like `'abc'` previously parsed to `NaN`, which read as an unlimited budget, so `optimize: 'cost'` ignored the caller's cap and could select the cheapest mode at any price.
