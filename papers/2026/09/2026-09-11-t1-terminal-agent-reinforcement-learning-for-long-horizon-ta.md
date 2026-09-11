---
title: "T1: Terminal Agent Reinforcement Learning for Long-Horizon Tasks"
authors: ["Junyao Yang", "Yucheng Shi", "Zhongzhi Li", "Ruhan Wang", "Zongxia Li", "Haitao Mi", "Leowei Liang"]
date: 2026-09-10
arxiv_id: "2609.11042v1"
url: "https://arxiv.org/abs/2609.11042"
score: 0.85
topics: [agentic RL, RL training, reinforcement learning, reward model, tool use]
status: unread
---

# T1: Terminal Agent Reinforcement Learning for Long-Horizon Tasks

## Summary

T1 is a 122B MoE model trained with RL on real terminal tasks (coding, scientific discovery) operating a live shell for up to 300+ tool-call turns per task, rewarded by task-specific verifiers. It introduces TITO (exact token identifier alignment with turn-boundary drift repair) and rollout routing replay (recording per-token MoE expert choices to eliminate log-probability drift in long-horizon trajectories). A dense process reward counting absolute passing verifiers per turn provides stable credit across 300+ tool-call spans, reaching 64.0% on Terminal-Bench 2.1 vs 43.8% for the base model.

## Key Contributions

- TITO: training-inference token alignment via exact sampled token identifiers with drift repair at turn boundaries — eliminates the log-probability gap between rollout and training passes in long-horizon MoE models
- Rollout routing replay: records per-token MoE expert routing choices at every layer during rollout, replays them during training — ensures identical expert assignments, eliminating a previously unmeasured source of training-inference drift
- Dense process reward: absolute number of passing verifiers per turn rather than binary terminal success — provides per-turn credit signal stable across 300+ tool-call trajectories
- Fully OOD training corpus: task seeds and synthesized tasks disjoint from Terminal-Bench 2.1 — confirms gains reflect capability transfer, not benchmark overfitting

## Relevance

T1 directly extends the long-horizon agentic RL thread by providing the first systematic treatment of training-inference drift in MoE models for 300+ turn tasks — TITO and rollout routing replay address a gap that SAPO/SAO/SRPO (which target single-rollout sampling efficiency) leave open. The dense verifier-counting reward is the concrete realization of the Long-Horizon PPM thread identified Sep 10: segment-level dense credit for very long reasoning chains, here implemented as turn-level absolute passing-verifier count.

## My Thoughts

<!-- Add your own notes here -->
