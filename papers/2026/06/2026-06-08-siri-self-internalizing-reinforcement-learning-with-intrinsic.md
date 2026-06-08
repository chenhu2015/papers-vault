---
title: "SIRI: Self-Internalizing Reinforcement Learning with Intrinsic Skills for LLM Agent Training"
authors: ["Zhongyu He", "Yuanfan Li", "Fei Huang", "Tianyu Chen", "Siyuan Chen", "Xingyang Li", "Meng Hsuan Yu", "Xiangrong Liu", "Leyi Wei", "Lu Pan", "Ke Zeng", "Xunliang Cai"]
date: 2026-06-01
arxiv_id: "2606.02355v1"
url: "http://arxiv.org/abs/2606.02355v1"
score: 0.85
topics: [agentic RL, LLM agent, tool use, RL training, reinforcement learning]
status: unread
---

# SIRI: Self-Internalizing Reinforcement Learning with Intrinsic Skills for LLM Agent Training

## Summary

SIRI is a three-phase framework for LLM agent training that enables skills to be discovered, validated, and internalized without external skill generators or inference-time skill banks. The agent uses GiGPO warmup, then self-mines compact skills from its own successful rollouts and validates them via paired skill-augmented vs. skill-free rollouts, and finally distills only beneficial skill-guided action tokens back into the plain policy. On ALFWorld and WebShop with Qwen2.5-7B, SIRI improves GiGPO from 0.908→0.930 and 0.728→0.813 respectively, with no inference overhead.

## Key Contributions

- Three-phase pipeline (warmup → self-skill-mining → selective distillation) that closes the skill loop entirely within the training agent
- Self-skill mining: policy summarizes skills from its own successful plain rollouts, validated via paired skill-augmented/skill-free rollout comparison
- Trajectory-level utility + action-level advantage filters that distill only beneficial skill-guided tokens into the plain policy
- Matches or exceeds distillation from closed-source large models using only the agent's own self-mined skills

## Relevance

This directly resolves the Skill0.5 runner-up thread from June 7 (agentic RL skill internalization for OOD generalization) and the broader SIRI/SUPERNOVA question of how learned behaviors become durable after RL training. The self-internalizing framing is a clean answer to a key open problem in the June 6–7 digests.

## My Thoughts

<!-- Add your own notes here -->
