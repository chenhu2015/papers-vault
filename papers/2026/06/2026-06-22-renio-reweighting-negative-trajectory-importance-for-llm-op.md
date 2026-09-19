---
title: "ReNIO: Reweighting Negative Trajectory Importance for LLM On-Policy Distillation"
authors: ["Chen Lin", "Kedi Chen", "Wei Zhang"]
date: 2026-06-22
arxiv_id: "2606.23104v1"
url: "http://arxiv.org/abs/2606.23104v1"
score: 0.80
topics: [RLHF, RLAIF, LLM agent, reward model]
status: unread
---

# ReNIO: Reweighting Negative Trajectory Importance for LLM On-Policy Distillation

## Summary

ReNIO identifies a consistent asymmetry in on-policy distillation: training only on incorrect student-generated outputs outperforms training on correct ones, because incorrect outputs preserve exploratory reasoning near the model's capability boundary. Using the student-to-teacher probability ratio, ReNIO identifies pivotal tokens in wrong reasoning traces and computes normalized sample weights without requiring final-answer observation, preserving OPD's prefix-training advantage over full-rollout RL. Relative gains reach 10.0% for Qwen-7B on mathematical reasoning benchmarks.

## Key Contributions

- Asymmetry finding: incorrect SGOs outperform correct ones in OPD; incorrect outputs preserve exploratory reasoning, correct ones produce shorter chains with weaker reflection
- Student-to-teacher probability ratio: identifies pivotal tokens leading to wrong traces without observing the final answer
- Normalized sample weights from prefix-conditioned probabilities: no full rollout needed, preserving OPD's prefix-training advantage
- Up to 10.0% relative gain on Qwen-7B math reasoning; improvements on both OPD and OPSD

## Relevance

ReNIO introduces a trajectory-level weighting angle orthogonal to BATON's trajectory mass normalization (TMN): BATON addresses inter-trajectory batch aggregation (equal mass across trajectories), while ReNIO addresses which trajectories to emphasize (negative > positive). Together they define a two-dimensional batch design space for GRPO-style training that no prior paper has characterized jointly.

## My Thoughts

<!-- Add your own notes here -->
