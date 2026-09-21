---
title: "ArenaFlow: From Trajectory Ranking to Hierarchical Credit Propagation for Open-Ended Agent RL"
authors: ["Qiang Zhang", "Ruixue Ding", "Fanrui Zhang", "Xi Chen", "Boli Chen", "Shihang Wang", "Yinfeng Huang", "Yi Zheng", "Pengjun Xie", "Kaipeng Zhang", "Jiawei Liu", "Zheng-Jun Zha"]
date: 2026-09-18
arxiv_id: "2609.21378v1"
url: "http://arxiv.org/abs/2609.21378v1"
score: 0.90
topics: [agentic RL, RL training, reward model, LLM agent, GRPO]
status: unread
---

# ArenaFlow: From Trajectory Ranking to Hierarchical Credit Propagation for Open-Ended Agent RL

## Summary

ArenaFlow addresses open-ended agent RL — where diverse solutions make scalar reward design hard — by combining tournament-based relative trajectory ranking with two-level hierarchical credit propagation. At the step level, trajectory-level advantages are distributed to high-confidence pivotal steps according to tournament survival depth; at the skill level, a global skill memory tracks utility of reusable strategy skills discovered via group-level usage attribution, with those skills then serving as policy priors for future exploration. Experiments validate effectiveness across open-ended agent tasks.

## Key Contributions

- Tournament-based relative ranking replaces pointwise scalar rewards for open-ended tasks, deriving trajectory-level signals from pairwise comparisons
- Structured reflective evaluation extracts three supervision types: pivotal success steps, reusable strategy skills, and per-skill usage attribution
- Step-level credit propagation distributes trajectory advantages to high-confidence pivotal steps weighted by tournament survival depth
- Global skill memory with utility-aware updating, pruning, and retrieval; skills serve as policy priors for future rollout exploration

## Relevance

Directly extends the credit assignment cluster (BATON/GRSD/StepOPSD/AHEAD et al.) by adding open-ended task support, where the core difficulty is that scalar rewards are unavailable rather than just noisy. The tournament-ranking trajectory comparison connects to the BATON/ReNIO inter-trajectory axis; the step-level pivotal-step propagation connects to AHEAD's step-type classification and StepOPSD's action-boundary segmentation. The global skill memory is a new axis not yet present in the vault, bridging credit assignment and skill-based policy priors (adjacent to APEx's procedural skills).

## My Thoughts

<!-- Add your own notes here -->
