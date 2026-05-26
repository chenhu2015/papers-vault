---
title: "DVAO: Dynamic Variance-adaptive Advantage Optimization for Multi-reward Reinforcement Learning"
authors: ["Guochao Jiang", "Jingyi Song", "Guofeng Quan", "Chuzhan Hao", "Guohua Liu", "Yuewei Zhang"]
date: 2026-05-26
arxiv_id: "2605.25604v1"
url: "http://arxiv.org/abs/2605.25604v1"
score: 0.83
topics: [GRPO, PPO, RL training, reward model, tool use]
status: unread
---

# DVAO: Dynamic Variance-adaptive Advantage Optimization for Multi-reward Reinforcement Learning

## Summary

DVAO tackles GRPO's instability in multi-reward settings by dynamically adjusting combination weights based on empirical reward variance within each rollout group, up-weighting objectives with stronger learning signal while suppressing noisy ones; this provably maintains bounded advantage magnitudes and introduces self-adaptive cross-objective regularization. Standard approaches (Reward Combination and Advantage Combination) either produce excessively large advantage magnitudes or rely on static hyperparameters that ignore cross-objective correlations. On mathematical reasoning and tool-use benchmarks with Qwen3 and Qwen2.5 models, DVAO achieves a superior multi-objective Pareto frontier with robust training stability.

## Key Contributions

- Identifies two failure modes of multi-reward GRPO scalarization: Reward Combination causes training instability via large advantage magnitudes; Advantage Combination ignores cross-objective correlations with static weights
- DVAO: dynamically adjusts weights per rollout group based on empirical reward variance of each objective, up-weighting high-signal objectives
- Mathematical proof: DVAO maintains bounded advantage magnitudes for training stability
- Self-adaptive cross-objective regularization mechanism; validated on math reasoning and tool-use with Qwen3/Qwen2.5

## Relevance

Directly addresses multi-reward GRPO — a practical need whenever multiple reward signals (e.g., format, correctness, tool-use, length) are combined during RL training. Connects to the tool use keyword and the GRPO/PPO topics in the interest profile.

## My Thoughts

<!-- Add your own notes here -->
