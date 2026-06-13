---
title: "Representation-Aware Advantage Estimation: Your Reward Model Provides More Than A Scalar Output"
authors: ["Guozheng Li", "Xiyan Fu", "Yiwen Guo"]
date: 2026-06-13
arxiv_id: "2606.10528"
url: "https://arxiv.org/abs/2606.10528"
score: 0.82
topics: [reward model, RLHF, PPO, GRPO, reinforcement learning]
status: unread
---

# Representation-Aware Advantage Estimation: Your Reward Model Provides More Than A Scalar Output

## Summary

Standard RLHF uses only the scalar output of a reward model, discarding richer preference information encoded in the model's hidden states. RAAE integrates RM hidden-state geometry directly into advantage computation as a drop-in replacement for scalar advantage estimation, consistently improving alignment quality and reducing reward hacking across PPO and GRPO baselines without additional reward model training.

## Key Contributions

- Identifies RM hidden states as an underutilized signal: they encode fine-grained preference differences that scalar rewards over-compress, particularly in near-tie cases
- Representation-Aware Advantage Estimation (RAAE): RM hidden-state geometry (e.g., embedding distance, directional similarity) is incorporated into advantage computation
- Drop-in replacement for standard scalar advantage — no additional model training, minimal overhead
- Consistent improvement in alignment quality benchmarks; reduced reward hacking rate under PPO and GRPO

## Relevance

Complements the reward model robustness thread (HARVE Jun 8, DynaCF Jun 8, PRISM Jun 13) with a signal-enrichment angle: rather than fixing the reward model's training or correcting its biases, RAAE extracts more information out of an existing RM at inference time. Together with PRISM (fixing training bias) and HARVE (editing hacking-susceptible heads), this forms a three-layer stack for improving reward signal quality.

## My Thoughts

<!-- Add your own notes here -->
