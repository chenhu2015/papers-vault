---
title: "SPA-RL: Reinforcing LLM Agents via Stepwise Progress Attribution"
authors: ["Hanlin Wang", "Chak Tou Leong", "Jiashuo Wang", "Jian Wang", "Wenjie Li"]
date: 2025-05-27
arxiv_id: "2505.20732v1"
url: "http://arxiv.org/abs/2505.20732v1"
score: 0.82
topics: [agentic RL, RL training, reward model, LLM agent]
status: unread
---

# SPA-RL: Reinforcing LLM Agents via Stepwise Progress Attribution

## Summary

SPA-RL proposes Stepwise Progress Attribution (SPA), a reward redistribution framework that decomposes the final outcome reward into per-step contributions by training a progress estimator whose cumulative sum matches task completion, without requiring oracle step annotations. Per-step reward combines the estimated progress contribution with a grounding signal for environment-executed actions, providing fine-grained intermediate rewards that address the delayed-reward problem in multi-step agentic RL. Evaluated on Webshop, ALFWorld, and VirtualHome, SPA-RL outperforms the prior state-of-the-art by +2.5% success rate and +1.9% grounding accuracy.

## Key Contributions

- Identifies delayed reward as the central failure mode in agentic RL: outcome feedback only available at task end provides insufficient guidance about which actions contributed
- SPA framework: trains a progress estimator on trajectories to produce per-step contributions; the estimator is constrained so its cumulative sum equals task completion (no oracle step labels needed)
- Per-step training reward = estimated progress contribution + environment grounding signal; combines learned credit with observable environmental feedback
- +2.5% success rate, +1.9% grounding accuracy over prior SOTA on Webshop, ALFWorld, VirtualHome; further analysis confirms more effective intermediate reward signal

## Relevance

SPA-RL is a direct predecessor to MileGPO (Aug 21) and sits at the center of the causal credit meta-gap opened by "Credit Without Ground Truth" (Aug 21): the progress estimator is one of the "fluency-tracking" signals that paper critiques — it measures progress toward completion, not causal counterfactual contribution. Comparing SPA's progress estimator against MileGPO's PCC criterion and against a counterfactual ground truth (Verifiable Counterfactual Supervision, Aug 22) on a shared benchmark (ALFWorld) would be a high-value empirical experiment.

## My Thoughts

<!-- Add your own notes here -->
