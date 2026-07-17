---
title: "Respecting Self-Uncertainty in On-Policy Self-Distillation for Efficient LLM Reasoning"
authors: ["Junlong Ke", "Zichen Wen", "Weijia Li", "Conghui He", "Linfeng Zhang"]
date: 2026-07-17
arxiv_id: "2605.13255v1"
url: "http://arxiv.org/abs/2605.13255v1"
score: 0.80
topics: [RL training, RLHF, RLAIF, reinforcement learning]
status: unread
---

# Respecting Self-Uncertainty in On-Policy Self-Distillation for Efficient LLM Reasoning

## Summary

Proposes EGRSD (Entropy-Guided Reinforced Self-Distillation), which unifies three training signals: a reward-grounded direction, a teacher-student likelihood-ratio magnitude, and a teacher-entropy confidence gate that down-weights high-entropy token positions while maintaining a nonzero floor. Introduces CL-EGRSD, a causal-lookahead variant that distinguishes sustained high-entropy spans (genuinely uncertain, down-weight) from transient high-entropy positions whose following context rapidly becomes low-entropy (informative, preserve). Advances the accuracy-length frontier for Qwen3-4B and Qwen3-8B in thinking mode.

## Key Contributions

- Unified EGRSD objective: reward-grounded direction + likelihood-ratio magnitude + teacher entropy confidence gate
- Entropy gate: down-weights high-entropy token positions where teacher is uncertain, maintains nonzero floor to preserve all token updates
- CL-EGRSD: causal-lookahead variant distinguishing sustained vs transient high-entropy spans via following-context entropy
- Advances accuracy-length Pareto frontier for Qwen3-4B and 8B thinking-mode models vs comparable trainable methods

## Relevance

Directly addresses the persistent vault gap of unified-loss reasoning + self-verification: EGRSD synthesizes RL reward direction with OPD token-level supervision using entropy as the confidence arbiter — exactly the gate mechanism the vault has been searching for across many sessions. The connection to RIPO (today) is notable: both papers identify that uniform treatment of all tokens/regions is wrong; RIPO fixes the geometry of policy updates, EGRSD fixes the weighting of individual token updates.

## My Thoughts

<!-- Add your own notes here -->
