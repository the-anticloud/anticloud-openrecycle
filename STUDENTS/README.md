# Students — OPENRECYCLE

**Project:** OPENRECYCLE  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `158f04567ac927d7ecfbf150480ced2e39978143`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `a3a66de5ebf4adde507890bf612c9154c270d7a166274dc94bf2368bda46749e`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `158f04567ac927d7ecfbf150480ced2e39978143`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `a3a66de5ebf4adde507890bf612c9154c270d7a166274dc94bf2368bda46749e`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
