---
title: "PAC: Progress-Augmented Advantage Curriculum for Multi-Task Reinforcement Learning of LLMs"
authors: ["Yuanqiang Yu", "Yanzhao Zheng", "Zhentao Zhang", "Tianze Xu", "Chao Ma", "Jihuai Zhu", "Jiashun Liu", "Xinle Deng", "Baohua Dong", "Hangcheng Zhu", "Ruohui Huang"]
date: 2026-08-31
arxiv_id: "2608.30528v1"
url: "http://arxiv.org/abs/2608.30528v1"
score: 0.87
topics: [agentic RL, RL training, GRPO]
status: unread
---

# PAC: Progress-Augmented Advantage Curriculum for Multi-Task Reinforcement Learning of LLMs

## Summary

PAC proposes a progress-augmented advantage curriculum for multi-task LLM RL that jointly tracks two task-level signals: advantage-derived learnability (policy update magnitude) and recent reward gains (actual performance improvement), allocated via Bayesian Thompson Sampling during GRPO training. This dual-signal design prevents misallocation toward tasks with large but ineffective updates — a common failure of magnitude-only curriculum methods. Evaluated in multi-level and multi-domain reasoning settings, PAC achieves higher sample efficiency and final performance than random sampling and advantage-only baselines.

## Key Contributions

- Identifies the failure mode of advantage-only curriculum: large updates ≠ reward gains, leading to rollout budget waste on stalled tasks
- Proposes a dual-signal learnability metric combining advantage magnitude with recent reward delta
- Uses Bayesian Thompson Sampling to allocate rollouts across tasks online, adapting as training progresses
- Validates in both multi-level reasoning (difficulty buckets) and multi-domain reasoning (heterogeneous task types) settings

## Relevance

Directly addresses the open gap identified on 2026-09-22: the missing "two-level curriculum" paper that jointly handles within-task difficulty (advantage signal) and across-task performance tracking (reward gains). PAC complements MATCH (model-aware within-task scheduling) and HarnessBandit (across-harness scheduling) by providing the signal fusion layer — it answers *which* task to train on next rather than *how hard* the task should be.

## My Thoughts

<!-- Add your own notes here -->
