---
title: "On Advantage Estimates for Max@K Policy Gradients"
authors: ["Shota Takashiro", "Soichiro Nishimori", "Paavo Parmas", "Yongmin Kim", "Kohsei Matsutani", "Gouki Minegishi", "Yusuke Iwasawa", "Takeshi Kojima", "Yutaka Matsuo"]
date: 2026-08-31
arxiv_id: "2606.06080"
url: "https://arxiv.org/abs/2606.06080"
score: 0.83
topics: [reinforcement learning, agentic RL, RL training, GRPO, PPO, reward model, RLHF]
status: unread
---

# On Advantage Estimates for Max@K Policy Gradients

## Summary

MaxPO unifies pass@K and max@K policy-gradient estimators through a systematic study of baseline design and advantage centering. Starting from GRPO's advantage estimator — shown to be policy-gradient unbiased but non-centered — they introduce a Leave-Two-Out (L2O) baseline that preserves unbiasedness while making realized batch advantages exactly zero-sum. The L2O baseline reduces gradient variance and outperforms non-centered alternatives across reasoning benchmarks.

## Key Contributions

- Proves that GRPO's advantage estimator is policy-gradient unbiased but yields non-centered advantages (non-zero sum within batch), introducing systematic gradient bias from baseline mismatch
- Introduces the Leave-Two-Out (L2O) baseline: for each sample, the baseline is the average of the other K-1 samples, giving exactly centered advantages in finite batches
- Derives the canonical finite-batch advantage for max@K, providing a unified theoretical view of existing estimators (GRPO, REINFORCE-leave-one-out, and variants)
- Efficient quadratic-time implementation that integrates naturally into group-based RL for LLM post-training

## Relevance

This paper directly addresses a structural property of GRPO's advantage estimation that underlies many vault papers (GRPO, OPDVR, AToD, Hints/Critics/Teachers). The L2O centering result is an actionable finding: any GRPO-derived method could benefit from swapping in the L2O baseline to reduce gradient variance without changing unbiasedness guarantees. Followed up the Hints/Critics/Teachers HL-Gauss critic thread (Aug 30) — both papers converge on the same lesson that advantage/critic calibration matters more than previously assumed.

## My Thoughts

<!-- Add your own notes here -->
