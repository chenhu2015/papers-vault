---
title: "Dual-Axis Policy Optimization for LLM Agents: Bayesian Feedback Attribution and Trajectory Mass Normalization"
authors: ["Yingxuan Zhuang", "Binhe Yu", "Jingxiao Yang", "Ruopei Sun", "Ziting Li", "Cheng Tan", "Xuhong Zhang", "Jianwei Yin", "Jintao Chen"]
date: 2026-09-17
arxiv_id: "2609.19830v1"
url: "http://arxiv.org/abs/2609.19830v1"
score: 0.88
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# Dual-Axis Policy Optimization for LLM Agents: Bayesian Feedback Attribution and Trajectory Mass Normalization

## Summary

BATON decomposes GRPO-style policy optimization into two orthogonal axes: intra-trajectory feedback attribution (how environment feedback is exploited within a trajectory) and inter-trajectory objective aggregation (how complete trajectories are weighted across a batch). The first axis is instantiated via Bayesian Feedback Attribution, which constructs a feedback-conditioned posterior over sampled actions; the second via Trajectory Mass Normalization (TMN), which assigns equal optimization mass to complete trajectories regardless of length. Both axes yield independent gains and their combination consistently achieves the strongest overall performance on ALFWorld, WebShop, and SearchQA with GRPO and GiGPO.

## Key Contributions

- Dual-axis taxonomy: cleanly separates the intra-trajectory credit distribution problem (what GACA, DRACO, CrEST address) from the inter-trajectory aggregation problem (what TMN addresses) — previously conflated in most GRPO variants
- Bayesian Feedback Attribution: feedback-conditioned posterior over actions within a trajectory, providing a principled intra-trajectory signal beyond scalar advantage estimates
- Trajectory Mass Normalization (TMN): equal mass to complete trajectories prevents length-biased gradient from dominating optimization
- Empirical decomposition: ablation shows both axes provide independent gains and their combination is strictly best on ALFWorld, WebShop, SearchQA

## Relevance

BATON provides the cleanest formal taxonomy for the dense credit assignment work accumulated since Sep 12: the intra-trajectory axis captures GACA/DRACO/CrEST/FACTOR/VICT, while the inter-trajectory axis is a distinct and largely unstudied dimension. TMN directly addresses the length-bias problem that was implicit in the CANOPY V_d analysis (Sep 17): longer trajectories dominate GRPO gradients in terminal-state-verified settings, which inflates the apparent benefit of extended rollouts. BATON's Bayesian attribution is also orthogonal to the hindsight cluster (TRIAL, T-STAR, TASPO, CRISP, VICT, HiMPO) — none of those methods model feedback as a posterior.

## My Thoughts

<!-- Add your own notes here -->
