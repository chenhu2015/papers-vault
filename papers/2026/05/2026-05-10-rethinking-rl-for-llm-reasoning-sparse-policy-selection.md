---
title: "Rethinking RL for LLM Reasoning: It's Sparse Policy Selection, Not Capability Learning"
authors: ["Ömer Faruk Akgül", "Rajgopal Kannan", "Willie Neiswanger", "Viktor Prasanna"]
date: 2026-05-07
arxiv_id: "2605.06241"
url: "http://arxiv.org/abs/2605.06241v1"
score: 0.85
topics: [reinforcement learning, RL training, GRPO, reward model]
status: unread
---

# Rethinking RL for LLM Reasoning: It's Sparse Policy Selection, Not Capability Learning

## Summary

Token-level analysis across multiple model families and RL algorithms shows RL only modifies 1–3% of token positions during LLM reasoning post-training, and the promoted tokens always lie within the base model's top-5 alternatives — reframing RL as sparse policy selection rather than capability acquisition. This insight motivates ReasonMaxxer, which applies contrastive loss only at entropy-gated decision points identified from base-model rollouts, matching full RL accuracy across six math benchmarks with roughly three orders of magnitude less training compute.

## Key Contributions

- Empirical finding: RL for LLM reasoning corrects only 1–3% of token positions, always within base model's top-5, across all tested RL algorithms
- Reframes RL improvement as sparse policy selection (steering existing paths) not capability learning (new paths)
- Base model entropy alone identifies the positions RL would correct — no RL-trained model needed
- ReasonMaxxer: contrastive loss at entropy-gated decision points, matching full RL with ~1000× less compute

## Relevance

Provides a fundamental mechanistic explanation for *why* GRPO and similar algorithms work, directly relevant to the RL training research thread running through the entire digest series. This is a companion theory paper to the data-curation and reward-design work (DEPO, Rollout Pass-Rate Control from May 7) — together they paint a picture of what RL actually optimizes in LLMs.

## My Thoughts

<!-- Add your own notes here -->
