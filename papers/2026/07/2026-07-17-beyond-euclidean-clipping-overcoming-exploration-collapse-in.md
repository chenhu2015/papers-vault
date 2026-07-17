---
title: "Beyond Euclidean Clipping: Overcoming Exploration Collapse in LLM RL via Riemannian Isometric Policy Optimization"
authors: ["Zhicheng Cai", "Xinyuan Guo", "Hanlin Wu", "Mingxuan Wang", "Wei-Ying Ma", "Ya-Qin Zhang", "Hao Zhou"]
date: 2026-07-17
arxiv_id: "2607.10169v1"
url: "http://arxiv.org/abs/2607.10169v1"
score: 0.90
topics: [RL training, PPO, GRPO, reinforcement learning]
status: unread
---

# Beyond Euclidean Clipping: Overcoming Exploration Collapse in LLM RL via Riemannian Isometric Policy Optimization

## Summary

Identifies that PPO-Clip implicitly measures policy discrepancy with Euclidean distance, which is geometrically inconsistent with the intrinsic Riemannian manifold structure of policy distributions — causing overly conservative updates in low-probability regions and aggressive updates in high-probability regions, collapsing exploration. RIPO replaces Euclidean clipping with isometric updates on the Riemannian manifold, guaranteeing balanced exploration-exploitation and a favorable bias-variance trade-off. Achieves up to 60% improvement over GRPO on AIME24 across seven competition-level benchmarks.

## Key Contributions

- Identifies the fundamental geometric flaw in PPO-Clip: Euclidean metric is theoretically inconsistent with the Riemannian manifold on which policy distributions live
- Proposes RIPO (Riemannian Isometric Policy Optimization) that guarantees isometric updates on the policy manifold
- Shows RIPO achieves a favorable bias-variance trade-off that stabilizes optimization without exploration collapse
- Up to 60% improvement over GRPO on AIME24; SOTA across seven competition-level benchmarks

## Relevance

The vault has tracked GRPO as the dominant RL training algorithm across many papers (RSPO, ARMOR, DISA, SCI-PRM, ViCrit) — RIPO identifies a fundamental mathematical flaw in PPO-Clip (and by extension GRPO) and proposes a principled geometric fix. This is the most foundational RL training optimization paper in the vault to date: it operates at the algorithm level rather than the data/curriculum/reward level.

## My Thoughts

<!-- Add your own notes here -->
