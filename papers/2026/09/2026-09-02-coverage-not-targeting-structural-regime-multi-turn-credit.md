---
title: "Coverage, Not Targeting: A Structural Regime in Multi-Turn Agent Credit Assignment"
authors: ["Chenyu Zhou", "Qiliang Jiang", "Shuning Wu", "Xu Zhou"]
date: 2026-09-02
arxiv_id: "2609.02417v1"
url: "http://arxiv.org/abs/2609.02417v1"
score: 0.95
topics: [agentic RL, RL training, reward model, GRPO, LLM agent]
status: unread
---

# Coverage, Not Targeting: A Structural Regime in Multi-Turn Agent Credit Assignment

## Summary

Identifies verifier information density (V_d = k/C, the fraction of an agent's C-step causal chain whose per-turn correctness the verifier exposes) as the structural quantity predicting when credit targeting helps; terminal-state verifiers sit at V_d ≈ 0.15 (far below the V_d* ≈ 0.8 crossover), making uniform coverage the correct default. Controlled experiments on tau²-bench and BFCL V3 across multiple model families confirm targeting is second-order when k=1 in 98% of rollouts; the matched-concentration shuffled control is proposed as the null that any future targeting claim must beat.

## Key Contributions

- Derives the verifier information density V_d = k/C as the structural predictor of the targeting vs. coverage regime boundary
- Empirically locates the phase crossover at V_d* ≈ 0.8; measures tau²-bench at V_d ≈ 0.15 and BFCL V3 at V_d ≈ 0.4 — both in the coverage regime
- Shows that uniform advantage redistribution consistently beats targeted credit across model families on both benchmarks, with targeted methods net-harmful on 4/5 seeds on tau²-bench
- Proposes the matched-concentration shuffled control as the minimum null any targeting method must clear

## Relevance

Directly answers the open CANOPY empirical question carried forward from Sep 12: whether the test-time interaction budget expansion in CANOPY is load-bearing, or whether coverage-anchoring alone explains the gain. This paper provides the theoretical framework (V_d) and empirical evidence that in terminal-state-verified multi-turn settings, coverage is the load-bearing axis — targeting is second-order.

## My Thoughts

<!-- Add your own notes here -->
