---
title: "Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems"
authors: ["Lang Feng", "Longtao Zheng", "Shuo He", "Fuxiang Zhang", "Bo An"]
date: 2026-05-23
arxiv_id: "2602.08847v1"
url: "http://arxiv.org/abs/2602.08847v1"
score: 0.78
topics: [GRPO, agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems

## Summary

Dr. MAS identifies a key source of training instability when extending GRPO to multi-agent LLM systems: a shared global normalization baseline deviates from each agent's individual reward distribution, causing gradient-norm spikes. The fix is agent-wise advantage normalization — each agent normalizes using its own reward statistics — which is theoretically shown to calibrate gradient scales. Beyond the algorithm, Dr. MAS provides an end-to-end RL training framework with scalable orchestration and per-agent LLM serving; on multi-agent math reasoning and search benchmarks, it achieves +5.6% and +15.2% avg@16 over vanilla GRPO while largely eliminating gradient spikes.

## Key Contributions

- Theoretical diagnosis: global GRPO normalization in MAS causes per-agent gradient scale mismatch leading to training instability
- Agent-wise advantage normalization as a one-line fix that is both theoretically motivated and empirically effective
- End-to-end RL training framework for multi-agent LLM systems with scalable orchestration, flexible per-agent serving, and shared resource scheduling
- Works under heterogeneous agent-model assignments (different model sizes per agent role)

## Relevance

Directly extends the GRPO/multi-agent RL thread. Connects to May 6's RL-for-LLM-MAS paper (orchestration traces) and May 22's Maestro (hierarchical multi-agent orchestration) — provides the training stability mechanism those works lack. LamPO (today) attacks the same GRPO baseline problem at the single-agent level; Dr. MAS solves it for the multi-agent case.

## My Thoughts

<!-- Add your own notes here -->
