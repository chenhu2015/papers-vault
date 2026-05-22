---
title: "DelTA: Discriminative Token Credit Assignment for Reinforcement Learning from Verifiable Rewards"
authors: ["Kaiyi Zhang", "Wei Wu", "Yankai Lin"]
date: 2026-05-22
arxiv_id: "2605.21467"
url: "https://arxiv.org/abs/2605.21467"
score: 0.86
topics: [RLVR, reward model, agentic RL, PPO]
status: unread
---

# DelTA: Discriminative Token Credit Assignment for Reinforcement Learning from Verifiable Rewards

## Summary

DelTA introduces a discriminative-view analysis of RLVR policy-gradient updates, showing that standard updates implicitly act as linear discriminators over token-gradient vectors using advantage-weighted centroids that can be dominated by high-frequency formatting tokens rather than semantically discriminative ones. The method estimates per-token coefficients to amplify side-specific gradient directions and downweight shared patterns, reweighting the self-normalized RLVR surrogate to reshape the effective update direction. Evaluated on 7 mathematical benchmarks, improving over strongest same-scale baselines by 3.26 and 2.62 average points on Qwen3-8B-Base and Qwen3-14B-Base respectively.

## Key Contributions

- Discriminative-view reframing of RLVR: standard policy-gradient updates act as linear discriminators over token-gradient vectors via advantage-weighted centroids
- Identifies a failure mode: shared high-frequency formatting tokens dilute sparse but semantically discriminative gradient directions
- DelTA: per-token coefficient estimation to amplify side-specific contrastive directions and downweight shared/weakly-discriminative ones via reweighted RLVR surrogate
- Generalizes across code generation, different backbone models, and out-of-domain evaluations

## Relevance

Extends the dense credit assignment thread from recent digests (CEPO May 20, SRaR/MoCA May 19) with a novel theoretical framing: rather than modifying the reward signal, DelTA reshapes the gradient update itself by making the discriminative structure explicit. Complements CEPO's contrastive-token-level approach with a gradient-space analysis.

## My Thoughts

<!-- Add your own notes here -->
