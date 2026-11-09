---
title: "Reward Budgeting Reduces Premature Convergence in Reinforcement Learning for LLM Reasoning"
authors: ["Mengni Jia", "Mengyu Zhou", "Xiaoxi Jiang", "Guanjun Jiang"]
date: 2026-11-04
arxiv_id: "2611.05942"
url: "https://arxiv.org/abs/2611.05942"
score: 0.80
topics: [GRPO, reinforcement learning, reward model, RL training, PPO]
status: unread
---

# Reward Budgeting Reduces Premature Convergence in Reinforcement Learning for LLM Reasoning

## Summary

Reward Budgeting is a plug-in advantage construction that assigns a fixed total reward budget per prompt, so advantage gaps diminish as more rollouts succeed; for binary rewards this is exactly the gradient of a finite-G concave objective with diminishing returns. The approach introduces a sharpness factor κ and effective counterpart κ_eff that describe how reward or advantage gaps translate into policy probability-ratio gaps, diagnosing why entropy manipulation alone fails to prevent early plateaus. On Qwen3-8B and Llama3.2-3B-Instruct, gains reach +12.50 AMC23, +10.00 AIME24 and AIME25.

## Key Contributions

- Sharpness factor κ and effective κ_eff as diagnostic lens for premature convergence — separates reward/advantage gaps from their effect on policy probability ratios
- Reward Budgeting: plug-in advantage construction with fixed per-prompt budget; advantage gap decreases as more rollouts succeed, providing automatic diminishing-returns schedule
- Mathematical grounding: exact gradient of a finite-G concave objective for binary rewards; shifted log-mean interpretation for general rewards (asymptotically)
- Strong empirical gains (+12.50 AMC23, +10 AIME) without explicit entropy constraints

## Relevance

This paper adds a principled new mechanism to the GRPO training dynamics thread (now 15+ entries). It is conceptually adjacent to GRAFT (Nov 8, all-fail peer exchange) and VeXact (Nov 8, TIM diagnostic) but attacks premature convergence from the advantage construction angle rather than the data or rollout angle. The concave-objective interpretation of reward budgeting complements the TAC curriculum approach (Nov 8) which uses gradient geometry for multi-domain scheduling.

## My Thoughts

<!-- Add your own notes here -->
