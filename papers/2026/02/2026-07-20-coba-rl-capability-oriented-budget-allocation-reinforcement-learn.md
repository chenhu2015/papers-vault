---
title: "CoBA-RL: Capability-Oriented Budget Allocation for Reinforcement Learning in LLMs"
authors: ["Zhiyuan Yao", "Yi-Kai Zhang", "Yuxin Chen", "Yueqing Sun", "Zishan Xu", "Yu Yang", "Tianhao Hu", "Qi Gu", "Hui Su", "Xunliang Cai"]
date: 2026-02-03
arxiv_id: "2602.03048"
url: "http://arxiv.org/abs/2602.03048v3"
score: 0.78
topics: [GRPO, RL training, reinforcement learning, agentic RL]
status: unread
---

# CoBA-RL: Capability-Oriented Budget Allocation for Reinforcement Learning in LLMs

## Summary

CoBA-RL proposes adaptive rollout budget allocation in RLVR based on the model's evolving capability rather than static per-instance metrics such as pass rates. A Capability-Oriented Value function maps tasks to their potential training gain given the current model state, and a heap-based greedy strategy allocates more rollouts to samples with high training value while avoiding over-sampling easy or saturated prompts. Consistent generalization improvements across multiple benchmarks demonstrate that quantifying sample training value is a meaningful axis for GRPO post-training efficiency.

## Key Contributions

- Capability-Oriented Value function that maps each task to its potential training gain conditioned on the model's current capability state — capturing dynamic learning value rather than static instance difficulty
- Heap-based greedy rollout allocation that self-calibrates the distribution of compute to high-training-value samples
- Differentiates from IGRPO (information gain per rollout branch) and RL-ZVP (zero-variance prompt recovery): CoBA-RL operates at the dataset sampling level, not the within-prompt branch level
- Consistent generalization improvements across challenging benchmarks

## Relevance

CoBA-RL extends the data efficiency thread (RL-ZVP, IGRPO, GeoMin) with a capability-aware sampling signal: where IGRPO decides which branches to expand within a prompt and RL-ZVP recovers value from zero-variance prompts, CoBA-RL decides which prompts to sample more from given the model's current learning state. The Capability-Oriented Value function is a novel signal orthogonal to instance-level pass rate or entropy.

## My Thoughts

<!-- Add your own notes here -->
