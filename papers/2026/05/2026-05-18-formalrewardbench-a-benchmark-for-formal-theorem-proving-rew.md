---
title: "FormalRewardBench: A Benchmark for Formal Theorem Proving Reward Models"
authors: ["Zeynel A. Uluşan", "Burak S. Akbudak", "Can S. Erer", "Gözde Gül Şahin"]
date: 2026-05-11
arxiv_id: "2605.10141v1"
url: "http://arxiv.org/abs/2605.10141v1"
score: 0.82
topics: [reward model, RLVR, RL training, RLAIF]
status: unread
---

# FormalRewardBench: A Benchmark for Formal Theorem Proving Reward Models

## Summary

FormalRewardBench is the first benchmark for evaluating reward models in formal theorem proving (Lean 4), motivated by the sparse credit-assignment problem in RLVR for proof search — binary correctness signals leave partial proof progress unrewarded. The benchmark uses 250 preference pairs with five expert-curated error injection strategies to test whether reward models can distinguish correct from near-correct proofs. Frontier LLMs (59.8%) substantially outperform specialized theorem-proving models (24.4%), revealing that proof-generation ability does not transfer to proof evaluation.

## Key Contributions

- First benchmark specifically for reward models in formal theorem proving (Lean 4 focus)
- Five error injection strategies: forced mistakes, minimal single-point variations, verbose incorrect proofs, natural language justification, Python code injection
- Key finding: theorem-proving ability ≠ proof evaluation ability — specialized provers are the worst evaluators
- Directly motivated by sparse credit assignment in RLVR: binary signals cannot reward partial progress in difficult proofs

## Relevance

Connects the reward model reliability thread (interest profile: reward model, RLVR) to formal reasoning, a domain that has never appeared in 17 days of prior digests. The sparse credit assignment finding directly parallels the process reward model research (SWE-Shepherd, May 9; verifiable process rewards, May 12), and the theorem proving angle opens a new adjacent research thread.

## My Thoughts

<!-- Add your own notes here -->
