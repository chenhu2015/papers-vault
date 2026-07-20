---
title: "Answer-Consistent Chain-of-thought Reinforcement Learning For Multi-modal Large Language Models"
authors: ["Minbin Huang", "Runhui Huang", "Chuanyang Zheng", "Jingyao Li", "Guoxuan Chen", "Han Shi", "Hong Cheng"]
date: 2025-10-11
arxiv_id: "2510.10104"
url: "http://arxiv.org/abs/2510.10104v1"
score: 0.73
topics: [GRPO, multimodal, VLM, vision-language, RL training]
status: unread
---

# Answer-Consistent Chain-of-thought Reinforcement Learning For Multi-modal Large Language Models

## Summary

ACRE identifies that outcome-driven GRPO training causes reasoning-answer misalignment in MLLMs—standard GRPO on MMVU yields only 79.7% consistency between reasoning traces and chosen answers. It addresses this by adding an auxiliary consistency-verification reward: after the model generates a CoT and initial answer, the answer options are shuffled and the model is re-prompted with the same reasoning trace; a high reward is granted only if both answers agree and are correct, penalizing reasoning-answer misalignment and discouraging option-ordering biases. Tested on video and multimodal math benchmarks, ACRE achieves +2.2% and +1.5% over GRPO.

## Key Contributions

- Quantifies reasoning-answer misalignment in standard GRPO: 79.7% consistency on MMVU, indicating ~20% of training examples have reasoning traces inconsistent with chosen answers
- Consistency-verification reward via option shuffling: re-prompts the model with the same reasoning trace after shuffling answer choices; coherent reasoning should produce the same answer regardless of option ordering
- Penalizes both reasoning-answer misalignment and option-ordering bias (a spurious pattern distinct from genuine reasoning)
- Earlier (Oct 2025) treatment of the same failure mode that CORA (2026) addresses with a more sophisticated HRAS mechanism

## Relevance

ACRE is the predecessor to CORA (Jul 19) in the thinking-answer consistency thread: both identify that GRPO-style training decouples reasoning traces from final answers, but ACRE uses a simpler option-shuffling consistency check while CORA uses a dedicated consistency reward model with HRAS coordination. ACRE's option-ordering bias finding is an additional failure mode not covered by CORA.

## My Thoughts

<!-- Add your own notes here -->
