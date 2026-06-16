---
title: "A First-Principles Derivation of LLM Policy Optimization: From Expected Reward to GRPO and Its Structural Extensions"
authors: ["Jianghan Shen", "Siqi Luo", "Yue Li", "Jiyao Liu", "Wanying Qu", "Yi Zhang", "Ziyan Huang", "Tianbin Li", "Ming Hu", "Xiaohong Liu", "Yirong Chen", "Junjun He"]
date: 2026-06-16
arxiv_id: "2606.16733v1"
url: "http://arxiv.org/abs/2606.16733v1"
score: 0.79
topics: [reinforcement learning, agentic RL, PPO, GRPO, RL training, reward model]
status: unread
---

# A First-Principles Derivation of LLM Policy Optimization: From Expected Reward to GRPO and Its Structural Extensions

## Summary

This survey derives all LLM policy optimization methods from the single objective J(θ) = E[R(τ)] and organizes them along two axes: the trajectory side (modifications to p_θ(τ)) and the reward side (modifications to R(τ)), covering REINFORCE → PPO → GRPO and post-GRPO variants including agentic RL and GRPO-OPD. The framework is diagnostic and extensible: it identifies which side each method modifies and why, and exposes compound failures that no single-side fix can resolve. The boundary cases identified mark where existing solutions run out and provide a principled starting point for next-generation LLM policy optimization.

## Key Contributions

- Unified two-axis framework (trajectory side vs reward side) organizing the full landscape from J(θ) on first principles
- Diagnostic analysis of why each method works: which factor it modifies, what failure it addresses, and where the intervention sits in the gradient estimator
- Identification of compound failures requiring joint trajectory+reward design — the structural gap no existing method solves alone
- Coverage of agentic RL and GRPO-OPD within the same framework as single-turn reasoning methods

## Relevance

This is the synthesis framework the past six weeks of individual papers have been building toward. The trajectory/reward two-axis structure maps directly onto what the Credit Assignment Survey (Jun 14) did for the CA literature — that paper organized by granularity×methodology while this one organizes by J(θ) factor. Together they provide orthogonal taxonomic handles on the same body of work. The compound failures category is particularly valuable: CPPO, ALP, and DCMDP all target specific failure modes, but this framework can identify which of those target single-axis vs compound problems.

## My Thoughts

<!-- Add your own notes here -->
