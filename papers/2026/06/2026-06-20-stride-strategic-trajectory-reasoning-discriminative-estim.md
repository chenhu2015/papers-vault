---
title: "STRIDE: Strategic Trajectory Reasoning via Discriminative Estimation for Verifiable Reinforcement Learning"
authors: ["Qinjian Zhao", "Zhihao Dou", "Dinggen Zhang", "Xiangyu Li", "Chaoda Song", "Zhongwei Wan", "Xinpeng Li", "Yanyan Zhang", "Kaijie Chen", "Qingtao Pan", "Chengcheng Feng", "Zhiqiang Gao", "Xiaoyu Xia"]
date: 2026-06-14
arxiv_id: "2606.15866v1"
url: "http://arxiv.org/abs/2606.15866v1"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model, VLM]
status: unread
---

# STRIDE: Strategic Trajectory Reasoning via Discriminative Estimation for Verifiable Reinforcement Learning

## Summary

STRIDE contrasts successful and failed trajectories within each GRPO response group to estimate the outcome-discriminative preference of each n-gram strategic pattern, then combines this with reasoning saliency entropy to identify decision-relevant patterns. These patterns receive differentiated advantage values during RL optimization, providing fine-grained credit assignment that remains fully verifiable (no annotations beyond ground-truth outcomes). Experiments confirm consistent gains across diverse models, tasks, VLMs, and agent-based systems.

## Key Contributions

- Trajectory-contrastive n-gram discriminativity: within-group success/failure contrast as a verifiable credit signal
- Saliency-entropy weighting to further filter for decision-relevant patterns among discriminative n-grams
- Differentiated per-pattern advantage values replacing uniform per-token advantages in RLVR
- Demonstrated applicability to VLMs and agentic settings (not only math reasoning)

## Relevance

STRIDE is the contrastive complement to the credit assignment thread built over the past week: where AT-RL (Jun 14) identifies anchor tokens cross-modally, DRE (Jun 19) edits trajectory segments post-hoc, and R3L (Jun 14) redistributes credit to pivotal tokens, STRIDE derives discriminative credit from within-group trajectory contrast — the most direct use of the GRPO group structure itself as a credit signal. The approach also connects to Reasoning Arena (Jun 13, trace tournaments) which similarly leverages within-group trajectory comparisons, but STRIDE operates at the n-gram level rather than full trajectory preference.

## My Thoughts

<!-- Add your own notes here -->
