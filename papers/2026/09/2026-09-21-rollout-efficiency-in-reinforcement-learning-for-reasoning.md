---
title: "Rollout Efficiency in Reinforcement Learning for Reasoning Large Language Models: A Taxonomy and Future Directions"
authors: ["Niloofar Gholipour", "Marcos Assuncao", "Gursimran Singh", "Timothy Yu", "Rajkumar Buyya", "Julien Gascon-Samson", "Zhenan Fan", "Yong Zhang", "Xiaojie Xu", "Yaqiang Yao", "Xiaolong Bai"]
date: 2026-09-21
arxiv_id: "2609.25463"
url: "https://arxiv.org/abs/2609.25463"
score: 0.80
topics: [RL training, GRPO, agentic RL, PPO]
status: unread
---

# Rollout Efficiency in Reinforcement Learning for Reasoning Large Language Models: A Taxonomy and Future Directions

## Summary

This survey taxonomizes techniques for reducing rollout cost in reasoning-oriented LLM RL, where trajectory generation accounts for the majority of training compute in methods like GRPO. It classifies approaches from both mechanism (scheduling, batching, speculative decoding, early stopping) and bottleneck perspectives, analyzing how different technique families address distinct inefficiency sources and identifying synergies and conflicts between them. The survey highlights gaps in standardized efficiency evaluation and outlines open challenges for making RL training of reasoning LLMs practical at scale.

## Key Contributions

- Systematic taxonomy of rollout efficiency techniques for reasoning RL, organized by mechanism and bottleneck type
- Analysis of technique family interactions: which combinations are synergistic vs. conflicting
- Identification of evaluation gaps in how efficiency gains are reported across papers
- Future directions for rollout efficiency in reasoning-oriented RL at scale

## Relevance

With GRPO being the core training method in most recent papers in the digest (GRAFT, SALT, ProCredit, EPIG-Tree, EAPO, GVPO), understanding rollout efficiency directly addresses the practical cost of running these methods. This survey provides a map of the space that helps contextualize where methods like EPIG-Tree (compute-optimal branching) and GRAFT (trajectory graph rollout reuse) fit.

## My Thoughts

<!-- Add your own notes here -->
