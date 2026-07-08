---
title: "TEMPO: Temporal Enforcement via Mode-Separated Policy Optimization for Trustworthy LLM Backtesting"
authors: ["Anonymous"]
date: 2026-07-08
arxiv_id: "2605.18843v1"
url: "https://arxiv.org/abs/2605.18843"
score: 0.72
topics: [RL training, GRPO, LLM agent, agentic RL]
status: unread
---

# TEMPO: Temporal Enforcement via Mode-Separated Policy Optimization for Trustworthy LLM Backtesting

## Summary

Proposes TEMPO, a GRPO-based training framework with two sequentially gated reward modes: a leakage-elimination mode (hard prerequisite) that drives post-cutoff knowledge claims to zero, followed by a performance mode that optimizes task accuracy once leakage reaches zero — the performance mode cannot activate until the compliance constraint is satisfied. Proves monotonic leakage reduction and convergence to the leak-free optimum; reduces temporal knowledge leakage from 2–13% to 0.6–3.7% across three prediction tasks and two models, improving task performance 6–13% where strong pre-cutoff signals exist.

## Key Contributions

- Two-mode sequential GRPO reward: leakage mode as hard prerequisite before performance mode, preventing the optimizer from trading compliance for accuracy
- Formal monotonic leakage reduction proof and convergence guarantee to the leak-free optimum
- Instance-specific temporal compliance formulation: same knowledge may be legitimate for one cutoff and a violation for another — the problem cannot be solved by knowledge unlearning
- Validates on three prediction tasks; leakage reduction generalizes across task difficulty levels

## Relevance

TEMPO is the third paper in the vault implementing mode-separated RL as an architectural primitive, alongside AutoTool's (Jul 7) dual-mode tool/no-tool reward and RL-PLUS's (Jul 6) hybrid-policy via Multiple Importance Sampling. All three treat the training signal as having two distinct regimes that require different optimization behaviors, and all three use GRPO as the base algorithm. The hard-prerequisite sequencing in TEMPO is structurally the strongest mode separation: unlike AutoTool (concurrent dual-mode exploration) or RL-PLUS (interpolated hybrid policy), TEMPO enforces a strict phase gate — suggesting mode-separation can be implemented as a phase schedule, a concurrent mixture, or an interpolated policy, each with different convergence properties.

## My Thoughts

<!-- Add your own notes here -->
