# Ethics — TRANSFORMERS

**Project:** TRANSFORMERS  
**Category:** PHILOSOPHY_SEMANTICS  
**Upstream:** https://github.com/huggingface/transformers  
**Pinned commit:** `35924ec379eec682bbdca219886e16eff4df8b09`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ed2cb72c2d3cd3594b4b154596cddb722c15aa3e85a7c317877f4e56dcded59c`  
**Date:** October 2026

## Position

TRANSFORMERS is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
