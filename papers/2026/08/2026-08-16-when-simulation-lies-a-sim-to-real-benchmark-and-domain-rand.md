---
title: "When Simulation Lies: A Sim-to-Real Benchmark and Domain-Randomized RL Recipe for Tool-Use Agents"
authors: ["Xiaolin Zhou", "Aojie Yuan", "Zheng Luo", "Zipeng Ling", "Xixiao Pan", "Yicheng Gao", "Haiyue Zhang", "Jiate Li", "Shuli Jiang", "Prince Zizhuang Wang", "Zixuan Zhu", "Jinbo Liu", "Ryan A. Rossi", "Hua Wei", "Xiyang Hu"]
date: 2026-05-12
arxiv_id: "2605.11928v1"
url: "https://arxiv.org/abs/2605.11928"
score: 0.73
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# When Simulation Lies: A Sim-to-Real Benchmark and Domain-Randomized RL Recipe for Tool-Use Agents

## Summary

RobustBench-TC introduces 22 perturbation types organized by POMDP components (observation, action space, reward-relevant metadata, transition dynamics) to measure tool-use agent robustness, finding that scale alone does not close gaps — transition perturbations cause ~30% accuracy drops across 1.5B to 32B models. ToolRL-DR applies domain-randomization RL on perturbation-augmented trajectories across three POMDP components, achieving robustness on a 3B backbone comparable to 14B function-calling baselines and closing ~27% of the transition gap despite never seeing transition perturbations in training. RL on adversarial static inputs appears to induce a more persistent retry policy that generalizes to unseen runtime failures.

## Key Contributions

- RobustBench-TC: 22 perturbation types by POMDP component (observation/action/reward-metadata/transition), grounded in verified GitHub issues
- Robustness profile: transition and reward-relevant perturbations are far more damaging (~30–40% drops) than observation perturbations (~5%), scale-invariant
- ToolRL-DR: domain-randomization RL recipe that trains on augmented trajectories for static POMDP components; 3B model reaches 14B-level robustness
- Transfer finding: ~27% transition-gap closure from never-seen transition perturbations, suggesting RL induces a general retry policy

## Relevance

Directly extends the tool-use RL thread (profile keyword: tool use) by framing robustness under realistic deployment conditions as a sim-to-real gap problem for LLM agents. The POMDP component taxonomy is a new axis complementing the vault's RL training mechanism taxonomy — instead of asking "how do we assign credit?", this asks "which POMDP component of the tool-use environment breaks the agent, and how do we train robustness to it?" The retry-policy transfer finding connects to SOD's cascading tool-call error amplification (confirmed novel, Aug 14) — domain-randomized RL may mitigate cascading failures by inducing persistence at the policy level.

## My Thoughts

<!-- Add your own notes here -->
