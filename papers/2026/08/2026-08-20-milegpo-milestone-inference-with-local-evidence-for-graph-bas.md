---
title: "MileGPO: Milestone Inference with Local Evidence for Graph-Based Policy Optimization of Long-Horizon LLM Agents"
authors: ["Bo Qian", "Yuting Wu", "Shuang Zeng", "Huaiyu Wan", "Dalin Zhang", "Jiqiang Liu"]
date: 2026-08-20
arxiv_id: "2608.19803v2"
url: "http://arxiv.org/abs/2608.19803v2"
score: 0.85
topics: [agentic RL, RL training, LLM agent, reward model]
status: unread
---

# MileGPO: Milestone Inference with Local Evidence for Graph-Based Policy Optimization of Long-Horizon LLM Agents

## Summary

MileGPO derives process-level credit from grouped on-policy rollouts via three components: Milestone Discovery identifies candidate milestones on successful rollouts and recurring traps on failed ones; Reliability-Calibrated Shaping (RCS) weights candidates by outcome-based confidence; Progress-Contrastive Calibration (PCC) tests whether a candidate reflects local progress relative to same-state alternatives. No auxiliary models or additional environment interaction are required. Experiments on ALFWorld and WebShop show state-of-the-art performance with a small in-distribution to out-of-distribution gap.

## Key Contributions

- Milestone Discovery: identifies positive milestones from successful trajectories and negative traps from failures — bidirectional signal
- RCS: outcome-based confidence weighting to down-weight uncertain milestone candidates
- PCC: local progress test using same-state branch evidence to reject candidates that merely coincide with good outcomes
- Ablation shows all three components are complementary; credit diagnostics provided

## Relevance

Fifth distinct approach to step-level credit for agentic GRPO alongside GRAFT (Bellman/graph), SALT (plug-and-play graph), ProCredit (verifiable-progress), and TIGPO (temporal graph). MileGPO's milestone-based framing is semantically richer than pure graph edges — it specifically identifies *turning points* in task completion, which maps onto the same intuition as Belief-Shift Branching's value-curve pivots.

## My Thoughts

<!-- Add your own notes here -->
