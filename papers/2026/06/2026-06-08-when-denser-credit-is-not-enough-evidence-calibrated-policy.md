---
title: "When Denser Credit Is Not Enough: Evidence-Calibrated Policy Optimization for Long-Horizon LLM Agent Training"
authors: ["Yuanfan Li", "Qi Zhou", "Wenjing Duan", "Lu Chen"]
date: 2026-06-04
arxiv_id: "2606.05885v1"
url: "http://arxiv.org/abs/2606.05885v1"
score: 0.82
topics: [agentic RL, RL training, GRPO, LLM agent, reinforcement learning]
status: unread
---

# When Denser Credit Is Not Enough: Evidence-Calibrated Policy Optimization for Long-Horizon LLM Agent Training

## Summary

ECPO identifies that step-level advantages in GiGPO can be statistically unreliable under limited rollouts — rare lucky actions get inflated advantages, causing divergent anchor bias and late-stage oscillation. It proposes Evidence-Calibrated Action Advantage (groups rollouts by canonical actions and shrinks low-count estimates) combined with Variance-Gated Credit Weighting (suppresses noise-dominated anchor states). On ALFWorld/WebShop, ECPO improves GiGPO by +5.2/+7.3 success points with only 0.1% additional overhead.

## Key Contributions

- Diagnostic analysis of GiGPO failure modes: divergent anchor bias from rare-but-lucky actions under limited rollouts
- Evidence-Calibrated Action Advantage: groups rollouts by canonical action, shrinks low-count advantage estimates to reduce variance
- Variance-Gated Credit Weighting: suppresses anchor states dominated by within-action noise
- Critic-free design preserves GiGPO's simplicity while fixing its statistical unreliability

## Relevance

Directly extends the multi-turn/long-horizon RL cluster (OpenWebRL/BranPO/Turn-PPO from June 2) with a principled fix for a failure mode in step-level credit assignment. Connects also to SIRI (same agent benchmarks: ALFWorld and WebShop) and the broader June 2–7 theme of fixing GRPO/GiGPO pathologies.

## My Thoughts

<!-- Add your own notes here -->
