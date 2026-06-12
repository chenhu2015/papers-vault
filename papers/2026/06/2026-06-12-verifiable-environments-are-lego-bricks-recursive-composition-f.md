---
title: "Verifiable Environments Are LEGO Bricks: Recursive Composition for Reasoning Generalization"
authors: ["Hao Xiang", "Qiaoyu Tang", "Le Yu", "Yaojie Lu", "Xianpei Han", "Ben He", "Le Sun", "Bowen Yu", "Peng Wang", "Hongyu Lin", "Dayiheng Liu"]
date: 2026-06-10
arxiv_id: "2606.12373v1"
url: "http://arxiv.org/abs/2606.12373v1"
score: 0.79
topics: [reinforcement learning, agentic RL, RL training]
status: unread
---

# Verifiable Environments Are LEGO Bricks: Recursive Composition for Reasoning Generalization

## Summary

RACES reframes the verifiable environment scaling problem: instead of manually constructing more environments, it recursively composes existing ones via type-compatible fusion (SEQUENTIAL, PARALLEL, SORT, SELECT operators). Starting from 300 individual environments it generates exponentially many composite environments that induce diverse reasoning patterns. RL training on these composites improves DeepSeek-R1-Distill-Qwen-14B by +3.1 points on six unseen benchmarks, matching the coverage of 300 individual environments with only 50 base environments.

## Key Contributions

- **Composable environment abstraction**: verifiable environments modeled as typed functions; two environments are composable when codomain of one matches domain of another
- **Four composition operators**: SEQUENTIAL, PARALLEL, SORT, SELECT create diverse reasoning patterns from a small base set
- **Strong generalization results**: +3.1 avg improvement on six unseen benchmarks; 50 base environments match 300 individual environments — a 6x efficiency gain
- **Scalable without manual construction**: the recursive framework generates exponentially many training environments with linear growth in base environments

## Relevance

Directly extends the SUPERNOVA/START (Jun 6-7) generalization thread: where SUPERNOVA showed that data curation from natural instructions generalizes RLVR, RACES shows that compositionally diverse training environments do the same. The type-compatible composition idea is a principled answer to the question of why some verifiable reward signals generalize better than others — compositional structure induces compositional reasoning.

## My Thoughts

<!-- Add your own notes here -->
