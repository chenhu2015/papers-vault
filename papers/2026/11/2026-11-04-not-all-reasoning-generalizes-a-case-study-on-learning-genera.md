---
title: "Not All Reasoning Generalizes: A Case Study on Learning Generalizable Reasoning Strategies in RLVR"
authors: ["Ziqi Pang", "Yu-Xiong Wang"]
date: 2026-11-02
arxiv_id: "2611.03627v1"
url: "http://arxiv.org/abs/2611.03627v1"
score: 0.78
topics: [reinforcement learning, agentic RL, GRPO, reward model, RLHF, RLAIF]
status: unread
---

# Not All Reasoning Generalizes: A Case Study on Learning Generalizable Reasoning Strategies in RLVR

## Summary

This paper exposes a subtle RLVR failure mode via a controllable equation-solving framework: RLVR achieves high in-distribution accuracy with structured step-by-step reasoning, but under OOD shifts (more solutions, longer inputs) the model abandons derivation and collapses to brute-force enumeration. The failure is neither from incapable base models nor reward hacking — rather, outcome-only RLVR implicitly credits effective reasoning strategies, which can be fragile. An indirect fix — co-training with bijective inversion tasks — restores correct strategy and accuracy under OOD shifts, suggesting that curriculum diversity matters for RLVR generalization.

## Key Contributions

- Controllable framework: equation-solving with non-bijective string functions makes reasoning strategies observable and OOD shifts precisely definable
- Identifies a new RLVR failure mode: in-distribution structured reasoning collapses to brute-force under OOD — distinct from entropy collapse or reward hacking
- Theoretical analysis: outcome-only RLVR implicitly credits effective reasoning strategies through advantage weighting, which explains both success and fragility
- Fix: co-training with bijective inversion tasks (not uniformly harder, further from OOD evaluation) makes derivation more certain and restores OOD accuracy

## Relevance

Extends the GRPO training dynamics thread (No Free Lunch, Sparse but Critical, PAEC, UCAS, QAE) with a generalization angle: prior entries analyzed statistical behavior during training, this paper probes what happens when the trained model faces distribution shift. The implicit strategy-crediting mechanism connects to the advantage estimation debate in the thread.

## My Thoughts

<!-- Add your own notes here -->
