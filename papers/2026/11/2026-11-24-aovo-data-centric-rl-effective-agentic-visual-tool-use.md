---
title: "From Reward Engineering to Data-Centric Reinforcement Learning for Effective Agentic Visual Tool Use"
authors: ["Jin Cui", "Xinyue Long", "Jiepeng Zhou", "Boran Zhao", "Pengju Ren", "Hao Dong"]
date: 2026-11-24
arxiv_id: "2611.28558v1"
url: "http://arxiv.org/abs/2611.28558v1"
score: 0.80
topics: [agentic RL, RL training, tool use, multimodal models]
status: unread
---

# From Reward Engineering to Data-Centric Reinforcement Learning for Effective Agentic Visual Tool Use

## Summary

Argues that call-contingent rewards for MLLM visual tool use distort the RL training objective and produce degenerate calling behaviors (e.g., calling tools indiscriminately or never). Proposes AOVO, a data-centric framework that counterfactually probes the model's reasoning states to identify observation-sensitive questions (where visual tool output changes the answer) versus reasoning-dominated ones, then uses policy-adaptive data sampling (PADS) to periodically reestimate category-level observation effects and dynamically reallocate training toward informative examples — optimizing solely on final-answer correctness with no tool-specific rewards.

## Key Contributions

- Data-centric framing: identifies *which* training examples benefit from tool use rather than incentivizing tool calls via rewards
- Counterfactual perception attribution: probes whether visual observations change the model's reasoning outcome to classify questions
- PADS (Policy-Adaptive Data Sampling): periodic reestimation of tool observation effects → dynamic training distribution reallocation
- Avoids reward engineering for tool use while outperforming call-contingent reward methods on visual perception and reasoning benchmarks

## Relevance

Directly addresses the tool use RL thread from the interest profile — connects to OpenReward (tool-augmented reward model) and extends the RLVR training thread to the question of *how* to train tool use without corrupting the reward signal. Distinct angle: data selection rather than reward design.

## My Thoughts

<!-- Add your own notes here -->
