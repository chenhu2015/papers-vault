---
title: "M-GRPO: Stabilizing Self-Supervised Reinforcement Learning for Large Language Models with Momentum-Anchored Policy Optimization"
authors: ["Bizhe Bai", "Hongming Wu", "Peng Ye", "Tao Chen"]
date: 2025-12-15
arxiv_id: "2512.13070v1"
url: "http://arxiv.org/abs/2512.13070v1"
score: 0.86
topics: [RL training, reinforcement learning, GRPO, PPO]
status: unread
---

# M-GRPO: Stabilizing Self-Supervised Reinforcement Learning for Large Language Models with Momentum-Anchored Policy Optimization

## Summary

M-GRPO diagnoses a 'policy collapse' failure mode in long-horizon LLM RL training where performance precipitously degrades, and shows that simply scaling rollouts delays but cannot prevent it. It introduces a momentum model as a slowly evolving stable training target and an IQR-based adaptive filtering method that dynamically prunes low-entropy trajectories to prevent premature convergence. The combination achieves superior stability and state-of-the-art performance on multiple reasoning benchmarks.

## Key Contributions

- Diagnosis of 'policy collapse' in long-horizon LLM RL and evidence that scaling rollouts is insufficient
- Momentum-anchored policy optimization: slowly evolving reference model as stable training target
- IQR-based adaptive filtering that prunes low-entropy trajectories dynamically
- SOTA on multiple reasoning benchmarks with improved training stability

## Relevance

Addresses the KL/entropy/training stability carry-forward directly; pairs naturally with EP-GRPO (also June 2) and the broader RL training pathology thread — EchoRL (advantage degeneration, June 1), DARE (difficulty staleness, June 1) — forming a coherent picture of GRPO failure modes and fixes.

## My Thoughts

<!-- Add your own notes here -->
