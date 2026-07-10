---
title: "SR-GRPO: Stable Rank as an Intrinsic Geometric Reward for Large Language Model Alignment"
authors: ["Yixuan Tang", "Yi Yang"]
date: 2026-07-10
arxiv_id: "2512.02807v1"
url: "https://arxiv.org/abs/2512.02807"
score: 0.78
topics: [RLHF, reward model, GRPO, RL training]
status: unread
---

# SR-GRPO: Stable Rank as an Intrinsic Geometric Reward for Large Language Model Alignment

## Summary

Proposes stable rank—the ratio of total to dominant-direction variance in hidden state representations—as an intrinsic, annotation-free quality signal for LLM alignment, achieving 84% accuracy on RewardBench without human labels or a reward model. SR-GRPO uses stable rank directly as the GRPO reward, improving Qwen2.5-1.5B-Instruct by 10% on STEM and 19% on math without any external supervision. This opens a path toward scalable RL alignment for tasks where verifiable rewards are unavailable, complementing LLM-as-a-Tutor's examiner-based approach with an entirely model-internal alternative.

## Key Contributions

- Stable rank as a quality signal: measures effective dimensionality of hidden states; high stable rank → information spread across many dimensions → higher quality response
- 84.04% RewardBench accuracy without any human annotations or reward model training
- SR-GRPO: plug-in replacement for the reward signal in GRPO; +10% STEM, +19% math on Qwen2.5-1.5B-Instruct
- Best-of-N sampling with stable rank achieves +11.3pp over greedy decoding on task accuracy

## Relevance

SR-GRPO is the third approach in the vault to non-verifiable RL (alongside LLM-as-a-Tutor's examiner-based constraint escalation and standard RLHF's human preference labels), but uniquely requires no external signal whatsoever — the reward is computed from the model's own hidden states. The stable rank signal is also related to the entropy-gating thread (EGSPO): both papers use information-theoretic measures from model internals to route or scale training updates, but at different levels (representation geometry vs. per-token output entropy).

## My Thoughts

<!-- Add your own notes here -->
