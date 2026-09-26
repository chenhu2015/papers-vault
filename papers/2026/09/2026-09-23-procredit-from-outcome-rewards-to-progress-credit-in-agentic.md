---
title: "ProCredit: From Outcome Rewards to Progress Credit in Agentic Reinforcement Learning"
authors: ["Ming Ma", "Yi Zhu", "Yiran Zhong", "Feida Zhu", "Chonghan Liu", "Pengkun Jiao", "Qichao Wang", "Yanhao Jia", "Tianming Yang", "Steven Hoi"]
date: 2026-09-23
arxiv_id: "2609.27532"
url: "https://arxiv.org/abs/2609.27532"
score: 0.93
topics: [agentic RL, RL training, GRPO, LLM agent, reward model]
status: unread
---

# ProCredit: From Outcome Rewards to Progress Credit in Agentic Reinforcement Learning

## Summary

ProCredit addresses sparse-reward credit assignment in long-horizon agentic RL by repurposing the task's own verifiable acceptance checks as dense intermediate rewards — running them after each turn and rewarding each turn by its change in progress. Unlike trajectory-graph methods (GRAFT, SALT), ProCredit derives step-level credit directly from task-native verification without a separate reward model or graph construction. Evaluated on AppWorld with Qwen3.5 at three scales, ProCredit outperforms outcome-reward and progress-based baselines by up to +4.1 percentage points, with ablations showing the gain comes from per-turn credit attribution, not final progress alone.

## Key Contributions

- Observation that acceptance checks used for final success evaluation can also be run on intermediate states, making progress as verifiable as the outcome reward
- ProCredit algorithm: reruns acceptance checks after each turn, rewards by change in progress, assigns credit both across attempts (same task) and across turns within a trajectory
- Demonstrates that adding final progress to the trajectory score alone does not improve performance — per-turn credit is what matters
- Consistent improvements over outcome-reward baselines at 3B, 7B, and 14B scales on AppWorld

## Relevance

ProCredit directly complements the step-level credit cluster (GRAFT, SALT) found in prior digests, offering a third distinct approach that avoids trajectory graphs and reward models entirely by leveraging task-native verification. The AppWorld benchmark shared with SALT enables direct comparison; the absence of any auxiliary model makes ProCredit more practically deployable than GRAFT's Bellman + Graph GAE setup.

## My Thoughts

<!-- Add your own notes here -->
