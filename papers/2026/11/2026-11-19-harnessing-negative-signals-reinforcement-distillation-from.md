---
title: "Harnessing Negative Signals: Reinforcement Distillation from Teacher Data for LLM Reasoning"
authors: ["Shuyao Xu", "Cheng Peng", "Jiangxuan Long", "Weidi Xu", "Wei Chu"]
date: 2025-05-30
arxiv_id: "2505.24850"
url: "https://arxiv.org/abs/2505.24850"
score: 0.75
topics: [RLAIF, RL training, RLHF, reinforcement learning]
status: unread
---

# Harnessing Negative Signals: Reinforcement Distillation from Teacher Data for LLM Reasoning

## Summary

REDI introduces a reinforcement distillation objective that leverages both correct and incorrect teacher reasoning traces in offline knowledge distillation, addressing the standard practice of discarding negative traces. A two-stage recipe (SFT on positive traces, then REINFORCE-style optimization on both) outperforms DPO and SimPO for distillation. A 1.5B model trained on 131k Open-R1 traces achieves 83.1% on MATH-500, matching DeepSeek-R1-Distill-Qwen-1.5B trained on 800k proprietary samples.

## Key Contributions

- REINFORCE-style Reinforcement Distillation (REDI) objective: applies REINFORCE to both positive and negative offline teacher traces
- Two-stage recipe: SFT on positive traces first, then REDI on both positive and negative traces
- Outperforms DPO and SimPO in the offline distillation setting
- 6× data efficiency vs DeepSeek-R1 proprietary distillation data (131k vs 800k samples) while matching performance at 1.5B scale

## Relevance

REDI connects to the OPSD/distillation cluster from a different angle: it is an offline distillation method (no live environment interaction) that uses rejected teacher traces. This is complementary to the online OPSD approaches (DASD, HSD, Skill-SD) but represents the negative-trace exploitation direction, related to REDI's approach of using the failed oracle branches that SERO would otherwise discard.

## My Thoughts

<!-- Add your own notes here -->
