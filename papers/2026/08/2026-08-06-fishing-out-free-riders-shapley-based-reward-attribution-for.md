---
title: "Fishing Out Free Riders: Shapley-Based Reward Attribution for Parallel Reasoning via Reinforcement Learning"
authors: ["Wentao Zhang", "Haoyu Zhang", "Xinke Jiang", "Yuxuan Cheng", "Yuhan Pan", "Miao Li", "Zhipeng Qiao", "Tao Feng", "Zhen Tao", "Dengji Zhao"]
date: 2026-08-06
arxiv_id: "2607.18979"
url: "https://arxiv.org/abs/2607.18979"
score: 0.78
topics: [RL training, reward model, agentic RL, GRPO]
status: unread
---

# Fishing Out Free Riders: Shapley-Based Reward Attribution for Parallel Reasoning via Reinforcement Learning

## Summary

Parallel Shapley reformulates credit assignment in multi-path LLM reasoning as a cooperative game where each reasoning path is a player, using Shapley values to quantify marginal contributions rather than assigning uniform outcome-level rewards to all paths. A generative reward model evaluates path utilities and Monte Carlo sampling enables efficient Shapley approximation; the framework explicitly identifies and down-weights free rider paths—redundant or misleading paths that receive uniform reward despite contributing little under standard GRPO. Experiments on mathematical reasoning benchmarks show Parallel Shapley outperforms existing baselines while providing more stable and interpretable training signals.

## Key Contributions

- Formulates multi-path reasoning as a cooperative game; Shapley value quantifies each path's marginal contribution to the group outcome
- Generative reward model for path utility evaluation + Monte Carlo Shapley approximation for efficiency
- Identifies "free riders" — paths that receive uniform reward but contribute negatively or minimally — and down-weights them
- More stable and interpretable training vs. outcome-level GRPO; evaluated on math reasoning benchmarks

## Relevance

Parallel Shapley addresses credit assignment at the path level in parallel reasoning, complementing the vault's token-level (ADRS, PCSD, OCSD) and step-level (Guided-OPD, FutureBridge-OPD) credit assignment threads. It is the first paper in the vault to apply cooperative game theory to RL credit in LLM reasoning. The free rider concept is structurally related to TACO's DAPR (Aug 2's differential probing for per-tool credit): both address the uniform-reward problem in multi-component rollouts, but DAPR uses counterfactual probing while Parallel Shapley uses Shapley marginal contribution.

## My Thoughts

<!-- Add your own notes here -->
