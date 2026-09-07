---
title: "DiDPO: Diff-in-Diff Policy Optimization for Coding Agent Training"
authors: ["Xucong Wang", "Zhe Zhao", "Liheng Yu", "Di Wu", "Xiaofeng Cao", "Pengkun Wang"]
date: 2026-09-07
arxiv_id: "2608.07147v1"
url: "https://arxiv.org/abs/2608.07147"
score: 0.79
topics: [agentic RL, LLM agent, tool use, GRPO, reinforcement learning, RL training]
status: unread
---

# DiDPO: Diff-in-Diff Policy Optimization for Coding Agent Training

## Summary

DiDPO constructs fine-grained credit units from code diff structure rather than outcome rewards or turn-level signals, using a groupability score to split code diffs into anchors that optimally balance semantic scope and group mass. Advantages are computed at the diff level and projected back to individual response tokens, making the independent contribution of each code change distinguishable during GRPO training. On Qwen2.5-7B-Coder, DiDPO exceeds comparable coding agent RL methods by over 10% and substantially narrows the gap with much larger models on long-horizon coding and reasoning benchmarks.

## Key Contributions

- Groupability score: splits code diffs into anchors that balance semantic scope and group mass, discovering cross-trajectory sub-diff similarity without manual annotation
- Diff-level advantage computation projected back to response tokens — fine-grained credit at the level of independent code changes
- Multi-turn coding agent RL: organizes interactions into thought-action steps and analyzes diffs across sampled trajectories
- Qwen2.5-7B-Coder: >10% over comparable methods; narrows gap to much larger models on long-horizon coding and reasoning

## Relevance

DiDPO extends the credit assignment thread (OTB per-token advantage reweighting, DARS planner-level prefix-gated reward, VICT verifier-side tracing) to the coding domain: the diff structure provides a natural semantic unit for credit that is richer than token-level but more precise than turn-level, analogous to how StructReward uses reasoning field boundaries. The groupability score's anchor discovery is structurally analogous to VICT's verifier-atom extraction — both identify semantically coherent units for advantage redistribution without human annotation.

## My Thoughts

<!-- Add your own notes here -->
