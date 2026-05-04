---
title: "ResRL: Boosting LLM Reasoning via Negative Sample Projection Residual Reinforcement Learning"
authors: ["Zihan Lin", "Xiaohan Wang", "Jie Cao", "Jiajun Chai", "Li Wang", "Xiaodong Lu", "Wei Lin", "Ran He", "Guojun Yin"]
date: 2026-05-01
arxiv_id: "2605.00380v1"
url: "http://arxiv.org/abs/2605.00380v1"
score: 0.80
topics: [agentic RL, RL training, RLHF, reward model, LLM agent]
status: unread
---

# ResRL: Boosting LLM Reasoning via Negative Sample Projection Residual Reinforcement Learning

## Summary

ResRL identifies that negative samples in RLVR share semantic distributions with positive samples, so standard negative reinforcement suppresses both good and bad content. The method projects negative-token hidden representations onto an SVD-based low-rank positive subspace and uses projection residuals to selectively modulate negative gradients, decoupling shared semantics from error-specific signals. Across 12 benchmarks spanning math, code, agent tasks, and function calling, ResRL outperforms NSR by +9.4% in Avg@16 on mathematical reasoning while improving generation diversity.

## Key Contributions

- Theoretically links Lazy Likelihood Displacement (LLD) to negative-positive head-gradient interference
- Derives a single-forward proxy that upper-bounds representation alignment to guide conservative advantage reweighting
- SVD-based low-rank projection decouples shared positive-negative semantics from truly negative residuals
- Evaluated on 12 diverse benchmarks: math, code, agent tasks, function calling — broad applicability confirmed

## Relevance

ResRL addresses the same over-penalisation-of-negative-samples problem that UCPO approaches from the diversity-collapse angle — together they triangulate a key RLVR failure mode. Its coverage of agent tasks and function calling directly links it to the tool-use and agentic RL threads in the profile, and the SVD-based approach is more mechanistically grounded than heuristic negative sample filtering.

## My Thoughts

<!-- Add your own notes here -->
