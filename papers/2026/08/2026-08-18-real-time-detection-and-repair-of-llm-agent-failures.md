---
title: "Real-Time Detection and Repair of LLM Agent Failures"
authors: ["Sunny Dubey"]
date: 2026-08-18
arxiv_id: "2608.02464"
url: "http://arxiv.org/abs/2608.02464v1"
score: 0.80
topics: [agentic RL, LLM agent, tool use, agentic evaluation]
status: unread
---

# Real-Time Detection and Repair of LLM Agent Failures

## Summary

The paper proposes a two-layer runtime failure detection system: a one-class echo-state-network ensemble with CUSUM alarms trained on healthy runs detects 71% of failures at 5% false-alarm budget (AUROC 0.872, ~200μs/step), followed by deterministic verification that catches 96% of failures at zero false positives by recomputing stated totals from actual tool results. Repair via rollback-and-rerun recovers 45% of flagged failures, lifting task success from 52% to 73% for approximately one extra model call. The detection advantage over a memoryless baseline is a monotone function of post-onset horizon, confirming that early failure onset creates an exploitable temporal signal.

## Key Contributions

- Echo-state-network ensemble with CUSUM: trains only on healthy runs, runs at ~200μs/step, achieves AUROC 0.872 across 2,823 episodes and four model families
- Deterministic verification layer: recomputes stated totals from actual tool results, catches 96% of failures at 0 false positives (no retraining needed across models)
- Rollback-and-repair: 45% failure recovery, +21pp task success rate for ~1 extra model call per flagged run
- Transfer without retraining: AUROC 0.745/0.779 on external AFTraj-2K and ATBench corpora

## Relevance

This paper closes Gap #24 (real-time shortcut onset detection). The gap asked whether failure onset can be detected before trajectory completion, and specifically whether the detection can be done cheaply without a per-step LLM judge. The echo-state-network monitor answers both: it detects onset in real time at microsecond cost, and its advantage is a monotone function of post-onset horizon (the earlier the detection relative to episode end, the larger the gain), confirming that failure onset propagates a detectable temporal signal across steps — the exact property Gap #24 hypothesised.

## My Thoughts

<!-- Add your own notes here -->
