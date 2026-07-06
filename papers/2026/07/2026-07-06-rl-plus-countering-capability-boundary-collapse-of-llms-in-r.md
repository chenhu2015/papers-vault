---
title: "RL-PLUS: Countering Capability Boundary Collapse of LLMs in Reinforcement Learning with Hybrid-policy Optimization"
authors: ["Yihong Dong", "Xue Jiang", "Yongding Tao", "Huanyu Liu", "Kechi Zhang", "Lili Mou", "Rongyu Cao", "Yingwei Ma", "Jue Chen", "Binhua Li", "Zhi Jin", "Fei Huang", "Yongbin Li", "Ge Li"]
date: 2025-07-31
arxiv_id: "2508.00222v5"
url: "http://arxiv.org/abs/2508.00222v5"
score: 0.72
topics: [RL training, reinforcement learning, PPO, RLHF, agentic RL]
status: unread
---

# RL-PLUS: Countering Capability Boundary Collapse of LLMs in Reinforcement Learning with Hybrid-policy Optimization

## Summary

RL-PLUS identifies "capability boundary collapse" as a failure mode distinct from information self-locking (SeL/AREW): RLVR's on-policy sampling combined with the LLM's vast action space and sparse reward narrows rather than expands the model's problem-solving scope. The paper addresses this with a hybrid-policy approach combining Multiple Importance Sampling (to handle distributional mismatch when incorporating external data) and an Exploration-Based Advantage Function (to steer training toward high-value unexplored reasoning paths), yielding up to 69.2% relative improvement over RLVR on six math reasoning benchmarks and six OOD reasoning tasks.

## Key Contributions

- "Capability boundary collapse" failure mode diagnosis: RLVR's on-policy constraint concentrates training on problems the current policy nearly solves, causing the policy to narrow its scope rather than broaden it
- Multiple Importance Sampling to safely incorporate off-policy external data into RLVR, correcting distributional mismatch with theoretical guarantees
- Exploration-Based Advantage Function that identifies high-value unexplored reasoning paths and biases the advantage signal toward them
- State-of-the-art on six math reasoning benchmarks; up to 69.2% relative improvement; consistent gains across Qwen/Llama/other model families

## Relevance

RL-PLUS names a third pathological failure mode in RLVR (alongside information self-locking from SeL/AREW and gradient vanishing/diversity collapse from TA-GRPO), forming a complementary triad: SeL is about the reward signal preventing useful trajectories from being generated at all, diversity collapse is about group-level gradient degeneracy, and capability boundary collapse is about on-policy scope restriction. RL-PLUS's Exploration-Based Advantage Function is structurally the most direct complement to AREW's directional critique reweighting — both target underexplored high-value reasoning paths but from advantage design vs. reward shaping.

## My Thoughts

<!-- Add your own notes here -->
