---
title: "ReAPO: Retry-Aware Policy Optimization for Efficient Exploration in LLM Reasoning"
authors: ["Nghi Dao", "Calder Morton-Ferguson", "Noah Golowich", "Adam Block"]
date: 2026-10-20
arxiv_id: "2610.28770v1"
url: "https://arxiv.org/abs/2610.28770"
score: 0.80
topics: [GRPO, RL training, agentic RL, RLHF]
status: unread
---

# ReAPO: Retry-Aware Policy Optimization for Efficient Exploration in LLM Reasoning

## Summary

ReAPO models multi-attempt rollout sequences as a Stochastic Shortest Path MDP to derive principled per-attempt credit assignment. Built as a simple GRPO modification, it allocates extra generation to failed trajectories and reinforces successful retries without rewarding preceding failures. Outperforms GRPO on 8 math/science benchmarks while using 31–39% fewer tokens than doubling group size or training steps.

## Key Contributions

- Frames multi-attempt RLVR exploration as a Stochastic Shortest Path MDP, providing a theoretical basis for retry-aware credit assignment
- Simple GRPO modification: extra generation budget to failed rollouts + credit only to the successful retry, not preceding failures
- 31–39% token reduction vs. doubling GRPO group size or training steps to reach same accuracy on Qwen3-0.6B
- Validated across Qwen3 and OLMo-2 models (0.6B–4B) on 8 math/science benchmarks

## Relevance

Extends the step-credit cluster with a novel angle: treating retry sequences as dependent rather than independent rollouts, framing the credit problem theoretically via SSP. Connects to the multi-turn agentic RL thread (State-Space Exploration, CoD) as retry-dependence is a structural analog of multi-turn dependency management.

## My Thoughts

<!-- Add your own notes here -->
