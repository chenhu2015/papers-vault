---
title: "T2SPO: Trajectory-to-Step Policy Optimization for Agentic Reinforcement Learning"
authors: ["Bo-Wen Zhang", "Junwei He", "Maoqi Liu", "Feiran Li", "Song-Lin Lv", "Wentao Ma", "Rongyi Lin", "Shuhan Zhong", "Lan-Zhe Guo"]
date: 2026-09-30
arxiv_id: "2610.00388v1"
url: "http://arxiv.org/abs/2610.00388v1"
score: 0.87
topics: [agentic RL, RL training, reward model, LLM agent]
status: unread
---

# T2SPO: Trajectory-to-Step Policy Optimization for Agentic Reinforcement Learning

## Summary

T2SPO derives step-level rewards from past successful trajectories using a TabPFN regressor that estimates remaining distance to task success at each state. Changes in this regression estimate across consecutive steps yield per-step credit that supplements the terminal task reward without annotations or a learned value network. On ALFWorld and WebShop, T2SPO consistently improves task success over GRPO with 1.5B and 7B models.

## Key Contributions

- TabPFN regressor conditioned on successful trajectory examples estimates remaining distance to success at each agent state, providing a non-parametric step-level value proxy
- Auxiliary credit derived from changes in the regression estimate between consecutive states, combined with task-level outcome supervision
- No annotation requirement: only past successful trajectories are needed; the estimator's context updates as new completions accumulate
- Consistent GRPO improvements on ALFWorld and WebShop across two model scales (1.5B and 7B)

## Relevance

Directly extends the step-credit design space opened by DARS (predicate-DAG discounting) and TASPO (PI-weighted advantage): T2SPO's regression-based remaining-distance proxy is a third distinct approach to dense credit without gold labels, complementing the dependency-graph structure of DARS. The "past successful trajectories as context" mechanism is architecturally similar to CCS's cycle-consistency proxy — both repurpose existing task signals rather than learning a separate reward model.

## My Thoughts

<!-- Add your own notes here -->
