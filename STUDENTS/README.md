# Students — TRANSFORMERS

**Project:** TRANSFORMERS  
**Category:** PHILOSOPHY_SEMANTICS  
**Upstream:** https://github.com/huggingface/transformers  
**Pinned commit:** `35924ec379eec682bbdca219886e16eff4df8b09`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ed2cb72c2d3cd3594b4b154596cddb722c15aa3e85a7c317877f4e56dcded59c`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `35924ec379eec682bbdca219886e16eff4df8b09`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `ed2cb72c2d3cd3594b4b154596cddb722c15aa3e85a7c317877f4e56dcded59c`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
