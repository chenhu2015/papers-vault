---
title: "SCOPE-RL: Optimizing Reasoning Paths Before and After Success"
authors: ["Xiaojian Liu", "Han Xu", "Jianqiang Xia", "Zhixuan Li", "Ke Xu", "Yiwei Dai", "Xinran Chen", "Changwo Wu", "Yuchen Li"]
date: 2026-07-13
arxiv_id: "2607.11506v2"
url: "http://arxiv.org/abs/2607.11506v2"
score: 0.83
topics: [GRPO, RLHF, reward model, agentic RL, reinforcement learning]
status: unread
---

# SCOPE-RL: Optimizing Reasoning Paths Before and After Success

## Summary

Two-stage RLVR framework densifying sparse outcome rewards: Adaptive Scaffolded RL adds prefix-decomposed verifiable sub-question rewards before success, while Quality-Aware Process RL applies correctness-gated process-shape rewards to refine correct trajectories after success. Achieves 11.2pp accuracy improvement and 27.1% token reduction over outcome-only GRPO on Qwen3-8B-Instruct, with gains complementary to policy-update-level RLVR advances like GSPO. An expert-validated Step-Quality Evaluation Protocol measures useful-step density, error localization, and token efficiency.

## Key Contributions

- Explicitly separates the reward densification problem into pre-success (prerequisite progress, hard problems with no reward signal) and post-success (trajectory quality, redundant/flawed correct paths) phases
- Adaptive Scaffolded RL decomposes hard problems into sub-question chains with prefix-verifiable rewards, giving credit before the final answer is reached
- Quality-Aware Process RL uses correctness gating to apply process-shape rewards only to successful trajectories, avoiding noise from failed attempts
- Introduces Step-Quality Evaluation Protocol with useful-step density, error localization, and token efficiency metrics beyond final accuracy

## Relevance

Directly extends the step-credit cluster (24 entries as of Oct 23) with the cleanest pre/post-success framing yet; the two-stage split is distinct from ReAPO's retry-aware SSP framing (which treats multi-attempt rollouts as dependent) and from TAR's diversity preservation. The "before success" scaffolded reward angle addresses the gap that VCBM (causal-chain credit) targets but from a decomposed-subproblem rather than episodic-memory direction.

## My Thoughts

<!-- Add your own notes here -->
