---
title: "Smaller Models are Natural Explorers for Policy-Level Diversity in GRPO"
authors: ["Yiming Ren", "Yiran Xu", "Zicheng Lin", "Chufan Shi", "Yukang Chen", "Dingdong Wang", "Tianhe Wu", "Junjie Wang", "Yujiu Yang", "Yu Qiao", "Ruihang Chu"]
date: 2026-06-16
arxiv_id: "2605.30789v2"
url: "http://arxiv.org/abs/2605.30789v2"
score: 0.76
topics: [reinforcement learning, GRPO, RL training, agentic RL]
status: unread
---

# Smaller Models are Natural Explorers for Policy-Level Diversity in GRPO

## Summary

S2L-PO exploits the finding that smaller models in the same family exhibit higher policy-level diversity (superior pass@k at higher sample counts despite lower mean accuracy), using them as fixed explorers to generate structurally diverse, temporally correlated rollouts for GRPO training of larger models. A progressive annealing strategy transitions from offline small-model rollouts to the large learner's own sampling mid-training, avoiding the capacity-ceiling drop while unlocking a higher final accuracy ceiling. S2L-PO achieves +8.8% on AIME 24 using a 1.7B explorer to guide an 8B model while reducing rollout compute compared to same-model sampling.

## Key Contributions

- Distinguishes policy-level diversity (temporally correlated, logically consistent trajectories) from token-level diversity (step-wise noise, incoherent trajectories) as a new axis for GRPO rollout quality
- Empirical finding: smaller same-family models have higher pass@k growth rate, making them natural high-diversity explorers for larger learners
- Progressive annealing: transitions offline small-model rollouts → learner's own sampling to avoid capacity-limit degradation mid-training
- Reduces rollout compute by offloading exploration to smaller, cheaper models

## Relevance

S2L-PO addresses a structural limitation of GRPO that DiScO (Jun 9) and ANCORA (Jun 15) also targeted — collapsed rollout diversity — but from a fundamentally different angle. DiScO adds diversity rewards over reasoning transitions; ANCORA uses self-play to grow the problem distribution; S2L-PO instead changes the source model for rollout generation. The three approaches are complementary and could be stacked: diverse source (S2L-PO) + diverse curriculum (ANCORA) + diversity-rewarded optimization (DiScO).

## My Thoughts

<!-- Add your own notes here -->
