---
title: "EDGE: Experience-Distillation for Guided Exploration in Agentic Reinforcement Learning"
authors: ["Can Xie", "Yuyi Zhou", "Wen Yang", "Ziyi zhang", "Siyao Song", "Yingzhuo Deng", "Shuo Ren", "Jiajun Zhang"]
date: 2026-08-22
arxiv_id: "2608.21946v2"
url: "http://arxiv.org/abs/2608.21946v2"
score: 0.85
topics: [agentic RL, RL training, LLM agent, tool use, GRPO]
status: unread
---

# EDGE: Experience-Distillation for Guided Exploration in Agentic Reinforcement Learning

## Summary

EDGE treats retrieved historical experiences as temporary training-time scaffolds rather than persistent inference-time context, partitioning each rollout group into experience-conditioned and experience-free trajectories to admit only positive marginal gains, then distilling the induced behavior into the base policy via reverse-KL on its own empirical support. A co-evolutionary experience bank synthesizes new guidance from emerging failure modes and prunes obsolete entries as the policy evolves. Across embodied, web, and search-based QA tasks, EDGE improves over strong RL baselines by up to 12.5 points and remains effective without inference-time scaffolds.

## Key Contributions

- Frames experiences as training-time scaffolds (not inference-time retrieval), avoiding persistent inference dependencies
- Positive marginal gain estimation: compares experience-conditioned vs. experience-free rollout groups before distilling
- Reverse-KL distillation on empirical support internalizes experience-induced behavior into parametric policy
- Co-evolutionary experience bank: synthesizes from failure modes, prunes obsolete entries as policy capability advances

## Relevance

EDGE sits at the intersection of the skill-evolution thread (SkillForge, Skill-R1, Skill1 — Aug 26) and the experience-reuse thread, but with a crucial architectural difference: unlike SkillForge's append-based skill library or Skill-R1's separate generator, EDGE internalizes experience directly into the base policy parameters via distillation. This is the same internalization objective as SKILL0 (curriculum withdrawal) but achieved via distillation rather than reward shaping — suggesting multiple paths to the same "experience-free inference" goal.

## My Thoughts

<!-- Add your own notes here -->
