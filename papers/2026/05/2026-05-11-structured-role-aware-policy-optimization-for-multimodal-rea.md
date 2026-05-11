---
title: "Structured Role-Aware Policy Optimization for Multimodal Reasoning"
authors: ["Bingqing Jiang", "Difan Zou"]
date: 2026-05-08
arxiv_id: "2605.07274"
url: "http://arxiv.org/abs/2605.07274v1"
score: 0.88
topics: [GRPO, multimodal models, VLM, reward model, agentic RL, vision-language]
status: unread
---

# Structured Role-Aware Policy Optimization for Multimodal Reasoning

## Summary

SRPO revisits multimodal RLVR by decomposing structured responses into perception tokens (visual evidence extraction) and reasoning tokens (answer derivation), then applying role-specific self-distilled on-policy contrasts to refine GRPO's sequence-level advantages. Perception tokens are weighted by their visual dependency under original vs. corrupted visual inputs; reasoning tokens by consistency with generated perception — all without external reward models or teachers. On diverse multimodal benchmarks, SRPO improves evidence-grounded reasoning over standard GRPO.

## Key Contributions

- Role decomposition: perception tokens vs. reasoning tokens within a single LVLM response
- Self-distilled on-policy contrasts: no external teachers or reward models required
- Corrupted-input contrast for perception weighting; generation-consistency contrast for reasoning weighting
- Unified trajectory-level baseline that preserves original GRPO reward/optimization direction

## Relevance

This paper directly extends the step-level credit assignment thread that has been central to recent digests (BEACON, HCAPO, STEPPO), but applies it to the multimodal domain by decomposing tokens by semantic role rather than by step. It matches the core interest in GRPO/RLVR variants and VLM fine-tuning, and offers a practically relevant recipe for improving multimodal reasoning without auxiliary models.

## My Thoughts

<!-- Add your own notes here -->
