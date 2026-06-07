---
title: "SUPERNOVA: Eliciting General Reasoning in LLMs with Reinforcement Learning on Natural Instructions"
authors: ["Ashima Suvarna", "Kendrick Phan", "Mehrab Beikzadeh", "Hritik Bansal", "Saadia Gabriel"]
date: 2026-06-07
arxiv_id: "2604.08477v2"
url: "http://arxiv.org/abs/2604.08477v2"
score: 0.84
topics: [agentic RL, RL training, reinforcement learning, GRPO, RLHF]
status: unread
---

# SUPERNOVA: Eliciting General Reasoning in LLMs with Reinforcement Learning on Natural Instructions

## Summary

SUPERNOVA introduces a framework for curating RLVR training data from natural instruction datasets, addressing the limitation of RLVR being confined to STEM domains. Through 100+ controlled experiments, it identifies source task selection as the dominant factor for downstream reasoning performance — beating both task mixing strategies and synthetic interventions. Training Qwen3-0.6B on the 25K-instance SUPERNOVA dataset yields a 64.4pp gain on BigBench Extra Hard, and these gains generalise to unseen benchmarks, larger model scales, and newer model families.

## Key Contributions

- 100+ controlled RL experiments identifying source task selection as the primary driver of RLVR downstream performance (over task mixing and synthetic augmentation)
- SUPERNOVA dataset: 25K instances curated from natural instruction datasets using target-task-specific selection strategy
- 64.4pp gain on BBEH for Qwen3-0.6B; gains generalise to unseen benchmarks, larger scales, and newer model families
- Finding that task-specific selection outperforms average-performance-based selection and that synthetic interventions do not improve reasoning

## Relevance

Directly extends the OOD generalization thread opened by June 6's START paper (RLVR gains don't transfer to general QA) — SUPERNOVA is a constructive answer showing that with careful data curation from non-STEM sources, RLVR *can* generalise to general reasoning. Complements the curriculum/data selection theme and the data scarcity angle for LLM RL.

## My Thoughts

<!-- Add your own notes here -->
