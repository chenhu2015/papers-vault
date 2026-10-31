---
title: "EnvSched: Environment-Aware Scheduling for Rollout-Efficient Agent Reinforcement Learning"
authors: ["Sihan Yang", "Weichen Bai", "Ruichuan An", "Yiming Cheng", "Zhiyuan Feng", "Tianyi Jiang", "Renye Yan", "Ning Ding", "Yifan Zhang", "Renrui Zhang", "Yehui Tang", "Wentao Zhang"]
date: 2026-10-31
arxiv_id: "2610.37609v1"
url: "http://arxiv.org/abs/2610.37609v1"
score: 0.85
topics: [agentic RL, reinforcement learning, LLM agent, tool use]
status: unread
---

# EnvSched: Environment-Aware Scheduling for Rollout-Efficient Agent Reinforcement Learning

## Summary

EnvSched is an online scheduler for rollout-efficient agentic RL that models environment-task pairs as nodes in a dual-relation graph: within-environment edges capture task semantics and shared verifier structure, cross-environment edges capture abstract execution and reward topology. Propagating rollout history along both edge types predicts reward variance; the scheduler allocates batches to high-variance tasks with coverage quotas and similarity penalties to avoid redundancy. On Qwen3-8B across BFCL-v3, tau-Bench, and ACEBench-Agent, EnvSched reaches 40-step performance that random selection takes 120 steps to match.

## Key Contributions

- Dual-relation graph over environment-task pairs: within-environment (task semantics, tool/verifier sharing) and cross-environment (abstract execution topology) edges
- Online reward variance prediction by propagating rollout statistics along graph edges — no pilot rollouts needed
- Coverage quotas + similarity penalty prevent concentration on a few high-variance environments
- 3x training step reduction on Qwen3-8B across three agentic benchmarks

## Relevance

Extends the RL rollout efficiency / allocation thread (12 entries) with an environment-level scheduling angle that is orthogonal to all prior approaches. Existing papers (Nested-ReFT, FlexMARL, QwenGyre) optimise rollout generation speed or trajectory selection; EnvSched optimises which task-environment combinations to roll out in the first place, attacking rollout inefficiency at the curriculum level rather than the execution level.

## My Thoughts

<!-- Add your own notes here -->
