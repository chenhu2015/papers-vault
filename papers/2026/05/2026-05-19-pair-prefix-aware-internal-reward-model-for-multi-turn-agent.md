---
title: "PAIR: Prefix-Aware Internal Reward Model for Multi-Turn Agent Optimization"
authors: ["Wonjoong Kim", "Yeonjun In", "Sangwu Park", "Dongha Lee", "Chanyoung Park"]
date: 2026-05-18
arxiv_id: "2605.17877v1"
url: "http://arxiv.org/abs/2605.17877v1"
score: 0.85
topics: [agentic RL, reward model, GRPO, RL training, LLM agent]
status: unread
---

# PAIR: Prefix-Aware Internal Reward Model for Multi-Turn Agent Optimization

## Summary

PAIR provides dense step-level reward signals for GRPO training in multi-turn agents without requiring external LLM judges, full-trajectory rollouts, or ground-truth labels at every step. It diagnoses that hidden-state probes degrade under prefix contamination in multi-step settings while attention-based features stay robust, then combines both into a two-stage model that achieves highest AUROC on contaminated trajectories. This enables scalable credit assignment for agentic RL training at negligible inference cost.

## Key Contributions

- Diagnoses prefix contamination as the root cause of hidden-state probe degradation in multi-turn settings, showing that probes track prefix coherence rather than grounded correctness when prior steps are corrupted
- Introduces the Prefix-Aware Internal Reward (PAIR) model: frozen hidden-state probe estimates belief-consistency; lightweight attention-based head corrects toward grounded correctness
- Achieves highest AUROC on contaminated trajectories while operating at negligible inference cost — no external model calls, no ground-truth at each step, no full rollouts
- Enables dense per-step reward signals as drop-in replacement for sparse GRPO outcome rewards in multi-turn agentic RL

## Relevance

Directly extends the multi-turn agentic RL thread (ActFocus, AEM, CM2, SDAR, May 16) with a novel credit assignment mechanism that avoids the cost of external PRM judges — a key practical bottleneck for scaling agentic GRPO training. Connects credit assignment to the internal model geometry rather than requiring privileged labels.

## My Thoughts

<!-- Add your own notes here -->
