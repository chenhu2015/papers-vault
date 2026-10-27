---
title: "Learning at the Right Pace: Adaptive Data Scheduling Improves LLM Reinforcement Learning"
authors: ["Zicheng Xu", "Ruixuan Zhang", "Yu-Neng Chuang", "Xiuyi Lou", "Hoang Anh Duy Le", "Oren Gal", "Alexander S. Szalay", "Zhaozhuo Xu", "Guanchu Wang", "Vladimir Braverman"]
date: 2026-06-21
arxiv_id: "2606.22305"
url: "https://arxiv.org/abs/2606.22305"
score: 0.87
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# Learning at the Right Pace: Adaptive Data Scheduling Improves LLM Reinforcement Learning

## Summary

Adaptive Data Scheduling (ADS) introduces a dual-level framework for LLM RL post-training that organises training samples into semantic clusters and adapts inter-cluster sampling toward clusters within the policy's current capability boundary, while simultaneously tracking individual prompts near the capability frontier for within-cluster selection. This directly addresses the limitation of uniform sampling in GRPO, which ignores both semantic structure and the evolving capability of the training policy. ADS improves average accuracy by 5.5% over GRPO across 3 LLMs and 7 reasoning benchmarks and generalises across RL objectives with different designs.

## Key Contributions

- Dual-level scheduling: inter-cluster adaptive distribution (prioritises reachable clusters) + intra-cluster boundary-aware sample selection
- Cluster organisation based on semantic patterns, not difficulty alone — distinguishes semantic structure from capability frontier
- +5.5% average accuracy over GRPO on 7 reasoning benchmarks across 3 LLMs
- Generalises across different RL objective designs (not GRPO-specific), positioning ADS as a general data scheduling layer

## Relevance

Directly extends the RL rollout efficiency / allocation cluster (VIGOR, LEEPS, HIVE, GMTS, TrajVal, I-PPO) with a complementary semantic-cluster angle: where VIGOR uses reward variance and LEEPS uses explore-exploit prompt portfolios, ADS uses policy-capability boundary as the allocation signal. The cluster-level + sample-level hierarchy mirrors TrajVal's solvability-vs-learnability distinction but applied dynamically during training rather than as a static prior.

## My Thoughts

<!-- Add your own notes here -->
