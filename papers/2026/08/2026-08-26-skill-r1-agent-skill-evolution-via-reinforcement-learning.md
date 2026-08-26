---
title: "Skill-R1: Agent Skill Evolution via Reinforcement Learning"
authors: ["Yash Vishe", "Rohan Surana", "Xunyi Jiang", "Zihan Huang", "Xintong Li", "Nikki Lijing Kuang", "Tong Yu", "Ryan A. Rossi", "Jingbo Shang", "Julian McAuley", "Junda Wu"]
date: 2026-05-10
arxiv_id: "2605.09359v1"
url: "http://arxiv.org/abs/2605.09359v1"
score: 0.82
topics: [agentic RL, RL training, GRPO, tool use, LLM agent]
status: unread
---

# Skill-R1: Agent Skill Evolution via Reinforcement Learning

## Summary

Skill-R1 trains a lightweight skill generator (not the task LLM) on task context, prior rollouts, and verified outcomes to produce skills that steer a frozen task LLM, preserving compatibility with closed-source models. The bi-level GRPO objective combines intra-generation (rollouts under same skill) and inter-generation (revisions across rounds) advantages to optimize the recurrent skill revision process rather than one-shot self-refinement. Achieves consistent gains on verifiable-reward benchmarks, with particularly strong improvements on complex multi-step tasks.

## Key Contributions

- Separates skill generation from task execution: a lightweight skill generator is trained while the task LLM is frozen, enabling black-box compatibility
- Formulates skill evolution as a recurrent multi-generation process with two coupled credit levels: skill quality and revision quality
- Bi-level GRPO: intra-generation term compares rollouts under shared skill conditioning; inter-generation term rewards revisions that improve behavior across successive rounds
- Consistent gains across verifiable-reward benchmarks, strongest on complex multi-step tasks

## Relevance

Skill-R1's bi-level GRPO for recurrent skill revision is structurally related to Skill1's (also today) frequency-decomposed single-signal credit, but takes the opposite architectural stance: Skill1 uses one policy and one signal; Skill-R1 uses two objectives and separates generator from executor. Together with SkillForge (today, continuous verification) and SPyCE (Aug 23, co-evolution), this digest completes the skill-reuse design space: Skill-R1 covers the closed-source / frozen-LLM corner that SPyCE and SkillForge do not address.

## My Thoughts

<!-- Add your own notes here -->
