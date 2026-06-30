---
title: "ExTra: Exploratory Trajectory Optimization for Language Model Reinforcement Learning"
authors: ["Wenyang Hu", "Junxiang Jia", "Zhen Shu", "Daniel Dahlmeier", "See-Kiong Ng", "Bryan Kian Hsiang Low"]
date: 2026-06-30
arxiv_id: "2606.24994"
url: "http://arxiv.org/abs/2606.24994v1"
score: 0.82
topics: [agentic RL, GRPO, RL training, reward model]
status: unread
---

# ExTra: Exploratory Trajectory Optimization for Language Model Reinforcement Learning

## Summary

GRPO fails at both difficulty extremes — easy prompts produce all-correct low-diversity groups with no gradient signal, and hard prompts produce all-incorrect groups with no positive reward. ExTra combines two GRPO-compatible mechanisms: a novelty reward that adds embedding-based diversity bonuses to diverse correct solutions after GRPO normalization, and entropy-guided prefix regeneration that scores partial trajectories by entropy and continues exploration from promising intermediate high-entropy steps. Across six math reasoning benchmarks, ExTra improves Qwen3-1.7B by approximately +5 points pass@1 and +7 points pass@16 over GRPO.

## Key Contributions

- Novelty reward: embedding-based diversity bonus added after GRPO normalization rewards diverse correct solutions (addresses easy-prompt homogeneity)
- Entropy-guided prefix regeneration: partial trajectories scored by entropy, exploration continued from high-entropy branching points (addresses hard-prompt failure)
- Two mechanisms address opposite difficulty extremes within a single GRPO-compatible framework
- +5 pass@1 / +7 pass@16 over GRPO on six math benchmarks; improved inference-time coverage

## Relevance

ExTra is the most direct synthesis of the exploration thread (SPS Jun 20 + GOLF Jun 20 + DEEP-GRPO Jun 20) and the sparse policy selection insight (ReasonMaxxer Jun 20): its entropy-guided prefix regeneration operationalizes the ReasonMaxxer finding that high-entropy positions are the effective branching points, explicitly continuing exploration from those positions. The novelty reward complements SPS's IRL-based distribution reshaping by operating at the group-level selection criterion rather than the training distribution. Together SPS (IRL shaping), GOLF (aggregated external feedback), and ExTra (entropy-guided prefix + novelty) form three orthogonal exploration interventions for the same underlying problem.

## My Thoughts

<!-- Add your own notes here -->
