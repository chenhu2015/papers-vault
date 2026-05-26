---
title: "LC-ERD: Mining Latent Logic for Self-Evolving Reasoning via Consistency-Regulated Reward Decomposition"
authors: ["Yanyu Chen", "Jiyue Jiang", "Dianzhi Yu", "Zheng Wu", "Jiahong Liu", "Jiaming Han", "Xiao Guo", "Jinhu Qi", "Yu Li", "Yifei Zhang", "Irwin King"]
date: 2026-05-26
arxiv_id: "2605.24005v1"
url: "http://arxiv.org/abs/2605.24005v1"
score: 0.82
topics: [GRPO, RL training, RLAIF, reward model, agentic RL]
status: unread
---

# LC-ERD: Mining Latent Logic for Self-Evolving Reasoning via Consistency-Regulated Reward Decomposition

## Summary

LC-ERD addresses three failures of self-rewarding GRPO — label noise from mimetic bias, coarse-grained supervision from sparse global rewards, and distributional collapse — by mining latent logic via Variational Logic Potential aggregation that denoises the reward manifold from a model's own internal expertise. A Multi-Agent Value Decomposition protocol using the IGM principle then quantifies individual step utility without any external labels, uncovering trade-offs between logic consistency and accuracy and identifying high-value reasoning patterns missed by standard rewards.

## Key Contributions

- Identifies three failure modes in self-alignment RL: label noise (mimetic bias creates "correctness illusion"), coarse supervision (GRPO treats reasoning chains as monolithic), and distributional collapse
- Variational Logic Potential: aggregates consensus from model's Latent Logic Expertise to denoise the reward manifold and filter statistically likely but logically wrong reasoning
- Multi-Agent Value Decomposition (IGM principle): decomposes group reward into per-step utility without external labels
- Self-evolving path uncovers logic consistency vs. accuracy trade-offs and identifies high-value reasoning patterns

## Relevance

Directly extends the self-rewarding/RLAIF thread (MISE, SD-Zero from May 24-25) with a unique framing around latent logic structure, tackling the label noise and distributional collapse problems that make GRPO self-rewarding unstable in practice.

## My Thoughts

<!-- Add your own notes here -->
