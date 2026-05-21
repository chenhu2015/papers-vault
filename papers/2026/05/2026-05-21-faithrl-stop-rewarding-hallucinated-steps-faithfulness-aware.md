---
title: "Stop Rewarding Hallucinated Steps: Faithfulness-Aware Step-Level Reinforcement Learning for Small Reasoning Models"
authors: ["Shuo Nie", "Hexuan Deng", "Chao Wang", "Ruiyu Fang", "Xuebo Liu", "Shuangyong Song", "Yu Li", "Min Zhang", "Xuelong Li"]
date: 2026-02-05
arxiv_id: "2602.05897v1"
url: "http://arxiv.org/abs/2602.05897v1"
score: 0.80
topics: [reward model, RLHF, PPO, RL training, reinforcement learning]
status: unread
---

# Stop Rewarding Hallucinated Steps: Faithfulness-Aware Step-Level Reinforcement Learning for Small Reasoning Models

## Summary

FaithRL identifies a failure mode where outcome-based RL inadvertently reinforces unfaithful reasoning steps when the final answer happens to be correct. It introduces step-level faithfulness rewards from a process reward model combined with implicit truncated resampling—generating contrastive signals from faithful prefixes of the reasoning chain. FaithRL consistently reduces hallucinations in both chain-of-thought steps and final answers across multiple small reasoning models.

## Key Contributions

- Diagnoses the failure mode: outcome-reward RL reinforces unfaithful CoT when final answer is accidentally correct
- Step-level faithfulness reward from a PRM targeting intermediate reasoning quality
- Truncated resampling generates contrastive signals from faithful prefixes without expensive additional rollouts
- Demonstrated across multiple small reasoning models on Open-Book QA benchmarks

## Relevance

Direct extension of the step-level credit assignment thread (SRaR from May 19, PAIR from May 19) into the faithfulness/hallucination domain. FaithRL applies PRM-style process supervision specifically to detect and penalize unfaithful intermediate reasoning steps, complementing SRaR's rubric-attribution approach.

## My Thoughts

<!-- Add your own notes here -->
