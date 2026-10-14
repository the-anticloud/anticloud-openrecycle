# Educators — OPENRECYCLE

**Project:** OPENRECYCLE  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `158f04567ac927d7ecfbf150480ced2e39978143`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `a3a66de5ebf4adde507890bf612c9154c270d7a166274dc94bf2368bda46749e`  
**Date:** October 2026

## Teaching with OPENRECYCLE

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `a3a66de5ebf4adde507890bf612c9154c270d7a166274dc94bf2368bda46749e` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
