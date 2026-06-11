---
title: "3SPO: State-Score-Supervised Policy Optimization for LLM Agents"
authors: ["Yu Han", "Kailing Li", "Yang Jiao", "Yulin Dai", "Yuqian Fu", "Linhai Zhuo", "Tianwen Qian"]
date: 2026-06-11
arxiv_id: "2606.09961v1"
url: "http://arxiv.org/abs/2606.09961v1"
score: 0.82
topics: [agentic RL, GRPO, LLM agent, RL training]
status: unread
---

# 3SPO: State-Score-Supervised Policy Optimization for LLM Agents

## Summary

Trajectory-level RL algorithms require complete episode rollouts before any update, which is problematic for multi-turn agents where rewards are sparse and delayed. 3SPO performs post-step policy optimization using dynamic state scores derived from historical per-state success rates, enabling adaptive rollout and step-wise credit assignment without a value function or auxiliary models. On ALFWorld and WebShop with Qwen2.5-1.5B/7B, 3SPO outperforms GRPO by +22.6% and +15.6 points while achieving 2.4× more state exploration at comparable cost.

## Key Contributions

- Post-step policy optimization with dynamic state score supervision (no value function or auxiliary models)
- State scores computed from historical per-state success rates, updated during training
- Per-state bandit abstraction with formal logarithmic allocation regret guarantee
- +22.6% ALFWorld, +15.6 WebShop over GRPO; 2.4× more state exploration, 1.8× faster convergence

## Relevance

Fills an important gap left by GRPO's trajectory-level credit assignment: 3SPO is the per-step version. This extends the credit assignment thread from RREDCoT (segment-level CoT credit, Jun 8) and ECPO (GiGPO anchor bias fix, Jun 8) into a fully step-level agent RL solution without adding a learned critic model.

## My Thoughts

<!-- Add your own notes here -->
