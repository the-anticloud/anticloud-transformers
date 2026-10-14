# Educators — TRANSFORMERS

**Project:** TRANSFORMERS  
**Category:** PHILOSOPHY_SEMANTICS  
**Upstream:** https://github.com/huggingface/transformers  
**Pinned commit:** `35924ec379eec682bbdca219886e16eff4df8b09`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ed2cb72c2d3cd3594b4b154596cddb722c15aa3e85a7c317877f4e56dcded59c`  
**Date:** October 2026

## Teaching with TRANSFORMERS

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `ed2cb72c2d3cd3594b4b154596cddb722c15aa3e85a7c317877f4e56dcded59c` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
