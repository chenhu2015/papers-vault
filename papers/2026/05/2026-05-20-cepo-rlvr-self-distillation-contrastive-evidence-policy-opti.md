---
title: "CEPO: RLVR Self-Distillation using Contrastive Evidence Policy Optimization"
authors: ["Ahmed Heakl", "Abdelrahman M. Shaker", "Youssef Mohamed", "Rania Elbadry", "Omar Fetouh", "Fahad Shahbaz Khan", "Salman Khan"]
date: 2026-05-20
arxiv_id: "2605.19436v1"
url: "http://arxiv.org/abs/2605.19436v1"
score: 0.85
topics: [RLVR, GRPO, reward model, RLAIF, multimodal, vision-language]
status: unread
---

# CEPO: RLVR Self-Distillation using Contrastive Evidence Policy Optimization

## Summary

CEPO sharpens RLVR credit assignment by asking a contrastive question at each token: does the correct answer favor this token while the wrong answer disfavors it? Only tokens satisfying both constraints are treated as genuine reasoning steps; the wrong-answer teacher is constructed from rejected rollouts already in the training batch, incurring zero extra sampling cost. CEPO achieves 43.43% / 60.56% average accuracy on five multimodal math benchmarks at 2B / 4B scale versus 41.17% / 57.43% for GRPO, with formal proof that credit sharpening vanishes exactly at filler token positions.

## Key Contributions

- Contrastive token-level credit: decisive reasoning steps defined as tokens that correct-answer teacher favors AND wrong-answer teacher disfavors simultaneously
- Zero-cost wrong-answer teacher: constructed from rejected rollouts already in the GRPO training batch
- Formal proof: CEPO inherits structural safety guarantees of prior SOTA while strictly sharpening credit at decisive tokens
- Empirical validation showing OPSD/SDPO information leakage, confirming theory; CEPO avoids this by not conditioning on the correct answer directly

## Relevance

Builds directly on the May 19 PAIR + SRaR + MoCA cluster of credit assignment papers. Where PAIR uses hidden states for step-level internal reward and SRaR uses rubric attribution, CEPO uses contrastive self-distillation at the token level—a distinct and theoretically grounded approach. The zero-cost wrong-answer teacher is an elegant engineering contribution applicable to any RLVR training loop.

## My Thoughts

<!-- Add your own notes here -->
