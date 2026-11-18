---
title: "Learning to Act with Task Progress: Distilling Small Agents from Compact Teacher Supervision"
authors: ["Wenxi Gan"]
date: 2026-10-07
arxiv_id: "2610.10332v1"
url: "http://arxiv.org/abs/2610.10332v1"
score: 0.72
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# Learning to Act with Task Progress: Distilling Small Agents from Compact Teacher Supervision

## Summary

Introduces Task-Progress Distillation (TPD), an offline approach that pairs each demonstrated action from large-model teacher trajectories with a compact task-stage label. A 1.7B student trained with 404 demonstrations on ALFWorld achieves 72.4% mean unseen task success; explicit task-progress labels add 19.7 pp over action-only supervision at the constrained 200-demonstration budget, though the gap closes at 808 demonstrations.

## Key Contributions

- TPD: offline distillation that augments teacher demonstrations with compact task-stage labels, enabling joint scoring of stage–action pairs
- Demonstrates that explicit task-progress information is most valuable at constrained demonstration budgets (200 demos: 67.7% vs 48.0% action-only)
- Shared-history analysis shows TPD gains concentrate at subgoal transitions (object acquisition → processing)
- 1.7B student achieves 72.4% on ALFWorld unseen tasks from 404 demonstrations (no large-model calls at inference)

## Relevance

Adjacent to the multi-turn OPSD cluster (Skill-SD, ActFirst-OPD, SAGE-OPD, EMPO) in that it addresses how to structure agent training supervision. Unlike RL-based approaches, TPD is offline distillation; its main contribution is showing that task-progress structure is a useful inductive bias for compact agent training, complementing the RL-based multi-turn training literature.

## My Thoughts

<!-- Add your own notes here -->
