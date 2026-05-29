---
title: "Rewards as Labels: Revisiting RLVR from a Classification Perspective"
authors: ["Zepeng Zhai", "Meilin Chen", "Jiaxuan Zhao", "Junlang Qian", "Lei Shen", "Yuan Lu"]
date: 2026-02-05
arxiv_id: "2602.05630v4"
url: "http://arxiv.org/abs/2602.05630v4"
score: 0.79
topics: [RLHF, GRPO, RL training, reinforcement learning, RLVR]
status: unread
---

# Rewards as Labels: Revisiting RLVR from a Classification Perspective

## Summary

REAL reframes RLVR by treating verifiable rewards as categorical labels rather than scalar weights, reformulating policy optimization as a classification problem with anchor logits; this induces monotonic and bounded gradient weighting that eliminates gradient misassignment in positives and gradient domination in negatives endemic to GRPO. On math benchmarks, REAL outperforms GRPO and DAPO by 6.7% on 1.5B and 6.2% on 7B models, with binary cross-entropy alone beating DAPO by 4.5%.

## Key Contributions

- Diagnoses two GRPO failure modes: gradient misassignment in positives (wrong gradient direction) and gradient domination in negatives (large negative gradients overwhelm positive signal)
- Reformulates RLVR as classification with reward labels and anchor logits, inducing bounded and monotonic gradient weighting
- Achieves consistent improvements over GRPO/DAPO on math reasoning at 1.5B and 7B scale
- Shows even vanilla binary cross-entropy under REAL framing beats DAPO, implying the reformulation itself (not the specific classifier) drives gains

## Relevance

Connects to the GRPO variant analysis thread that has been productive throughout May; REAL provides a principled theoretical framing for why GRPO's gradient dynamics are suboptimal and fixes them via a classification lens rather than advantage normalization or token-level credit tricks.

## My Thoughts

<!-- Add your own notes here -->
