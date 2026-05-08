---
title: "MMC: Iterative Refinement of VLM Reasoning via MCTS-based Multimodal Critique"
authors: ["Shuhang Liu", "Zhenrong Zhang", "Pengfei Hu", "Jiefeng Ma", "Jun Du", "Qing Wang", "Jianshu Zhang", "Quan Liu", "Jianqing Gao", "Feng Ma"]
date: 2025-04-15
arxiv_id: "2504.11009v1"
url: "https://arxiv.org/abs/2504.11009v1"
score: 0.75
topics: [multimodal models, vision language models, VLM, RL training, reward model]
status: unread
---

# MMC: Iterative Refinement of VLM Reasoning via MCTS-based Multimodal Critique

## Summary

MMC builds a multimodal actor-critic framework where a critic evaluates MCTS-generated VLM reasoning paths and provides corrective feedback for iterative refinement. MCTS explores reasoning paths from shared ancestor nodes to automatically construct preference data (correct vs. incorrect branches) for the critique dataset, eliminating costly manual annotation while training a critique model. Experiments across mainstream VLMs show significant gains on complex multimodal reasoning benchmarks.

## Key Contributions

- Multimodal actor-critic loop: actor generates MCTS-explored reasoning paths, critic evaluates and corrects them iteratively
- Automated critique dataset construction via MCTS path divergence (shared ancestor → correct/incorrect branch pairs)
- Eliminates manual annotation for multimodal preference data while preserving fine-grained step-level signals
- Broad applicability: evaluated across multiple mainstream VLMs with consistent improvements

## Relevance

Extends the VLM RL training thread (video VLMs from May 6, VAGEN/VISTA-R1 from May 5) to multimodal reasoning with an actor-critic + MCTS framing that bridges reward model construction and RL policy optimisation for VLMs.

## My Thoughts

<!-- Add your own notes here -->
