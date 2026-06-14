---
title: "R3L: Reflect-then-Retry Reinforcement Learning with Language-Guided Exploration, Pivotal Credit, and Positive Amplification"
authors: ["Weijie Shi", "Yanxi Chen", "Zexi Li", "Xuchen Pan", "Yuchang Sun", "Jiajie Xu", "Xiaofang Zhou", "Yaliang Li"]
date: 2026-06-14
arxiv_id: "2601.03715v2"
url: "http://arxiv.org/abs/2601.03715v2"
score: 0.78
topics: [agentic RL, RL training, LLM agent, reinforcement learning, PPO]
status: unread
---

# R3L: Reflect-then-Retry Reinforcement Learning with Language-Guided Exploration, Pivotal Credit, and Positive Amplification

## Summary

R3L addresses the dual failure modes of LLM agent RL — poor exploration on hard tasks and coarse credit assignment on successful ones — with three coupled mechanisms: Reflect-then-Retry uses language feedback to diagnose failures and synthesize high-quality off-policy trajectories by restarting from the identified failure point; Pivotal Credit Assignment restricts gradient updates to only the diverging suffix where a successful and failed trajectory branch apart, excluding the shared prefix; Positive Amplification upweights successful trajectories to prevent failure-dominated groups from overwhelming optimization. Together these mechanisms yield 5–52% relative improvements over baselines on agentic and reasoning benchmarks.

## Key Contributions

- Reflect-then-Retry: language model reflection diagnoses failure causes and transforms failed attempts into successful off-policy demonstrations, restarting rollouts from identified failure points to reduce cost
- Pivotal Credit Assignment: identifies where a successful trajectory diverges from a failed one and restricts gradient to only the diverging suffix — shared prefix excluded from update
- Positive Amplification: upweights successful trajectories when failures dominate the rollout group, preventing gradient collapse under high failure rates
- 5–52% relative improvements over RL baselines on agentic tasks; training stability maintained under high failure rates

## Relevance

R3L assembles three complementary credit assignment improvements that connect threads from recent digests: the failure-as-signal insight parallels SENTINEL's (Jun 12) failure-driven RL; Pivotal Credit Assignment is a simpler, prefix-aware variant of RREDCoT's (Jun 8) segment-level reward redistribution; and Positive Amplification addresses the same failure-dominated-group problem as Reasoning Arena's (Jun 13) trace tournaments — three independent solutions to the same zero-or-negative signal collapse.

## My Thoughts

<!-- Add your own notes here -->
