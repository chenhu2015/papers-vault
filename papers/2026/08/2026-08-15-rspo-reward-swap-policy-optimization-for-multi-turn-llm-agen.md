---
title: "RSPO: Reward-Swap Policy Optimization for Multi-Turn LLM Agents"
authors: ["Qiang Liu", "Taian Guo", "Ruizhi Qiao", "Xing Sun"]
date: 2026-08-15
arxiv_id: "2607.04713"
url: "http://arxiv.org/abs/2607.04713v2"
score: 0.75
topics: [agentic RL, LLM agent, GRPO, PPO, RL training]
status: unread
---

# RSPO: Reward-Swap Policy Optimization for Multi-Turn LLM Agents

## Summary

RSPO resolves the tension between dense process rewards (rich signal, possibly misaligned) and sparse outcome rewards (aligned but slow convergence) in multi-turn agentic RL: the reward-swap mechanism uses process rewards to diversify sampled trajectories while ensuring the optimization objective remains the true outcome reward. Applied as a wrapper to GRPO, PPO, and GiGPO on WebShop and ALFWorld, RSPO consistently improves all three baselines by leveraging process reward information for exploration without introducing outcome-misalignment bias.

## Key Contributions

- Identifies the rich-vs-aligned dilemma in multi-turn agent RL: process rewards improve sampling but bias the objective away from true outcomes
- Reward-swap mechanism: use process rewards for trajectory diversification during rollout, swap to outcome rewards for policy gradient update
- Plug-in wrapper compatible with GRPO, PPO, and GiGPO — generalizes across policy optimization algorithms
- Consistent improvement on WebShop and ALFWorld across all three baselines

## Relevance

RSPO addresses the same alignment-vs-richness tension as SOD's divergence-adaptive gating in a complementary way: SOD adaptively gates when to apply dense OPD supervision based on divergence magnitude, while RSPO accepts the process reward fully for exploration and only swaps it out at the gradient update stage. Together they represent two design points in the "when to use dense signals" design space for agentic RL—SOD's gating is continuous (weight by divergence magnitude) while RSPO's swap is discrete (use process for sampling, outcome for updating). This directly connects to the multi-turn sparse reward problem that CSO (same digest) and PAIR address from different angles.

## My Thoughts

<!-- Add your own notes here -->
