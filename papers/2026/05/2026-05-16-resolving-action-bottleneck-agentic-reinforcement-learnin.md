---
title: "Resolving Action Bottleneck: Agentic Reinforcement Learning Informed by Token-Level Energy"
authors: ["Langzhou He", "Junyou Zhu", "Yue Zhou", "Zhengyao Gu", "Junhua Liu", "Wei-Chieh Huang", "Henry Peng Zou", "David Wipf", "Philip S. Yu", "Qitian Wu"]
date: 2026-05-16
arxiv_id: "2605.14558v1"
url: "http://arxiv.org/abs/2605.14558v1"
score: 0.89
topics: [agentic RL, LLM agent, PPO, GRPO, RL training]
status: unread
---

# Resolving Action Bottleneck: Agentic Reinforcement Learning Informed by Token-Level Energy

## Summary

Token-level training signals in multi-turn agentic RL concentrate sharply on action tokens rather than reasoning tokens — the "Action Bottleneck" — even though action tokens are only a tiny fraction of the trajectory. ActFocus reweights gradients by downweighting reasoning tokens and boosting high-uncertainty action tokens via an energy-based redistribution mechanism, yielding gains of up to 65.2pp over PPO and 63.7pp over GRPO across four agent environments with no added runtime cost.

## Key Contributions

- Identifies the Action Bottleneck: empirical finding that reward-correlated signal concentrates on action tokens (~small fraction of trajectory), not reasoning tokens
- ActFocus: embarrassingly simple token reweighting — downweight reasoning gradients, add energy-based redistribution to action tokens with higher uncertainty
- 65.2pp over PPO, 63.7pp over GRPO on four environments at various model sizes
- Zero additional runtime or memory cost compared to standard PPO/GRPO

## Relevance

Directly addresses the credit assignment problem in agentic RL (PPO/GRPO keywords), explaining why reasoning traces receive disproportionate gradient budget despite carrying little reward signal. Connects naturally to the GRPO/PRM credit assignment thread from May 12 (VPR, GenAC) but offers a completely different diagnostic: the bottleneck is at the token reweighting level, not the reward model level.

## My Thoughts

<!-- Add your own notes here -->
