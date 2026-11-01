---
title: "Where to Learn and How Far to Roll Out: Efficient Adaptive Training for GUI Agents"
authors: ["Yuxiang Chai", "Quyu Kong", "Panrong Tong", "Steven Hoi", "Yue Wang"]
date: 2026-11-01
arxiv_id: "2610.39251v1"
url: "https://arxiv.org/abs/2610.39251"
score: 0.92
topics: [agentic RL, RL training, GRPO, LLM agent, tool use]
status: unread
---

# Where to Learn and How Far to Roll Out: Efficient Adaptive Training for GUI Agents

## Summary

Proposes a two-stage adaptive GRPO framework for GUI agent training that addresses the inefficiency of re-executing mastered trajectory prefixes from scratch. Stage I uses action disagreement (uncertainty over sampled GUI actions) to select informative pivot states from expert trajectories, performing one-step RL at those pivots; Stage II then progressively expands policy responsibility via Local→Suffix→Root training. Reduces environment interaction by 56–61% relative to vanilla GRPO on MobileGym and CUA-Gym-Hub while improving task success.

## Key Contributions

- Action disagreement metric: measures uncertainty directly from sampled GUI actions to identify which intermediate states are worth training on, avoiding both already-mastered and hopelessly difficult states
- Reusable intermediate checkpoints from expert trajectories enable repeated training from mid-trajectory states without replaying the full prefix
- Two-stage curriculum: Stage I one-step RL at pivots → Stage II progressive expansion (Local → Suffix → Root) that gradually transfers policy responsibility
- 56–61% reduction in environment interaction vs. vanilla GRPO with simultaneous performance improvement on MobileGym and CUA-Gym-Hub

## Relevance

Directly extends the GUI agent RL thread (EnvSched, Online Dense RL iOS, AndroidFlux) with a training efficiency angle: while prior work optimised which tasks to roll out or how to scale execution, this paper optimises where within a trajectory to apply RL supervision. Complements EnvSched's environment-level curriculum with a state-level curriculum.

## My Thoughts

<!-- Add your own notes here -->
