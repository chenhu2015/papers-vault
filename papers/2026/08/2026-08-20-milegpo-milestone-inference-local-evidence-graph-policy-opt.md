---
title: "MileGPO: Milestone Inference with Local Evidence for Graph-Based Policy Optimization of Long-Horizon LLM Agents"
authors: ["Bo Qian", "Yuting Wu", "Shuang Zeng", "Huaiyu Wan"]
date: 2026-08-20
arxiv_id: "2608.19803"
url: "https://arxiv.org/abs/2608.19803"
score: 0.89
topics: [agentic RL, reward model, LLM agent, GRPO]
status: unread
---

# MileGPO: Milestone Inference with Local Evidence for Graph-Based Policy Optimization of Long-Horizon LLM Agents

## Summary

MileGPO addresses credit assignment in long-horizon agentic RL by inferring process-level credits from grouped on-policy rollouts without auxiliary models. Three mechanisms—Milestone Discovery (candidate milestones on successes, traps on failures), Reliability-Calibrated Shaping (outcome-based confidence weighting), and Progress-Contrastive Calibration (local progress test against same-state alternatives)—work together to resolve ambiguous intermediate credit. Achieves state-of-the-art on ALFWorld and WebShop with a small in-distribution to out-of-distribution gap.

## Key Contributions

- Milestone Discovery: identifies candidate milestones on successful rollouts and recurring traps on failed ones from grouped rollouts
- Reliability-Calibrated Shaping (RCS): weights milestone candidates by outcome-based confidence, strengthening reliable signals and down-weighting uncertain ones
- Progress-Contrastive Calibration (PCC): tests whether a candidate reflects local progress relative to observed same-state alternatives
- No auxiliary models or additional environment interaction required; SOTA on ALFWorld and WebShop

## Relevance

MileGPO addresses a third axis of the agentic RL credit assignment problem — sparse intermediate signals — complementing SkillGate (Aug 20, selector credit starvation) and RTPO (Aug 20, temporal credit across turns). However, this paper should be read alongside "Credit Without Ground Truth" (Aug 20): MileGPO's milestone signals are inferred from rollout groups, not validated against causal ground truth, so they may track correctness rather than contribution. The PCC mechanism (comparing against same-state alternatives) is the closest to causal validity of any signal in the current vault.

## My Thoughts

<!-- Add your own notes here -->
