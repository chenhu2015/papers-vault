---
title: "Stabilizing Off-policy LLM Optimization with Prefix Importance Ratio"
authors: ["Shiye Lei", "Zhihao Cheng", "Dacheng Tao"]
date: 2026-01-30
arxiv_id: "2601.22718v2"
url: "https://arxiv.org/abs/2601.22718"
score: 0.89
topics: [reinforcement learning, RL training, GRPO, PPO, agentic RL]
status: unread
---

# Stabilizing Off-policy LLM Optimization with Prefix Importance Ratio

## Summary

MinPRO demonstrates that token-level importance sampling fails to correct for prefix distribution shift in off-policy LLM RL — the exact correction requires the cumulative prefix importance ratio, which is unstable under large policy lag. MinPRO replaces the cumulative ratio with the minimum token-level ratio over the preceding prefix as a stable biased surrogate, without accumulating errors across the sequence. Experiments on dense and MoE LLMs across math reasoning benchmarks show substantially improved training stability and peak performance in off-policy regimes.

## Key Contributions

- Proves that prefix-marginal policy gradient correction requires the cumulative prefix importance ratio (product of token ratios), not token-level ratios
- Identifies that cumulative prefix ratio becomes unstable under large policy lag (the exact formula diverges)
- Proposes MinPRO: replaces cumulative ratio with min(token ratios over prefix) as a biased but stable surrogate
- Validates on dense and MoE LLMs across math reasoning; substantially improves stability and peak performance vs. token-level IS objectives

## Relevance

Directly extends the IS ratio/trust region cluster (LGPO + EPIC + MinPRO): LGPO showed IS ratio is unnecessary in on-policy regimes; EPIC derived the exact prefix-level IS weight from MDP reformulation; MinPRO completes the picture by identifying that the exact cumulative prefix ratio is unstable and deriving a stable min-based surrogate for large off-policy drift. The three papers together give a full mechanistic account of when and how IS correction should (and should not) be applied in LLM RL training.

## My Thoughts

<!-- Add your own notes here -->
