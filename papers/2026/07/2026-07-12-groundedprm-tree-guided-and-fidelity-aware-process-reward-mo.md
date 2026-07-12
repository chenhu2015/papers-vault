---
title: "GroundedPRM: Tree-Guided and Fidelity-Aware Process Reward Modeling for Step-Level Reasoning"
authors: ["Yao Zhang", "Yu Wu", "Haowei Zhang", "Weiguo Li", "Haokun Chen", "Jingpei Wu", "Guohao Li", "Zhen Han", "Volker Tresp"]
date: 2025-10-16
arxiv_id: "2510.14942"
url: "https://arxiv.org/abs/2510.14942"
score: 0.80
topics: [reward model, RL training, agentic RL, reinforcement learning]
status: unread
---

# GroundedPRM: Tree-Guided and Fidelity-Aware Process Reward Modeling for Step-Level Reasoning

## Summary

GroundedPRM trains a PRM using MCTS-constructed structured reasoning paths combined with external tool verification for each intermediate step, providing execution-grounded correctness signals that eliminate hallucinated supervision. A hybrid reward aggregation mechanism fuses tool-based step verification with MCTS-derived outcome feedback, formatted as a rationale-enhanced generative structure. Trained on only 40K automatically labeled samples (10% of competitors), GroundedPRM achieves up to 26% relative improvement on ProcessBench and outperforms PRMs trained with human-labeled supervision in reward-guided greedy search.

## Key Contributions

- MCTS-constructed structured reasoning paths for fine-grained credit assignment (reduces noisy credit attribution vs. Monte Carlo rollout methods)
- External tool verification for each intermediate step: execution-grounded signals eliminate hallucinated supervision
- Hybrid reward aggregation: fuses tool-based step correctness with MCTS-derived global outcome feedback
- Generative rationale-enhanced reward format: improves interpretability and compatibility with instruction-tuned LLMs
- 40K samples (10% of competitive baselines) → 26% improvement on ProcessBench, beating human-labeled PRMs

## Relevance

GroundedPRM is the most direct answer to the tree-based PRM gap identified from DART (Jul 11): where DART uses tree-based process advantage as a training signal for policy optimization, GroundedPRM uses MCTS + tool verification to build a separate PRM that could serve as DART's reward signal. The tool-verification component also connects directly to the agentic tool-use thread (AutoTool, ARTIST, DynaWeb, DART): GroundedPRM uses tool execution as a ground-truth verifier for step correctness, which is the reward modeling complement to DART's tool-insertion discovery. Together: DART finds where to insert tools; GroundedPRM verifies whether the insertion was correct.

## My Thoughts

<!-- Add your own notes here -->
