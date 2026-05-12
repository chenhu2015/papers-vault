---
title: "Exploration-Driven Optimization for Test-Time Large Language Model Reasoning"
authors: ["Changhao Li", "Yuchen Zhuang", "Chenxiao Gao", "Haotian Sun", "Rushi Qiang", "Chao Zhang", "Bo Dai"]
date: 2026-05-11
arxiv_id: "2605.09853v1"
url: "http://arxiv.org/abs/2605.09853v1"
score: 0.85
topics: [GRPO, RLHF, RL training, reinforcement learning, agentic RL]
status: unread
---

# Exploration-Driven Optimization for Test-Time Large Language Model Reasoning

## Summary

EDO addresses the fundamental tension between inference-time scaling (which benefits from diverse, flat distributions) and RL post-training (which sharpens distributions), by integrating reward-biasing exploration objectives into GRPO and iDPO as ED-GRPO and ED-iDPO. Both variants improve solution diversity and reasoning accuracy—+1.0–1.3% in-distribution and +1.5% on five OOD tasks—while preserving model entropy to prevent over-optimization collapse, making EDO a practical framework for balancing exploration and exploitation during LLM RL training.

## Key Contributions

- Formal identification of the exploration-exploitation tension in RL post-training: RL sharpens distributions, hurting inference-time diversity
- ED-GRPO and ED-iDPO: reward-biasing exploration objectives integrated into standard RL training loops
- Consistent gains on in-distribution (+1.0–1.3%) and OOD (+1.5% avg across 5 benchmarks) reasoning tasks
- Entropy preservation mechanism that prevents over-optimization collapse and stabilizes RL training dynamics

## Relevance

Addresses the over-optimization / distribution collapse thread from the May 11 reward hacking digest, but from the training-time exploration angle rather than the reward model perspective. Directly relevant to GRPO and RLHF interests; complements the exploration strategies covered earlier in the month by applying them specifically to the post-training distribution sharpening problem.

## My Thoughts

<!-- Add your own notes here -->
