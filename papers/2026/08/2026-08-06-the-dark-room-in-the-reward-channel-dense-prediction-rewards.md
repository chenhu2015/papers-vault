---
title: "The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents -- and The Channel, Not the Content, Decides What Works"
authors: ["Yu Wang"]
date: 2026-08-06
arxiv_id: "2607.21273"
url: "https://arxiv.org/abs/2607.21273"
score: 0.79
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents

## Summary

This paper systematically characterizes why dense per-step prediction rewards collapse GRPO-trained LLM agents through 74 preregistered ablation arms across ALFWorld, WebShop, a synthetic POMDP, and Qwen3-1.7B/4B/8B. The core finding is that in all-fail groups, standard z-score normalization cancels the shaping coefficient of any dense reward signal, causing the optimizer to exploit environment structure (the "dark room") rather than task-relevant behavior; a signal's danger is predictable from its within-group variance trajectory plus hackability. The delivery channel (auxiliary loss vs. reward channel), not signal content, determines training outcome—and content-free auxiliary updates match or beat gold signal in multiple configurations.

## Key Contributions

- 74-arm preregistered study isolating dense prediction reward effects in GRPO across scales and environments
- "Dark room" collapse mechanism: in all-fail groups, z-score normalization cancels the dense shaping coefficient → optimizer finds reward-maximizing absorbing states unrelated to task
- Within-group variance trajectory + hackability as predictors of reward channel danger
- Content-free auxiliary updates (placebo) match or beat gold signal at 4B scale; at 8B, recipe turns bistable — regime-dependent safety
- Removing std normalization restores baseline parity, identifying it as the structural cause of collapse

## Relevance

This paper provides a structural explanation for why dense teacher supervision signals (ADRS, PCSD, FutureBridge-OPD) in the vault's OPD thread must be delivered carefully. The "dark room" collapse is the same failure mode that OCSD (today) addresses by calibrating the observation residual — if the scaffold-induced score changes dominate the teacher signal, the within-group variance collapses and GRPO exploits the scaffold rather than the task. This also connects to Gap #16: the all-fail group filtering literature (CIGPO, TAO-RL, etc.) is motivated by exactly this collapse mechanism, which this paper now formally characterizes for dense reward channels.

## My Thoughts

<!-- Add your own notes here -->
