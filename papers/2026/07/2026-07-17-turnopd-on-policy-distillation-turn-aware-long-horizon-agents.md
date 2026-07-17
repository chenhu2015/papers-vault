---
title: "TurnOPD: Making On-Policy Distillation Turn-Aware for Efficient Long-Horizon Agent Training"
authors: ["Yuhang Zhou", "Kai Zheng", "Haoling Li", "Dengyun Peng", "Can Xu", "Jingjing Chen"]
date: 2026-07-17
arxiv_id: "2607.05804v1"
url: "http://arxiv.org/abs/2607.05804v1"
score: 0.78
topics: [agentic RL, LLM agent, RL training]
status: unread
---

# TurnOPD: Making On-Policy Distillation Turn-Aware for Efficient Long-Horizon Agent Training

## Summary

Identifies two inefficiencies in vanilla on-policy distillation (OPD) for long-horizon agents: tail turns produce weak and noisy KL supervision wasting wall-clock, and trajectory-level KL concentrates loss on shallow tokens leaving decision turns under-trained after initial alignment. TurnOPD introduces two turn-level budget controllers: adaptive rollout-depth budgeting (probe-based turn statistics to determine when to truncate) and progressive turn-normalized loss (gradually shifts KL weighting from token-level to turn-balanced supervision). Achieves superior accuracy on ALFWorld, WebShop, and Multi-Hop Search under equal wall-clock training budgets.

## Key Contributions

- Diagnoses two OPD failure modes for long-horizon agents: tail-turn noise waste and shallow-token KL concentration
- Adaptive rollout-depth budgeting: probe-based turn statistics gate rollout length, cutting waste without accuracy loss
- Progressive turn-normalized loss: gradually reweights KL from token-level to turn-balanced, ensuring decision turns are trained
- Superior accuracy-time frontier on ALFWorld, WebShop, Multi-Hop Search vs vanilla OPD

## Relevance

Extends the agentic RL training efficiency thread that today's digest opened (alongside Prune-OPD). The "when to truncate rollouts" question is structurally the same as TTI's "when to extend rollout horizons" — TurnOPD's probe-based truncation addresses the complementary problem of wasted tail-turn compute in distillation vs. RL. The progressive turn-normalized loss connects to Learning When to Plan's insight that indiscriminate supervision across all steps degrades long-horizon training.

## My Thoughts

<!-- Add your own notes here -->
