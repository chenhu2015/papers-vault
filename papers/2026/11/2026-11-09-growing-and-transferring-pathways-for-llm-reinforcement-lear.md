---
title: "Growing and Transferring Pathways for LLM Reinforcement Learning"
authors: ["Haolin Tian", "Yikang Li", "Tonghan Wang"]
date: 2026-10-12
arxiv_id: "2610.16489"
url: "https://arxiv.org/abs/2610.16489"
score: 0.78
topics: [reinforcement learning, agentic RL, RL training, LLM agent]
status: unread
---

# Growing and Transferring Pathways for LLM Reinforcement Learning

## Summary

GrowRL freezes the pretrained backbone and adds independent causal-attention and feed-forward branches at each Transformer layer with zero-initialized output projections, isolating all RL updates into compact explicit pathways that can be transferred to structurally compatible target models or used for sequential multi-domain adaptation. After transfer, 10 target-side updates achieve performance close to 100 updates from scratch in every evaluated case, demonstrating immediate utility of the learned pathways. Competitive mathematical reasoning and OOD performance with far fewer trainable parameters across five backbones.

## Key Contributions

- Structural growth for RL: independent causal-attention + FFN branches with zero-initialized output projections preserve pretrained policy at init; RL updates only the added pathways
- Cross-model transfer: explicit pathway structure survives transfer to structurally compatible targets; 10 updates after transfer ≈ 100 from-scratch updates
- Sequential pathway transfer: architecture supports stacking additional domain-specific pathways (sequential multi-domain adaptation)
- Parameter-efficient RL: competitive performance with a small fraction of trainable parameters vs full fine-tuning

## Relevance

GrowRL directly addresses the continual/multi-domain RLVR thread (3+ entries): Beyond Forgetting addressed sequential forgetting, R^3 addressed cross-context replay, TAC (Nov 8) addressed multi-domain curriculum — GrowRL adds a structural approach to the same problem. Its explicit pathway design is complementary to TAC's bandit curriculum: TAC chooses which domains to train on; GrowRL provides parameter-isolated containers for each domain's learning. Together they suggest a principled multi-domain RLVR recipe: GrowRL pathway isolation + TAC gradient-transferability curriculum.

## My Thoughts

<!-- Add your own notes here -->
