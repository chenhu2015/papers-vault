---
title: "How Much, Then Where: Credit-Conserving Action-to-Token Allocation for Multi-Turn Agent Reinforcement Learning"
authors: ["Lichao Ma", "Yang Sun", "Shuaitao Zhao", "Yangyi Fang", "Cong Qin", "Xiaoliang Fu", "Yuhang Tian", "Yuchen Wei", "Junbo Zhu", "Yang Wei", "Lu Pan", "Jiaye Lin"]
date: 2026-08-07
arxiv_id: "2608.07118v1"
url: "http://arxiv.org/abs/2608.07118v1"
score: 0.88
topics: [agentic RL, RL training, GRPO, LLM agent, RLHF]
status: unread
---

# How Much, Then Where: Credit-Conserving Action-to-Token Allocation for Multi-Turn Agent Reinforcement Learning

## Summary

FACTOR separates multi-turn agent credit assignment into two orthogonal decisions: how much trajectory-level credit to assign to each action (via checkpoint-calibrated TD residuals) and where within an action's tokens to place that credit (via credit-conserving intra-action allocation). This decomposition avoids the conflation of inter-action and intra-action credit that causes gradient dilution in standard per-token GRPO, and the credit-conserving constraint prevents advantage mass from leaking across token boundaries.

## Key Contributions

- Decomposes multi-turn credit assignment into action-level (how much) and token-level (where) as two explicitly separated and independently optimised decisions
- Checkpoint-calibrated TD residuals for action-level credit: uses policy checkpoints as value function proxies to compute inter-action advantages without a separate critic
- Credit-conserving intra-action token allocation: ensures that advantage mass assigned to an action is redistributed within that action's tokens, not diluted across the full trajectory
- Addresses the gradient dilution failure mode in per-token GRPO by preventing cross-boundary advantage leakage

## Relevance

Directly extends the credit assignment cluster with a two-level decomposition framing that complements GACA (step-level), VICT (verifier-trace), and CrEST (turn-segmented + token-level). FACTOR's credit-conserving constraint is analogous to CrEST's entropy-gated modulation but operates at the action boundary rather than the turn boundary — the two framings are complementary and their interaction is worth exploring.

## My Thoughts

<!-- Add your own notes here -->
