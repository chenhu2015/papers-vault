---
title: "d-TreeRPO: Towards More Reliable Policy Optimization for Diffusion Language Models"
authors: ["d-TreeRPO authors"]
date: 2026-10-19
arxiv_id: "2512.09675v3"
url: "http://arxiv.org/abs/2512.09675v3"
score: 0.80
topics: [GRPO, RL training, reward model, step credit]
status: unread
---

# d-TreeRPO: Towards More Reliable Policy Optimization for Diffusion Language Models

## Summary

d-TreeRPO addresses two dLLM RL reliability bottlenecks — reward sparsity and intractable probability estimates — via tree-structured rollouts with bottom-up advantage computation from verifiable outcome rewards, providing fine-grained step-wise signals. A theoretical proof shows that higher prediction confidence minimises the single-step estimate gap to the unbiased expectation, motivating a time-scheduled self-distillation loss that improves probability estimation in later training stages; results show +86.2% on Sudoku and +51.6% on Countdown over the base model.

## Key Contributions

- Tree-structured rollouts for dLLMs with bottom-up advantage from verifiable terminal rewards
- Theoretical analysis: prediction confidence bounds the gap between single-step estimate and unbiased expectation
- Time-scheduled self-distillation loss to increase confidence and accuracy in later training
- Strong empirical gains: +86.2% Sudoku, +51.6% Countdown, +4.5% GSM8K, +5.3% Math500

## Relevance

Seventh paper overall in the diffusion LM RL thread; bridges step-credit cluster and diffusion LM RL — tree-structured rollouts for dLLMs is structurally analogous to PACT's trajectory-segment approach and d-TreeRPO's analysis of probability estimation gap is a foundational contribution for the whole dLLM RL field.

## My Thoughts

<!-- Add your own notes here -->
