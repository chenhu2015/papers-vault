---
title: "Post-Training Language Models for Gold-Medal Performance in Coding Competitions"
authors: ["Aleksander Ficek", "Sean Narenthiran", "Mehrzad Samadi", "Somshubra Majumdar", "Boris Ginsburg"]
date: 2026-09-05
arxiv_id: "2609.02849v1"
url: "http://arxiv.org/abs/2609.02849v1"
score: 0.80
topics: [RL training, reinforcement learning, reward model, RLHF]
status: unread
---

# Post-Training Language Models for Gold-Medal Performance in Coding Competitions

## Summary

Nemotron-3 (Nano-CC 30B-A3B and Ultra-CC 550B-A55B) is trained with a pipeline combining 22,000 curated competitive programming problems, synthetic reasoning traces, SFT, and RL, achieving gold-medal performance at IOI 2025/2026. GenCorrect, a feedback-driven test-time compute strategy, iteratively generates, evaluates, and refines diverse solutions, pushing Nano-CC from 291 points post-training to 468 (above the gold threshold of 438.3). In live IOI 2026 evaluation under the same time, internet-access, and submission constraints as human contestants, the system scores 535.4/600 — the first AI to outscore the highest-scoring human contestant on an IOI problem set.

## Key Contributions

- End-to-end specialization pipeline: 22K problem curation → synthetic reasoning traces → SFT → RL, demonstrating the SFT-then-RL ordering validated by Demystifying RL Post-Training
- GenCorrect: inference-time compute strategy that iteratively generates, evaluates, and refines diverse solutions — structurally similar to MCTS but using code execution feedback as the verification signal
- Nemotron-3-Nano-CC (30B-A3B): improves from 130 → 291 (post-training) → 468 (+ GenCorrect) on IOI 2025; above gold threshold of 438.3
- First AI to outscore the highest-scoring human contestant at IOI (535.4/600 vs. top human 498.27 at IOI 2026)

## Relevance

The SFT-then-RL pipeline confirms the base model prior finding from Demystifying RL Post-Training: RL success requires the base model to already place probability on correct behaviors, which the SFT phase guarantees. GenCorrect provides a concrete instantiation of the verifiable-reward RL principle (LLMs-as-Jury Sep 04: jury error floor is near zero on code/math) — the error floor is indeed near zero when execution-based test cases are the reward signal, which is why iterative self-refinement against code tests works without a trained reward model.

## My Thoughts

<!-- Add your own notes here -->
