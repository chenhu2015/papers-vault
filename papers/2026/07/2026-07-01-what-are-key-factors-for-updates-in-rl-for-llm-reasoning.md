---
title: "What are Key Factors for Updates in RL for LLM Reasoning?"
authors: ["Peidong Wang", "Demi Wang", "Xufang Luo", "Jiahang Xu", "Xiaocui Yang", "Shi Feng", "Yuqing Yang", "Dongsheng Li"]
date: 2026-06-21
arxiv_id: "2606.22570v1"
url: "http://arxiv.org/abs/2606.22570v1"
score: 0.80
topics: [RLHF, GRPO, PPO, RL training, reinforcement learning]
status: unread
---

# What are Key Factors for Updates in RL for LLM Reasoning?

## Summary

Theoretical analysis of RLVR updates reveals that off-policy degree (gradient steps per rollout) substantially affects importance sampling ratio distributions and clipping behavior, determining which tokens dominate the update; gradient expectation over token probability, advantage, and IS ratio is identified as the central governing quantity. ACPO (Adaptive Clip Policy Optimization) adjusts clipping boundaries per token group according to empirical IS ratio variance, outperforming DAPO and CISPO across math, tabular QA, and logic reasoning benchmarks on 3B/7B models.

## Key Contributions

- Theoretical characterization of RLVR update dynamics: off-policy degree controls IS ratio distribution, which determines effective token-level learning signal under clipping
- Gradient expectation as the unifying quantity governing which tokens learn and which are effectively muted by clipping
- ACPO: per-token-group adaptive clipping where clip boundary scales with empirical IS ratio variance within the group, preventing both over-conservatism (flat learning) and over-aggressiveness (instability)
- Comprehensive ablation distinguishing the roles of token probability, advantage value, and IS ratio in the update, explaining why divergent algorithmic choices (DAPO, CISPO, etc.) can each report gains despite contradicting each other

## Relevance

ACPO provides the theoretical foundation that was missing from the GRPO variant landscape accumulated in June digests (GRPO, DAPO, DEEP-GRPO, EP-GRPO, BPPO, etc.) — instead of another heuristic variant, it explains mechanistically why any given variant wins on its specific benchmark. The off-policy degree finding directly connects to the credit resolution mismatch identified by PASS (today): both papers identify clipping and standardization as the primary loss pathways, from complementary perspectives (PASS: signal contamination; ACPO: IS ratio distribution).

## My Thoughts

<!-- Add your own notes here -->
