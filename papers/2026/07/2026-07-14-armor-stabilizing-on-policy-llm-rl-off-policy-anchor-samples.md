---
title: "ARMOR: Stabilizing On-Policy LLM RL with Off-Policy Anchor Samples"
authors: ["Kexin Huang", "Junkang Wu", "Jinda Lu", "Shuo Yang", "Chiyu Ma", "Jiancan Wu", "Xiang Wang", "Xiangnan He", "Guoyin Wang", "Jingren Zhou"]
date: 2026-07-11
arxiv_id: "2607.10481"
url: "https://arxiv.org/abs/2607.10481"
score: 0.80
topics: [RL training, GRPO, RLHF, reinforcement learning, PPO]
status: unread
---

# ARMOR: Stabilizing On-Policy LLM RL with Off-Policy Anchor Samples

## Summary

ARMOR identifies that reverse KL regularization — standard protection against over-optimization in LLM RL — fails to ensure complete reference distribution coverage, allowing policies to exploit training heuristics outside the reference support. The proposed fix mixes off-policy anchor rollouts from the reference policy into training (Anchor Rollout) with a reformulated mixed optimization objective that enables controlled exploration without auxiliary KL losses. On reasoning benchmarks, ARMOR prevents validation collapse and sustains performance improvement over extended training horizons.

## Key Contributions

- Formal analysis showing reverse KL regularization fails coverage in the over-optimization regime
- Anchor Rollout: off-policy reference samples mixed into training to preserve established solution patterns
- Mixed Optimization: reformulated policy objective for controlled exploration without auxiliary KL loss terms
- Demonstrates sustained validation performance over extended training, avoiding the collapse documented in GRPO-based methods

## Relevance

ARMOR addresses the training instability problem that Nemotron-Cascade-2 (vault Jul 6) and From Accuracy to Robustness (vault Jul 13) identified from different angles — the over-optimization failure mode where the policy exploits training heuristics is the training-side complement to the reward hacking documented in those papers. ARMOR's off-policy anchoring offers an alternative stabilization mechanism to Tango's generative co-training: Tango co-evolves the verifier to prevent reward exploitation; ARMOR anchors the policy to the reference distribution directly. The extended training horizon result is particularly relevant for long-horizon agentic RL (DART, ARTIST) where training collapse is a known failure mode.

## My Thoughts

<!-- Add your own notes here -->
