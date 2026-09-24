---
title: "GVPO++: Group Variance Policy Optimization for LLM Post-Training and On-Policy Distillation"
authors: ["Kaichen Zhang", "Yuzhong Hong", "Junwei Bao", "Hongfei Jiang", "Yang Song", "Dingqian Hong", "Hui Xiong"]
date: 2026-09-18
arxiv_id: "2609.21432v1"
url: "https://arxiv.org/abs/2609.21432"
score: 0.88
topics: [GRPO, RL training, RLHF, reward model]
status: unread
---

# GVPO++: Group Variance Policy Optimization for LLM Post-Training and On-Policy Distillation

## Summary

GVPO integrates the analytical solution of KL-constrained reward maximization into its gradient weighting scheme, replacing GRPO's importance-sampling ratio with the MSE between central distances of implicit vs actual rewards — guaranteeing a unique optimal solution to the constrained objective. This formulation allows flexible sampling distributions without importance sampling, eliminating the training instability that plagues GRPO. GVPO extends naturally to on-policy distillation, providing a principled foundation for a broad family of OPD objectives.

## Key Contributions

- Derives gradient of GVPO as MSE between central distances of implicit rewards and actual rewards — an intuitive interpretation that GRPO lacks
- Guarantees a unique optimal solution exactly equal to the KL-constrained reward maximization objective
- Enables flexible sampling distributions: no importance sampling ratio required, no off-policy instability
- Natural extension to on-policy distillation (OPD) and a unified family of extended OPD objectives

## Relevance

Directly addresses the training instability identified in GRPO (importance-sampling ratio causes gradient variance spikes) that has been a recurring concern in the RL training thread. The principled theoretical foundation — unique optimal solution, flexible sampling — makes GVPO a compelling drop-in replacement in any GRPO-based pipeline, including multi-task and agentic settings studied in recent digests.

## My Thoughts

<!-- Add your own notes here -->
