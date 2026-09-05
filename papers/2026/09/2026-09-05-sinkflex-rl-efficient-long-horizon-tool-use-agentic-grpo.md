---
title: "Efficient Reinforcement Learning for Long-Horizon Tool-Use Agentic Tasks"
authors: ["Zelei Cheng", "Amritansh Mishra", "Sambit Sahu", "William Campbell"]
date: 2026-09-05
arxiv_id: "2608.10357v1"
url: "http://arxiv.org/abs/2608.10357v1"
score: 0.82
topics: [agentic RL, tool use, GRPO, LLM agent, RL training]
status: unread
---

# Efficient Reinforcement Learning for Long-Horizon Tool-Use Agentic Tasks

## Summary

SINKFLEX-RL is a modular training system for RL in dual-control tool-use environments, combining a Gymnasium-compatible environment wrapper, VERL-style rollout dataflow, GRPO without a separate value model, and sink-aware FlexAttention for memory-efficient long-context training. On Tau2Bench retail evaluation, validation reward (mean@1) rises from 0.25 to 0.44 during training; the optimized attention path reduces peak VRAM by 19.7% at 4096 tokens. The system demonstrates that co-designing environment interfaces, RL dataflow, and attention-kernel mechanics together enables memory-feasible long-horizon agentic RL that would otherwise OOM on standard eager attention.

## Key Contributions

- Modular RL training system integrating Gymnasium environment wrapper + VERL-style rollout dataflow + GRPO (no separate value model) for tool-use agents
- Sink-aware FlexAttention path that preserves model-specific sink scaling under causal and sliding-window masks, reducing peak VRAM 19.7% at 4096 tokens and enabling 8192-token runs that eager attention cannot fit
- Preliminary Tau2Bench retail results: validation reward (mean@1) from 0.25 → 0.44 during the observed training window
- Demonstrates that environment interface design, RL dataflow, and attention-kernel co-optimization are jointly necessary for memory-feasible long-horizon agent RL

## Relevance

This directly advances the agentic RL + tool use thread established by GAP (task-dependency-structure axis) and HARTS (prefix-sharing rollout efficiency). SINKFLEX-RL occupies a fourth axis: training infrastructure — specifically, that GRPO without a value model requires co-designed attention kernels and rollout dataflow to remain memory-feasible at the long context lengths that multi-turn tool-use generates. The sink normalization insight also extends the OTB/Q-RM token-level heterogeneity thread to the attention-mechanics level.

## My Thoughts

<!-- Add your own notes here -->
