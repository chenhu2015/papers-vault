---
title: "LongRCA Bench: Diagnosing Responsible Roles and Root Causes in Long-Horizon Agent Failures"
authors: ["Yunfei Zhang", "Boyu Feng", "Changhua Pei", "Zexin Wang"]
date: 2026-08-18
arxiv_id: "2608.15242"
url: "http://arxiv.org/abs/2608.15242v1"
score: 0.83
topics: [agentic RL, LLM agent, agentic evaluation, long-horizon]
status: unread
---

# LongRCA Bench: Diagnosing Responsible Roles and Root Causes in Long-Horizon Agent Failures

## Summary

LongRCA Bench provides 1,140 failed long-horizon agent trajectories (median 145 steps) with human labels for both the responsible role and the earliest decisive root-cause step, treating these as separate attribution targets. The strongest baseline reaches only 13.2% exact root-step accuracy; the proposed RCTA method (segment-summary retrieval + handoff-instruction tracing) improves to 51.1% responsible-role and 24.1% exact root-step accuracy. This benchmark formalises the repair-assignment gap: the same visible failure may call for model post-training, harness engineering, or environment redesign depending on where the root cause originated.

## Key Contributions

- LongRCA Bench: 1,140 failed trajectories across five domains, no injected errors, median 145 steps, dual human labels (responsible role + earliest decisive step)
- Establishes that responsible-role accuracy and exact root-step accuracy are separate, independently hard targets (SOTA 51.1% / 24.1%)
- RCTA: training-free method using segment summaries + handoff-instruction tracing to retrieve and localize root-cause steps
- Shows existing failure-attribution benchmarks are too short to capture the real diagnosis difficulty in long-horizon settings

## Relevance

LongRCA Bench directly extends the Aug 17 cascade analysis thread (OrchestraBench + Layer-Isolated Evaluation): OrchestraBench separates model from scaffold at the aggregate level; Layer-Isolated decomposes scaffold layers; LongRCA Bench now provides step-level and role-level ground truth for where inside a long trajectory the decisive fault entered. The responsible-role dimension maps directly onto the "Model or Harness?" taxonomy (Aug 18), completing a three-level failure attribution stack: component taxonomy → cascade diagnosis → root-cause localization.

## My Thoughts

<!-- Add your own notes here -->
