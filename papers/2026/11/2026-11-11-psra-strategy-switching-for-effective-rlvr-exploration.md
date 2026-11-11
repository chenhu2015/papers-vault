---
title: "The Model Knows Another Way: Strategy Switching for Effective RLVR Exploration"
authors: ["Jin Cui", "Xinyue Long", "Boran Zhao", "Pengju Ren", "Hao Dong"]
date: 2026-11-11
arxiv_id: "2609.33085v1"
url: "http://arxiv.org/abs/2609.33085v1"
score: 0.82
topics: [agentic RL, RL training, GRPO, reinforcement learning]
status: unread
---

# The Model Knows Another Way: Strategy Switching for Effective RLVR Exploration

## Summary

PSRA (Problem-Strategy Rollout Allocation) treats unguided and strategy-conditioned prompts as competing exploration arms, using Bayesian sequential allocation to direct a fixed rollout budget toward arms most likely to yield informative, non-saturated groups. A preservation objective keeps useful strategy-conditioned routes accessible while successful guided behaviors transfer to the unguided policy, reducing dead saturation. Across Qwen2.5 models 1.5B–7B, PSRA consistently improves reasoning performance and maintains gains under increased inference budgets.

## Key Contributions

- Frames RLVR exploration as a bandit problem: unguided vs strategy-conditioned prompt variants as arms; Bayesian sequential allocation directs rollout budget
- Identifies that all-fail groups often reflect finite-sampling saturation of one dominant strategy, not missing capability — alternative strategies already exist in the model
- Preservation objective prevents accessible strategy-conditioned routes from being absorbed/forgotten as guided behaviors succeed
- Consistent improvement across Qwen2.5 1.5B–7B, stronger gains with larger inference budget

## Relevance

Directly follows the TGRL (temperature-grouped exploration, Nov 10) and EDEN (embedding-space perturbation, today) cluster — all three attack the exploration/saturation problem in RLVR but via different mechanisms: TGRL via temperature partitioning + JS divergence credit, EDEN via embedding-space perturbation, PSRA via strategy-conditioned arm allocation. PSRA's bandit framing is the most structured and explicitly addresses the accessibility/forgetting dimension that TGRL and EDEN leave open.

## My Thoughts

<!-- Add your own notes here -->
