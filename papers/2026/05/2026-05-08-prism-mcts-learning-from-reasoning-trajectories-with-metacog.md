---
title: "PRISM-MCTS: Learning from Reasoning Trajectories with Metacognitive Reflection"
authors: ["Siyuan Cheng", "Bozhong Tian", "YanChao Hao", "Zheng Wei"]
date: 2026-04-07
arxiv_id: "2604.05424v1"
url: "https://arxiv.org/abs/2604.05424v1"
score: 0.78
topics: [reinforcement learning, reward model, agentic RL, RL training]
status: unread
---

# PRISM-MCTS: Learning from Reasoning Trajectories with Metacognitive Reflection

## Summary

PRISM-MCTS makes MCTS for LLM reasoning efficient by coupling a Process Reward Model (PRM) with a shared dynamic memory of 'Heuristics' and 'Fallacies' across parallel rollouts, so each trajectory benefits from prior explorations rather than searching in isolation. The shared memory prunes error-prone branches and reinforces successful strategies, halving trajectory requirements on GPQA while outperforming MCTS-RAG and Search-o1. A data-efficient few-shot PRM training strategy further reduces annotation overhead.

## Key Contributions

- Shared dynamic memory across MCTS rollouts: captures Heuristics (successes) and Fallacies (failures) for cross-trajectory learning
- PRM integrated into MCTS selection, expansion, and backpropagation — not just as a scoring oracle
- 50% reduction in trajectory count on GPQA vs. standard MCTS while outperforming MCTS-RAG and Search-o1
- Few-shot PRM training strategy achieving high-fidelity evaluation with low annotation cost

## Relevance

Bridges the reward model training thread (Rollout Pass-Rate Control, Power Distribution from May 7) with the test-time compute / MCTS-for-LLMs angle that has been a persistent gap in the digest. The PRM-guided shared memory is a novel form of credit sharing across trajectories.

## My Thoughts

<!-- Add your own notes here -->
