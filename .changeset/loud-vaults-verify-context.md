---
"@routedock/nulth-sdk": patch
"@routedock/routedock": patch
---

Nulth signers now decode the Soroban auth entry before signing and reject it with `NulthPolicyError` code `auth_entry_mismatch` unless it is a single `transfer` on `assetContract` from the Nulth account to `paymentContext.payee` for exactly `paymentContext.amountStroops`, with no sub-invocations. `assertAuthEntryMatchesContext` is exported from `@routedock/nulth-sdk`.
