---
title: "Compositional RL: Evaluating and Training LLMs for Collaborative Reasoning"
authors: ["Shangbin Feng", "Yulia Tsvetkov", "Jan Kautz", "David Acuna"]
date: 2026-10-16
arxiv_id: "2610.17456"
url: "https://arxiv.org/abs/2610.17456"
score: 0.75
topics: [agentic RL, LLM agent, reinforcement learning, RLHF]
status: unread
---

# Compositional RL: Evaluating and Training LLMs for Collaborative Reasoning

## Summary

This work formalizes a model's value in multi-agent systems using Shapley values over model coalitions, finding that individual benchmark strength and compositional (collaborative) strength are largely uncorrelated across 15 pool-method settings. C-RL trains a policy inside a live multi-model system rewarding collaborative outcome rather than individual correctness; the Shapley leave-one-out baseline cancels under a group policy gradient, adding no rollout overhead. Across three collaboration protocols and eight tasks, C-RL lifts collaborative performance by +4.0 to +5.4 pts on average (up to +13.1 pts), outperforming standard RL in 21 of 24 settings.

## Key Contributions

- Shapley-value framework for measuring compositional (collaborative) model strength — n+1 evaluations vs 2^n brute force
- Empirical finding: individual benchmark rank and collaborative rank are uncorrelated in 12 of 15 settings
- C-RL: group policy gradient where the Shapley leave-one-out baseline cancels, requiring no additional rollout
- +4.0–5.4 pts average collaborative performance gain across 8 tasks spanning reasoning, coding, and scientific discovery

## Relevance

C-RL extends the agentic RL thread in a new direction: instead of credit assignment within a single trajectory, it addresses credit assignment across models in a collaborative system, using Shapley values as a formal credit mechanism. This connects to the step-credit cluster's long-running concern with "who contributed what" — generalizing from steps-within-agent to agents-within-system.

## My Thoughts

<!-- Add your own notes here -->
