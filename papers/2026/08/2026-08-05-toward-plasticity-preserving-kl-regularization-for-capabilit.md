---
title: "Toward Plasticity-Preserving KL Regularization for Capability Retention in LLM Reinforcement Learning"
authors: ["Li Wang", "Xiaodong Lu", "Xiaohan Wang", "Jiajun Chai", "Wei Lin", "Tianhao Peng", "Guojun Yin"]
date: 2026-08-05
arxiv_id: "2608.01743"
url: "https://arxiv.org/abs/2608.01743"
score: 0.77
topics: [RLHF, RLAIF, RL training, PPO, reward model]
status: unread
---

# Toward Plasticity-Preserving KL Regularization for Capability Retention in LLM Reinforcement Learning

## Summary

CoKL (Correctness-Conditioned KL regularization) identifies that standard full-policy KL constraints in LLM RL can inadvertently suppress plasticity by anchoring incorrect outputs and inducing an "optimal correctness gap" when the reference policy is imperfect. CoKL narrows the preservation constraint from the full output distribution to correctness-conditioned response distributions only, decoupling the total probability assigned to correct responses from their relative allocation among reference-supported correct outputs. Experiments in controlled multi-solution environments and continual post-training settings across multiple model scales show CoKL achieves a better target-task improvement / prior-capability retention balance than full-policy forward or reverse KL.

## Key Contributions

- Identification of the "optimal correctness gap": full-policy KL regularization (both forward and reverse) introduces a fundamental lower bound on correctness loss when the reference policy is imperfect
- CoKL: narrows KL constraint to correctness-conditioned response distributions, freeing the policy to update incorrect outputs without anchoring them to an imperfect reference
- Practical finite-group training objective for RL-based LLM post-training derived from CoKL
- Multi-scale experiments showing improved target-task improvement + prior-capability retention balance

## Relevance

CoKL addresses a previously uncharacterized failure mode of KL regularization in RLHF/RLAIF: the constraint is too broad, applying to incorrect outputs where it actively harms learning, and it creates a correctness gap when the reference model is not perfect on the training distribution. This connects directly to the GRPO advantage normalization thread (the same on-policy optimization structure that SFT Conflicts/RL Coexists shows produces near-orthogonal multi-task gradients also interacts with KL regularization in ways that prior work has not analyzed). CoKL is the first vault paper to formally separate the KL regularization objective into correctness-conditioned components.

## My Thoughts

<!-- Add your own notes here -->
