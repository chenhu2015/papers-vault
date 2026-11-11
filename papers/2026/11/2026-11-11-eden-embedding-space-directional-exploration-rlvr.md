---
title: "Beyond Policy Rollouts: Embedding-Space Directional Exploration via anchored Noise for LLM RLVR"
authors: ["Daijiao Liu", "Huiyi Wang", "Lina Yao", "Dong Gong"]
date: 2026-11-11
arxiv_id: "2610.16105v1"
url: "http://arxiv.org/abs/2610.16105v1"
score: 0.83
topics: [agentic RL, RL training, GRPO]
status: unread
---

# Beyond Policy Rollouts: Embedding-Space Directional Exploration via anchored Noise for LLM RLVR

## Summary

EDEN (Embedding-space Directional Exploration via anchored Noise) addresses low within-group reward variation in RLVR by intervening at the rollout source: a fraction of each rollout group is generated from the prompt plus an anchored Gaussian-perturbed embedding position, introducing diversity without changing the model architecture or test-time inference. Within the same rollout budget, EDEN expands the prompt groups providing non-zero learning signals; complementary roles of noise (variation) and anchoring (shared conditioning direction) are confirmed through ablations, and EDEN outperforms GRPO across model scales on mathematical reasoning benchmarks.

## Key Contributions

- Intervenes at the rollout source via embedding-space perturbation (Gaussian noise + shared anchor per group) rather than modifying policy updates or sampling temperature
- Downweighted advantage for perturbed rollouts prevents the diverse candidates from destabilizing the update
- Model architecture, discrete decoding, and test-time inference remain unchanged — a purely training-time diversity injection
- Improves solution coverage (more prompt groups with non-zero advantage signal) across scales; noise and anchoring play complementary roles per ablation

## Relevance

This directly extends the RLVR exploration thread opened by TGRL (Nov 10, temperature-grouped JS divergence credit): where TGRL groups rollouts by temperature to assign credit, EDEN perturbs the prompt embedding to generate a structurally different rollout, attacking the same low-diversity / zero-gradient problem from a different angle. Together they form a small cluster of exploration-at-the-rollout-source methods.

## My Thoughts

<!-- Add your own notes here -->
