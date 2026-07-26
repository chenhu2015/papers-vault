---
title: "Neglected Free Lunch from Post-training: Progress Advantage for LLM Agents"
authors: ["Changdae Oh", "Wendi Li", "Seongheon Park", "Samuel Yeh", "Tanwi Mallick", "Sharon Li"]
date: 2026-07-26
arxiv_id: "2606.26080"
url: "https://arxiv.org/abs/2606.26080"
score: 0.93
topics: [agentic RL, reward model, GRPO, LLM agent, RL training]
status: unread
---

# Neglected Free Lunch from Post-training: Progress Advantage for LLM Agents

## Summary

Proves that the log-probability ratio between the RL-trained policy and its reference policy (log π_RL/π_ref) exactly recovers the optimal step-level advantage function under a general stochastic MDP — the 'progress advantage'. This signal is annotation-free, domain-agnostic, and available as a byproduct of standard RL post-training with no additional training or annotations. Evaluated across five benchmarks and four model families for test-time scaling, uncertainty quantification, and failure attribution, consistently outperforming confidence-based baselines and trained reward models.

## Key Contributions

- Derives the progress advantage as log π_RL(a|s) / π_ref(a|s), proving this log-ratio equals the optimal advantage function under general stochastic MDPs
- Zero annotation cost: the signal requires only the RL-trained model and the reference model, both already available after standard post-training
- Three validated applications: test-time scaling (selecting best rollouts), uncertainty quantification (detecting when the model is about to fail), and failure attribution (diagnosing which steps caused a failure)
- Consistently outperforms dedicated trained reward models across model families despite requiring no task-specific training

## Relevance

This paper directly answers the queued follow-up from Jul 25: are there papers using the base/reference model's implicit beliefs as a training or evaluation signal? Progress advantage is the principled derivation showing that TRACE's core insight (log-ratio state values from the frozen reference model) is not ad hoc — it is the optimal step-level advantage function by definition. This retroactively strengthens TRACE (Jul 25) and closes the theoretical gap behind reference-model-as-signal approaches.

## My Thoughts

<!-- Add your own notes here -->
