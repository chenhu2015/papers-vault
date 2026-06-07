---
title: "Generate, Filter, Control, Replay: A Comprehensive Survey of Rollout Strategies for LLM Reinforcement Learning"
authors: ["Rohan Surana", "Gagan Mundada", "Xunyi Jiang", "Chuhan Wang", "Zhenwei Tang", "Difan Jiao", "Zihan Huang", "Yuxin Xiong", "Junda Wu", "Sheldon Yu", "Xintong Li", "Raghav Jain", "Nikki Kuang", "Sizhe Zhou", "Bowen Jin", "Zhendong Chu", "Tong Yu", "Ryan Rossi", "Kuan-Hao Huang", "Jingbo Shang", "Jiawei Han", "Julian McAuley"]
date: 2026-06-07
arxiv_id: "2605.02913v1"
url: "http://arxiv.org/abs/2605.02913v1"
score: 0.81
topics: [RL training, reinforcement learning, agentic RL, reward model, tool use, GRPO, PPO]
status: unread
---

# Generate, Filter, Control, Replay: A Comprehensive Survey of Rollout Strategies for LLM Reinforcement Learning

## Summary

This survey formalises the rollout pipeline for RL-based post-training through a Generate-Filter-Control-Replay (GFCR) taxonomy, decomposing rollout design into four modular stages covering trajectory generation, verifier/critic filtering, compute control, and self-evolving replay. It synthesises methods across verifiable rewards, process supervision, tree/segment rollouts, adaptive compute allocation, early-exit policies, and replay-based self-improvement curricula, grounded in case studies spanning math, code, multimodal, tool-using agents, and agentic skill benchmarks. A diagnostic index maps common rollout pathologies (entropy collapse, all-correct batches, reward hacking) to GFCR modules and mitigation levers.

## Key Contributions

- GFCR taxonomy: Generate (trajectory/topology), Filter (verifier/judge/critic signals), Control (compute allocation, branching, stopping), Replay (artifact reuse, self-evolving curricula)
- Criterion taxonomy of reliability, coverage, and cost sensitivity for characterising rollout trade-offs
- Synthesis of methods spanning verifiable rewards, process supervision, judge gating, adaptive compute, early-exit, and replay/self-improvement
- Diagnostic index mapping common rollout pathologies to GFCR modules and mitigations

## Relevance

Provides a unifying lens over many papers covered in recent digests: POPO (off-policy replay = Replay stage), EchoRL (rollout echoing = Replay), DARTS (rollout shaping = Control), EP-GRPO/M-GRPO (filtering via entropy = Filter), Turn-PPO (multi-turn = Generate topology). The GFCR framework helps situate the full trajectory of LLM RL papers across all recent sessions.

## My Thoughts

<!-- Add your own notes here -->
