---
title: "Towards Hierarchical Multi-Step Reward Models for Enhanced Reasoning in Large Language Models"
authors: ["Teng Wang", "Zhangyi Jiang", "Zhenqi He", "Shenyang Tong", "Wenhan Yang", "Yanan Zheng", "Zeyu Li", "Zifan He", "Hailei Gong", "Zewen Ye", "Shengjie Ma", "Jianping Zhang"]
date: 2025-03-16
arxiv_id: "2503.13551"
url: "https://arxiv.org/abs/2503.13551"
score: 0.82
topics: [reward model, RL training, reinforcement learning, agentic RL]
status: unread
---

# Towards Hierarchical Multi-Step Reward Models for Enhanced Reasoning in Large Language Models

## Summary

HRM (Hierarchical Reward Model) addresses PRM reward hacking by evaluating both individual and consecutive reasoning steps at fine-grained and coarse-grained levels simultaneously, excelling at multi-step coherence where flawed steps are later corrected via self-reflection. Training data is generated via MCTS trajectories augmented with Hierarchical Node Compression (HNC), which merges consecutive steps to diversify the training distribution with controlled noise. HRM outperforms standard PRMs on PRM800K and shows stronger cross-domain generalization on MATH500 and GSM8K.

## Key Contributions

- Hierarchical dual-granularity evaluation: fine-grained (individual step) + coarse-grained (consecutive step pairs), capturing correction dynamics that flat PRMs miss
- Hierarchical Node Compression (HNC): merges consecutive reasoning steps within MCTS trees to generate richer, more diverse PRM training data with controlled noise
- Addresses self-reflection cases (flawed step followed by correction) that confound single-step PRMs
- Outperforms flat PRMs in both within-distribution (PRM800K) and cross-domain (MATH500, GSM8K) evaluation

## Relevance

HRM is the process-reward answer to DART's tree-based process advantage (Jul 11): where DART discovers tree-based advantage estimates for tool-insertion positions within long CoT, HRM builds a hierarchical reward model trained on MCTS trajectories to supervise those step-level decisions. Together they form a natural pairing: DART generates tree rollouts and needs process-level credit; HRM provides a tree-trained reward model that can score those rollouts at multiple granularities. HRM's two-level granularity also maps directly onto DART's cross-turn (TSR) and within-turn (DART) distinction from Jul 11.

## My Thoughts

<!-- Add your own notes here -->
