---
title: "Policy-Adaptive Credit Assignment for Spatial Reasoning with Verifiable Rewards"
authors: ["Hailiang Yang", "Shengchao Chen"]
date: 2026-10-19
arxiv_id: "2610.26410"
url: "https://arxiv.org/abs/2610.26410"
score: 0.83
topics: [agentic RL, reward model, VLM, vision-language, multimodal models]
status: unread
---

# Policy-Adaptive Credit Assignment for Spatial Reasoning with Verifiable Rewards

## Summary

CALIPER proposes an adaptive process-reward framework for VLM spatial reasoning that jointly estimates the association between stage-wise reference coverage and answer correctness via within-group ridge regression, dynamically reweighting rewards to track the changing training bottleneck (perception → decomposition → inference). A closed-loop harness monitors estimator reliability and triggers checkpoint rollback, rollout diversification, and early stopping when utility estimates become unreliable. Achieves highest mean across 8 benchmarks and 3 backbones over fixed-weight process supervision.

## Key Contributions

- Adaptive reward weight allocation that uses within-group ridge regression to estimate stage-utility proxies and updates weights as the training bottleneck shifts
- SpatialTrace: a corpus of stage-decomposed spatial reasoning traces (perception, decomposition, inference) used as process supervision
- Closed-loop harness with automated estimator reliability monitoring, checkpoint rollback, and rollout diversification
- Demonstration that CALIPER supervises uniformly-failing rollout groups (where answer-level reward provides no gradient)

## Relevance

Directly extends the step-credit cluster (19 entries) to the spatial reasoning domain, providing the first adaptive (rather than fixed-weight) process reward mechanism for VLM RL. The ridge regression utility proxy connects to the VLM RL credit assignment thread — notably complementing PARA/GRAD's diagnostic framework from Oct 19: CALIPER provides a way to act on identified perception/reasoning bottlenecks by reweighting stage rewards accordingly.

## My Thoughts

<!-- Add your own notes here -->
