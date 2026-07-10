---
title: "Reinforced Efficient Reasoning via Semantically Diverse Exploration"
authors: ["Ziqi Zhao", "Zhaochun Ren", "Jiahong Zou", "Liu Yang", "Zhiwei Xu", "Xuri Ge", "Zhumin Chen", "Xinyu Ma", "Daiting Shi", "Shuaiqiang Wang", "Dawei Yin", "Xin Xin"]
date: 2026-07-10
arxiv_id: "2601.05053v2"
url: "https://arxiv.org/abs/2601.05053"
score: 0.82
topics: [RL training, GRPO, reward model, agentic RL, LLM agent]
status: unread
---

# Reinforced Efficient Reasoning via Semantically Diverse Exploration

## Summary

ROSE extends RLVR beyond vanilla GRPO by combining MCTS-based tree rollouts with a semantic-entropy branching strategy that identifies high-divergence decision points to expand, and an ε-exploration mechanism for root-level stochastic restarts, producing more diverse and higher-quality reasoning trajectories. A length-aware segment-level advantage estimator rewards concise, correct reasoning while penalizing unnecessarily long chains, directly addressing the efficiency gap left by tree-based search. Validated on multiple math reasoning benchmarks with Qwen and Llama models.

## Key Contributions

- Semantic-entropy-based branching: selects MCTS expansion points by measuring semantic divergence across already-sampled rollouts, not random or UCB-only selection
- ε-exploration: stochastic root-level restarts prevent MCTS search from becoming too local around early committed steps
- Length-aware segment-level advantage estimator: jointly rewards correctness and conciseness; penalizes unnecessarily long reasoning chains
- Validated across Qwen and Llama model families on multiple math benchmarks

## Relevance

ROSE sits at the intersection of three active threads in the vault: (1) diversity in RLVR rollouts (TA-GRPO input diversity, Reaching Beyond the Mode output diversity, today's novelty-bonus paper), (2) segment-level credit assignment (Segmenting Text for RLHF, MRPO's step-position weighting), and (3) MCTS-based exploration for LLM reasoning. The semantic-entropy branching is a principled alternative to the perplexity-based novelty bonus — same goal (diverse rollouts) but operating at the tree search level rather than the objective level.

## My Thoughts

<!-- Add your own notes here -->
