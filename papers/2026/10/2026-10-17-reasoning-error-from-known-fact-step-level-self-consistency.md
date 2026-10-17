---
title: "Reasoning Error from Known Fact: Step-Level Self-Consistency Group Relative Policy Optimization for LLMs"
authors: ["Xiaomeng Hu", "Jiaqi Hu", "Hao Chen", "Qi Zhang", "Zhanming Shen", "Wentao Ye", "Junbo Zhao"]
date: 2026-07-21
arxiv_id: "2607.18915v2"
url: "http://arxiv.org/abs/2607.18915v2"
score: 0.82
topics: [reinforcement learning, GRPO, reward model, RL training, agentic RL]
status: unread
---

# Reasoning Error from Known Fact: Step-Level Self-Consistency Group Relative Policy Optimization for LLMs

## Summary

SSC-GRPO targets Context-Sensitive Factual Hallucinations — cases where the model knows the relevant fact but contradicts it due to contextual interference during long reasoning. Step-level rewards are assigned by computing cross-rollout self-consistency scores for individual reasoning steps, providing a cheap and fine-grained signal without a separate critic or PRM. The method achieves state-of-the-art on both math reasoning benchmarks and hallucination leaderboards, adding a consistency-based mechanism to the step-credit thread.

## Key Contributions

- Identifies and formalises Context-Sensitive Factual Hallucinations as a distinct failure mode separate from parametric ignorance
- Computes step-level self-consistency scores across multiple rollouts as a reward signal — no separate critic, PRM, or annotation required
- SOTA on math reasoning benchmarks and hallucination leaderboards simultaneously
- Step-level granularity generalises to both correctness and factual faithfulness objectives

## Relevance

SSC-GRPO adds a third mechanism to the step-credit thread alongside value-difference estimation (LVRL) and claim-level group formation (SPLIT-RL). Its cross-rollout consistency score is cheap to compute and model-agnostic, making it a strong candidate for the "step reward without a separate PRM" use case that connects this thread to the PRM integration cluster (PASS, PROGRS, rePIRL) from Oct 16.

## My Thoughts

<!-- Add your own notes here -->
