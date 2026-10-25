---
title: "LLMZero: Discovering Adaptive Training Strategies for RL Post-Training via LLM Agents"
authors: ["Haoyang Fang", "Wei Zhu", "Boran Han", "Alex Zhang", "Zhenyu Pan", "Shuo Yang", "Shuai Zhang", "Jiading Gai", "Peng Tang", "Cuixiong Hu", "Xuan Zhu", "Huzefa Rangwala", "George Karypis", "Bernie Wang"]
date: 2026-10-25
arxiv_id: "2606.18388v2"
url: "http://arxiv.org/abs/2606.18388v2"
score: 0.78
topics: [agentic RL, GRPO, RL training, LLM agent]
status: unread
---

# LLMZero: Discovering Adaptive Training Strategies for RL Post-Training via LLM Agents

## Summary

LLMZero uses LLM agents to discover adaptive RL post-training strategies via tree search, diagnosing pathologies at each checkpoint and proposing coordinated multi-parameter transitions. It uncovers a capacity-regularization asymmetry: capacity parameters accumulate monotonically while regularization parameters oscillate with shifting training dynamics, consistent across four GRPO tasks. Achieves 6–15% relative improvement over grid search and 9–140% over base model across diverse GRPO tasks.

## Key Contributions

- Agentic tree-search system for adaptive RL training strategy optimization via checkpoint diagnosis
- Capacity-regularization asymmetry discovery: capacity monotonic accumulation vs. regularization oscillation across training phases
- Multi-parameter coordinated transitions from pathology diagnosis (vs. single-parameter grid search)
- 6–15% relative improvement over grid search; 9–140% over base model on 4 GRPO tasks

## Relevance

Connects two threads: the RL training dynamics/scaling thread (Oct 23–24, "How RL Reshapes" + Ring-Zero) and the agentic RL thread. LLMZero's capacity-regularization asymmetry is a mechanistic characterization of GRPO training dynamics distinct from the scaling-law angle of IsoCompute/Scaling Behaviors — it describes what changes during training rather than how performance scales with budget.

## My Thoughts

<!-- Add your own notes here -->
