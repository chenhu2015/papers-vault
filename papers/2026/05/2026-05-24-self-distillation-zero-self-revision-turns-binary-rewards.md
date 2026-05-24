---
title: "Self-Distillation Zero: Self-Revision Turns Binary Rewards into Dense Supervision"
authors: ["Yinghui He", "Simran Kaur", "Adithya Bhaskar", "Yongjin Yang", "Jiarui Liu", "Narutatsu Ri", "Liam Fowl", "Abhishek Panigrahi", "Danqi Chen", "Sanjeev Arora"]
date: 2026-04-13
arxiv_id: "2604.12002v1"
url: "http://arxiv.org/abs/2604.12002v1"
score: 0.82
topics: [RLHF, RLAIF, RL training, reward model, reinforcement learning]
status: unread
---

# Self-Distillation Zero: Self-Revision Turns Binary Rewards into Dense Supervision

## Summary

SD-Zero trains a single model to play two roles: a Generator producing an initial response and a Reviser that, conditioned on that response and its binary reward, produces an improved response. On-policy self-distillation then uses the Reviser's token distributions as dense supervision for the Generator—converting sparse binary rewards into token-level self-guidance without any external teacher or high-quality demonstrations. On math and code benchmarks with Qwen3-4B-Instruct and Olmo-3-7B-Instruct, SD-Zero improves by at least 10% over base models and outperforms RFT, GRPO, and SDFT under the same sample budget.

## Key Contributions

- Generator + Reviser dual-role architecture instantiated from a single model backbone
- On-policy self-distillation: Reviser's token distributions conditioned on Generator's response + reward serve as dense supervision
- Token-level self-localization: Reviser identifies which tokens need revision based on binary reward signal
- Iterative self-evolution: regular teacher synchronization enables progressive distillation from improving revision capability

## Relevance

Follows the ICRL (May 20) self-critique internalization thread but takes an orthogonal route—ICRL used a shared backbone critic trained jointly via RL, while SD-Zero uses self-distillation from a conditioning mechanism to replace the external teacher that RLAIF methods typically require.

## My Thoughts

<!-- Add your own notes here -->
