---
title: "Adaptive Layerwise Perturbation: Unifying Off-Policy Corrections for LLM RL"
authors: ["Chenlu Ye", "Xuanchang Zhang", "Yifan Hao", "Zhou Yu", "Ziji Zhang", "Abhinav Gullapalli", "Hao Chen", "Jing Huang", "Tong Zhang"]
date: 2026-03-19
arxiv_id: "2603.19470v3"
url: "http://arxiv.org/abs/2603.19470v3"
score: 0.80
topics: [reinforcement learning, RL training, PPO, GRPO, agentic RL, tool use]
status: unread
---

# Adaptive Layerwise Perturbation: Unifying Off-Policy Corrections for LLM RL

## Summary

ALP injects small learnable perturbations into the input hidden states of each transformer layer during parameter updates, using the resulting perturbed policy as the importance-ratio numerator against the unchanged inference policy. By flattening the policy distribution at the representation level, ALP naturally tightens the training-inference gap and reduces the heavy tails of importance ratios that cause KL spikes and training instability in off-policy LLM RL. Evaluated on single-turn math and multi-turn tool reasoning, ALP improves final performance, avoids importance-ratio tail blow-up, and enhances exploration throughout iterative training.

## Key Contributions

- Representation-level perturbation as an alternative to IS correction or explicit policy alignment
- Unification perspective: ALP covers inference-time mismatch noise by enlarging the effective policy family
- Ablations showing all-layer representation perturbation substantially outperforms partial-layer and logits-only variants
- Gains on both single-turn math benchmarks and multi-turn tool-integrated reasoning

## Relevance

Opens the off-policy stability thread that POPO (Jun 3) first introduced. ALP's mechanism (perturbing representations to flatten IS ratios) is complementary to today's CPPO (cumulative prefix budget for trust region) and yesterday's ConSteer-RL (confidence-aware GRPO shaping) — they attack the same off-policy instability problem from different angles: trust-region geometry (CPPO), reward shaping (ConSteer-RL), and representation perturbation (ALP). Connects to CTPO (runner-up today) which proposes a theoretically principled IS ratio rather than removing it.

## My Thoughts

<!-- Add your own notes here -->
