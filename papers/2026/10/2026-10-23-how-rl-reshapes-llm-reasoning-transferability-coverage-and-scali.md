---
title: "How RL Reshapes LLM Reasoning: Transferability, Coverage, and Scaling Laws"
authors: ["Ziheng Cheng", "Yixiao Huang", "Hanlin Zhu", "Somayeh Sojoudi"]
date: 2026-10-03
arxiv_id: "2610.04158v1"
url: "https://arxiv.org/abs/2610.04158"
score: 0.83
topics: [RL training, GRPO, agentic RL, reward model]
status: unread
---

# How RL Reshapes LLM Reasoning: Transferability, Coverage, and Scaling Laws

## Summary

Analyzes how RL post-training shifts LLM reasoning strategy distributions, resolving seemingly conflicting evidence on cross-domain transfer and coverage. Introduces a two-stage autoregressive policy model separating strategy selection from execution, and proves log-sigmoid and log-linear scaling laws for RL compute. Shows that RL's implicit bias on strategy preferences can simultaneously broaden coverage on some tasks while narrowing it on others.

## Key Contributions

- Two-stage policy model separating strategy selection from problem-specific execution, explaining cross-domain transfer and coverage changes
- Formal proof of log-sigmoid and log-linear scaling laws for RL compute budget
- Empirical analysis across Qwen and Gemma families showing both cross-domain gains and forgetting depending on strategy overlap
- Theoretical mechanism linking RL's strategy-preference reshaping to both coverage expansion and suppression at fixed sampling budgets

## Relevance

Directly addresses the test-time compute + RL scaling angle that has been absent from recent digests, providing the theoretical underpinning for why RL training at scale produces the results it does. Connects to the step-credit cluster and GRPO training dynamics threads by explaining the strategy-selection layer beneath reward optimization.

## My Thoughts

<!-- Add your own notes here -->
