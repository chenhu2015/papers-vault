---
title: "CompactionRL: Reinforcement Learning with Context Compaction for Long-Horizon Agents"
authors: ["Yujiang Li", "Zhenyu Hou", "Yi Jing", "Jie Tang", "Yuxiao Dong"]
date: 2026-07-26
arxiv_id: "2607.05378"
url: "https://arxiv.org/abs/2607.05378"
score: 0.85
topics: [agentic RL, LLM agent, RL training, GRPO]
status: unread
---

# CompactionRL: Reinforcement Learning with Context Compaction for Long-Horizon Agents

## Summary

Addresses the fundamental constraint that long-horizon agentic LLM trajectories exceed the context window before task completion, by jointly optimizing task execution and context summarization within a single RL objective. Uses token-level loss normalization and cross-trajectory generalized advantage estimation so the model learns both to compress prior trajectory state and to act on it. Applied to GLM-4.5-Air (106B-A30B), achieves 66.8% on SWE-bench Verified (+7.0 pts over base) and 24.5% on Terminal-Bench 2.0 (+3.1 pts); the method is deployed in the RL training pipeline for GLM-5.2 (750B-A40B).

## Key Contributions

- Joint RL optimization of task execution and compaction quality — the model is trained to summarize its own trajectory while continuing to act
- Token-level loss normalization that applies equally to task-action tokens and compaction tokens, avoiding imbalanced gradient pressure
- Cross-trajectory GAE that properly assigns credit across the compaction boundary (where trajectory identity changes after compression)
- Deployed at production scale in GLM-5.2 training — one of the largest reported agentic RL deployments in the vault

## Relevance

CompactionRL addresses a structural limitation (context window) that constrains all long-horizon agentic RL work in the vault. TRACE (Jul 25) extends horizon via turn-level credit; PATS (Jul 25) adapts training context dynamically; CompactionRL extends horizon directly by training compaction within the RL loop. The cross-trajectory GAE is a new credit assignment primitive: it treats the summarized-then-continued trajectory as a single optimization unit, which is a different decomposition from BPO's prefix branching, PATR's tree rollouts, or TRACE's turn-level TD.

## My Thoughts

<!-- Add your own notes here -->
