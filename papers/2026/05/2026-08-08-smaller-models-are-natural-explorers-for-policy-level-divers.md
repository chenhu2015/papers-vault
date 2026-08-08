---
title: "Smaller Models are Natural Explorers for Policy-Level Diversity in GRPO"
authors: ["Yiran Xu", "Yiming Ren", "Zicheng Lin", "Chufan Shi", "Yukang Chen", "Dingdong Wang", "Tianhe Wu", "Junjie Wang", "Yujiu Yang", "Yu Qiao", "Ruihang Chu"]
date: 2026-08-08
arxiv_id: "2605.30789v3"
url: "http://arxiv.org/abs/2605.30789v3"
score: 0.78
topics: [GRPO, agentic RL, RL training]
status: unread
---

# Smaller Models are Natural Explorers for Policy-Level Diversity in GRPO

## Summary

S2L-PO identifies that smaller models exhibit higher policy-level diversity than larger models — evidenced by superior pass@k relative to sample count — because their trajectory variation is temporally correlated and logically coherent rather than token-level noise. It leverages a fixed small model as a natural explorer to generate GRPO rollouts for a larger learner model, with progressive annealing transitioning from offline small-model rollouts to the large model's own sampling to avoid capacity-limit-induced performance drops mid-training.

## Key Contributions

- Identifies policy-level diversity (temporally correlated, coherent trajectory variation) as distinct from token-level noise in GRPO rollouts
- Small models naturally exhibit higher pass@k diversity relative to large models in the same family
- S2L-PO framework: fixed small model as explorer, large model as learner, jointly training via GRPO
- Progressive annealing from offline small-model rollouts to large learner's own sampling avoids mid-training drops; achieves +8.8% on AIME 24 with reduced rollout compute

## Relevance

S2L-PO directly extends the agentic RL exploration taxonomy from a new angle: where DPEPO (Aug 7) uses multi-environment parallel interaction and explicit diversity rewards, S2L-PO uses model-size hierarchy as an intrinsic source of policy diversity — no new environments needed. The small-model explorer role is structurally analogous to a curriculum provider: it supplies diverse, coherent exploration signals for the larger learner. The progressive annealing strategy addresses the same exploitation-exploration balance that DPEPO's diversity rewards target, but via a sampling schedule rather than an explicit reward term. Together with DPEPO and RAPO, S2L-PO forms a three-way taxonomy of diversity provision mechanisms: explicit reward (DPEPO), retrieved trajectory injection (RAPO), and model-size-induced exploration (S2L-PO).

## My Thoughts

<!-- Add your own notes here -->
