---
title: "When All Rollouts Fail: Policy-Compatible Joint Decoding for Hard-Problem Reasoning"
authors: ["Zehao Wang", "Hanzhu Chen", "Runquan Gui", "Zhe Wang", "Lin Yang"]
date: 2026-10-27
arxiv_id: "2610.36849v1"
url: "https://arxiv.org/abs/2610.36849"
score: 0.84
topics: [agentic RL, RL training, GRPO, RLVR, LLM agent]
status: unread
---

# When All Rollouts Fail: Policy-Compatible Joint Decoding for Hard-Problem Reasoning

## Summary

PICO addresses the zero-advantage collapse in GRPO/RLOO when all rollouts on hard problems fail: standard group-relative estimators produce zero gradient, leaving hard problems invisible to learning. It performs distribution-constrained joint decoding where expert data guides token-level sampling while preserving the student's relative token probabilities, with a dynamic top-k mechanism enforcing a finite divergence budget — yielding trajectories that are both correct and policy-compatible. These are optimized jointly with on-policy rollouts under a mixed-behavior objective with importance sampling, consistently outperforming standard RLVR and off-policy baselines on reasoning and agentic benchmarks.

## Key Contributions

- Diagnoses the zero-advantage collapse problem: when all rollouts fail, group-relative estimators produce no gradient signal, stalling learning on hard problems
- Distribution-constrained joint decoding: expert data guides token-level probabilities while a dynamic top-k mechanism enforces a KL divergence budget, ensuring policy-compatible expert trajectories
- Mixed-behavior objective with importance sampling corrects for distribution mismatch between joint-decoded and on-policy trajectories
- Consistent gains over standard RLVR and prior off-policy injection baselines across reasoning benchmarks and agentic tasks

## Relevance

Directly complements BRAT (multi-pass RLVR fragility) and the GRPO training dynamics thread: BRAT fixes the instability of reusing data across passes, while PICO fixes the zero-signal problem on the hardest problems within a single pass. Both address fundamental failure modes of the GRPO learning signal from different angles. The policy-compatibility framing is also closely related to the adaptive scaffolding cluster (AutoScaffold, Scaf-GRPO) — all three are addressing "how do you inject external information into GRPO without breaking it?"

## My Thoughts

<!-- Add your own notes here -->
