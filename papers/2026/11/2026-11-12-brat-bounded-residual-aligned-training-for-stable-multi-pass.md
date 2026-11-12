---
title: "BRAT: Bounded Residual-Aligned Training for Stable Multi-Pass LLM Post-Training"
authors: ["Xunlan Zhou", "Yuzhe Zhao", "Xuhong Huang", "Feng Chen", "Xuanlin Chen", "Lang Feng", "Bo An"]
date: 2026-11-12
arxiv_id: "2611.10873v1"
url: "https://arxiv.org/abs/2611.10873"
score: 0.80
topics: [RL training, GRPO, PPO, RLHF, agentic RL]
status: unread
---

# BRAT: Bounded Residual-Aligned Training for Stable Multi-Pass LLM Post-Training

## Summary

BRAT addresses multi-pass rollout reuse fragility in GRPO/PPO by assigning each token a gradient weight that decreases linearly with the probability ratio and vanishes at the trust-region boundary, with group-centered rewards normalised by their maximum magnitude to stay bounded without extra hyperparameters. A held-out alignment analysis shows in-sample vs held-out policy alignment drops nearly an order of magnitude under repeated passes, motivating the proximal bounded reweighting objective. With four reuse passes, BRAT avoids training collapse and achieves higher average accuracy with lower seed variance than clipped PPO-style objectives.

## Key Contributions

- Empirical diagnosis: in-sample vs held-out policy alignment drops ~10× across 3 base models under multi-pass reuse, confirming that repeated passes overfit the sampled group
- Linear gradient weight w(r) → 0 at boundary: softer than PPO clipping (abrupt cutoff), avoids unclipped collapse (all gradients retained), avoids negative baseline (all responses reinforced)
- Reward normalisation by maximum magnitude keeps advantages zero-mean and bounded without extra hyperparameters
- Avoids training collapse and achieves higher accuracy + lower seed variance at 4 reuse passes

## Relevance

Extends the GRPO training dynamics thread: BRAT addresses a practical engineering problem (multi-pass reuse instability) that any team running GRPO with K>1 gradient passes will encounter. The linear weight scheme is a principled middle ground between the two failure modes that have been identified (PPO clipping's gradient cutoff vs unclipped collapse), and the held-out alignment diagnostic is reusable as a training health check.

## My Thoughts

<!-- Add your own notes here -->
