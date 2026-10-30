---
title: "RSIPO: Recursive Self-Improving Policy Optimization for Agentic Reinforcement Learning via Skill-Policy Co-Evolution"
authors: ["Fan Zhang", "Hao Wu", "Jinyang Wu", "Hongyu Qu", "Zheng Lian", "Xiao Luo", "Yefeng Zheng", "Bo Zhang", "Haoxuan Li", "Pheng-Ann Heng"]
date: 2026-10-30
arxiv_id: "2610.15772v1"
url: "http://arxiv.org/abs/2610.15772v1"
score: 0.87
topics: [agentic RL, RL training, LLM agent, GRPO, reinforcement learning]
status: unread
---

# RSIPO: Recursive Self-Improving Policy Optimization for Agentic Reinforcement Learning via Skill-Policy Co-Evolution

## Summary

RSIPO is a self-evolving agentic RL framework where agentic skills and the policy model co-evolve: the policy extracts skills from completed trajectories and is explicitly optimized for skill-generation through trajectory replay. It combines RLVR with on-policy self-distillation, using empirical Bayes shrinkage to calibrate trust in teacher scores since skill-enhanced guidance can sometimes be unreliable. On ALFWorld with Qwen2.5-7B, RSIPO achieves 98.6% success rate — 17.4% absolute improvement over standard GRPO.

## Key Contributions

- Skill-policy co-evolution: policy both uses and generates agentic skills within the same training loop
- Trajectory replay optimizes skill-generation capability explicitly, not just task-completion policy
- Empirical Bayes shrinkage for dynamic calibration of student trust in teacher scores
- 98.6% on ALFWorld (Qwen2.5-7B); 17.4% absolute improvement over GRPO; strong on search-based agentic tasks

## Relevance

RSIPO directly advances the long-horizon agentic RL thread (previously at 3 entries for 2+ weeks). The skill-policy co-evolution angle is qualitatively new: prior agentic RL papers in the vault treat skills/subgoals as fixed structure, while RSIPO makes skill generation itself a learned and optimized capability. The combination of RLVR with self-distillation echoes the credit assignment cluster, applied to the agentic setting.

## My Thoughts

<!-- Add your own notes here -->
