---
title: "CLORE: Content-Level Optimization for Reasoning Efficiency"
authors: ["Yuyang Wu", "Qiyao Xue", "Guanxing Lu", "Weichen Liu", "Zihan Wang", "Manling Li", "Olexandr Isayev"]
date: 2026-05-23
arxiv_id: "2605.22211v1"
url: "http://arxiv.org/abs/2605.22211v1"
score: 0.79
topics: [GRPO, RLHF, RL training, reinforcement learning, agentic RL]
status: unread
---

# CLORE: Content-Level Optimization for Reasoning Efficiency

## Summary

CLORE addresses reasoning inefficiency in RL-trained LLMs at the content level rather than via length penalties: an augmentation model deletes repetitive segments, irrelevant content, and post-answer exploration from correct on-policy rollouts, and the resulting edited–original pairs are optimized with a reference-free DPO objective alongside standard policy-gradient training. By restricting edits to correct trajectories and local deletions, CLORE avoids off-policy distribution shift. Experiments on DeepSeek-R1-Distill-Qwen-7B and Qwen2.5-Math-7B across five benchmarks show improved accuracy–efficiency trade-off, compatible with GRPO, DAPO, and ThinkPrune.

## Key Contributions

- Content-level supervision as a complementary axis to length-level control for reasoning efficiency
- Augmentation model that performs local deletion of repetition, illegible content, and post-answer drift from correct rollouts only
- Reference-free DPO auxiliary objective alongside standard policy gradient — no separate reward model needed
- Plug-in compatibility: works alongside GRPO, DAPO, Training Efficient, and ThinkPrune

## Relevance

Fills a gap in the reasoning-efficiency thread (target of the repeated "reasoning budget RL" searches): rather than controlling token count via reward shaping, it directly edits the content of reasoning traces. Complements May 22's DelTA and CEPO (token-level credit) with an orthogonal content-quality angle.

## My Thoughts

<!-- Add your own notes here -->
