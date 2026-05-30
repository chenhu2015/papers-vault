---
title: "Label-Free Reinforcement Learning via Cross-Model Entropy"
authors: ["Matt Gorbett", "Hossein Shirazi"]
date: 2026-05-27
arxiv_id: "2605.29009"
url: "http://arxiv.org/abs/2605.29009v1"
score: 0.83
topics: [RLAIF, reward model, GRPO, RL training]
status: unread
---

# Label-Free Reinforcement Learning via Cross-Model Entropy

## Summary

Cross-Model Entropy (CME) uses the mean log-likelihood of a generator's response under a separate verifier model as a continuous, training-free reward signal for GRPO, extending label-free RL to open-ended instruction following where self-referential signals (majority voting, token entropy) fail because they can reinforce the generator's own errors. Integrated into GRPO with no other changes, CME achieves tie-adjusted win rates of 52.5–71.4% over untrained base models across four model families on UltraFeedback/AlpacaEval 2.0.

## Key Contributions

- CME = mean log-likelihood of generator response under independent verifier; continuous and training-free
- Cannot be gamed via self-consistency since verifier is independent of generator
- Extends label-free RL to open-ended instruction following (beyond math/code with ground-truth verifiers)
- Consistent wins across Qwen, Llama, Gemma, OLMo in pretrained, SFT, and instruction-tuned regimes

## Relevance

Complements the RLAIF/reward-free thread (SARL, Cancellation Hypothesis from May 26) with a novel cross-model entropy reward that avoids self-reinforcing errors — a clean conceptual advance in label-free RL.

## My Thoughts

<!-- Add your own notes here -->
