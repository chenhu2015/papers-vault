---
title: "Entropy Pacing Policy Optimization for Multi-Task Agentic Reinforcement Learning"
authors: ["Zetian Hu", "Shunyu Liu", "Junjie Zhang", "Yongcheng Jing", "Ting-En Lin", "Yongbin Li", "Dacheng Tao"]
date: 2026-07-10
arxiv_id: "2607.07178v1"
url: "https://arxiv.org/abs/2607.07178"
score: 0.82
topics: [agentic RL, GRPO, RL training, LLM agent, multimodal models]
status: unread
---

# Entropy Pacing Policy Optimization for Multi-Task Agentic Reinforcement Learning

## Summary

EPPO identifies a previously unnamed failure mode in multi-task agentic RL—inter-task entropy crossovers, where easier tasks converge prematurely to low-entropy policies and their overflow disrupts harder tasks' exploration, causing entropy spikes and training instability. The fix is task-wise dynamic clipping, replacing GRPO's fixed clip threshold with a task-entropy-aware adaptive bound that tightens updates for over-confident tasks and relaxes them for under-explored ones. Experiments on multi-task agentic benchmarks show EPPO outperforms GRPO and other multi-task RL baselines.

## Key Contributions

- Identifies inter-task entropy crossover as a distinct multi-task failure mode: easy task → low entropy → overflow disrupts hard task exploration (bidirectional)
- Task-wise dynamic clipping: GRPO's fixed ε replaced with per-task entropy-aware adaptive bound (tighter for over-confident, looser for under-explored)
- First GRPO variant specifically targeting the multi-task agentic setting (not just multi-domain data mixing)
- Connects entropy-adaptive clipping to EGSPO's entropy-gated gradient routing — both papers use entropy as the control signal, but EPPO acts at the task level, EGSPO at the token level

## Relevance

EPPO extends the entropy-adaptive control thread (EGSPO, AdaPrefix-GRPO) from single-task to multi-task agentic RL. Together with AdaPrefix-GRPO (per-problem success-rate control) and EGSPO (token-level entropy gate), the vault now has three papers applying entropy as a feedback signal at three granularities: per-token (EGSPO), per-problem (AdaPrefix), and per-task across a multi-task curriculum (EPPO). The inter-task entropy crossover failure mode is also the first RLVR failure mode identified at the *task distribution* level rather than within a single training campaign or trajectory.

## My Thoughts

<!-- Add your own notes here -->
