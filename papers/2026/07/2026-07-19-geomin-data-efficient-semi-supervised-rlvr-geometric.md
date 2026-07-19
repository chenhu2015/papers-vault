---
title: "GeoMin: Data-Efficient Semi-Supervised RLVR via Geometric Distribution Modeling"
authors: ["Guangcheng Zhu", "Shenzhi Yang", "Haobo Wang", "Xing Zheng", "Yingfan MA", "Xuening Feng", "Zhongqi Chen", "Kai Tang", "Zhengqing Zang", "Bowen Song", "Weiqiang Wang", "Gang Chen"]
date: 2026-06-03
arxiv_id: "2606.04516"
url: "https://arxiv.org/abs/2606.04516"
score: 0.81
topics: [RL training, agentic RL, GRPO, RLHF, RLAIF]
status: unread
---

# GeoMin: Data-Efficient Semi-Supervised RLVR via Geometric Distribution Modeling

## Summary

GeoMin addresses the data efficiency bottleneck in semi-supervised RLVR, where a small labeled set guides training on unlabeled data but existing methods discard most valuable instances via coarse performance heuristics. The approach models global feature distributions on labeled data to decode the structural discrepancy between correct and incorrect rollouts, establishing a geometric prior to assess self-reward reliability on unlabeled data. GeoMin outperforms the strongest semi-supervised baselines by +4.1% and matches fully supervised models using only 10% of the annotations.

## Key Contributions

- Semi-supervised RLVR framing: articulates the annotation cost bottleneck in RLVR and the failure mode of existing semi-supervised methods (coarse heuristics leave most unlabeled data underutilized)
- Geometric distribution modeling: learns global feature distributions over labeled correct/incorrect rollouts to characterize structural separability
- Self-reward reliability prior: uses the geometric model to score unlabeled rollout quality without ground-truth labels; high-reliability instances receive standard self-reward, low-reliability instances are filtered or down-weighted
- 10% annotation efficiency: matches fully supervised RLVR performance at 10% annotation cost; +4.1% over semi-supervised baselines

## Relevance

Directly answers the queued search from Jul 18 for data quality/selection approaches in RLVR. GeoMin complements the vault's existing data efficiency thread (RL-ZVP: zero-variance prompts, IGRPO: information gain branch allocation, Prune-OPD: token truncation) with a new axis: how to assess the reliability of self-generated reward signals on unlabeled data. The geometric structural discrepancy measure is conceptually related to the Paradox of Outcome Optimization's Semantic Coverage Measure (η) — both identify when training signals are trustworthy — but from opposite directions: η asks whether outcome supervision covers the right semantic space; GeoMin asks whether a specific rollout's self-reward is reliable.

## My Thoughts

<!-- Add your own notes here -->
