---
title: "Learning at the Right Pace: Adaptive Data Scheduling Improves LLM Reinforcement Learning"
authors: ["Zicheng Xu", "Ruixuan Zhang", "Yu-Neng Chuang", "Xiuyi Lou", "Hoang Anh Duy Le", "Oren Gal", "Alexander S. Szalay", "Zhaozhuo Xu", "Guanchu Wang", "Vladimir Braverman"]
date: 2026-07-09
arxiv_id: "2606.22305v1"
url: "http://arxiv.org/abs/2606.22305v1"
score: 0.80
topics: [RL training, GRPO, reinforcement learning, RLHF]
status: unread
---

# Learning at the Right Pace: Adaptive Data Scheduling Improves LLM Reinforcement Learning

## Summary

Adaptive Data Scheduling (ADS) replaces uniform data sampling in GRPO with a dual-level framework: at the cluster level it maintains an adaptive inter-cluster distribution over semantic groupings to consolidate current training progress, and at the sample level it selects policy-boundary examples within each cluster to maximize informative relative advantages. Across three LLMs and seven reasoning benchmarks, ADS improves average accuracy by 5.2% over GRPO and generalises across different RL objective designs.

## Key Contributions

- Dual-level curriculum: inter-cluster adaptive distribution (exploits semantic structure) + intra-cluster policy-boundary sample selection (exploits capability boundary)
- Policy-boundary selection identifies samples where the model is near its current performance edge, generating maximally informative group-relative advantages
- Demonstrates 5.2% average accuracy gain over GRPO across three LLMs (7B–70B scale) and seven benchmarks
- Validated as a general data scheduling strategy: compatible with different RL objective designs beyond GRPO

## Relevance

ADS complements AdaPrefix-GRPO (Jul 09) as a second member of an emerging adaptive curriculum triad for GRPO post-training. Where AdaPrefix intervenes at the per-problem level (adjusting difficulty via prefix), ADS operates at the data distribution level (adjusting which samples to draw). Together with DUMP's UCB-based distribution scheduling, these three papers establish adaptive curriculum as a key training-efficiency dimension in LLM RL post-training — orthogonal to the credit-assignment (GRPO-λ, EGSPO) and mode-separation (AutoTool, TEMPO) threads already in the vault.

## My Thoughts

<!-- Add your own notes here -->
