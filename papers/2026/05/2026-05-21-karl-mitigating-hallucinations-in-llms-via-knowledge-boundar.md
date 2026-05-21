---
title: "KARL: Mitigating Hallucinations in LLMs via Knowledge-Boundary-Aware Reinforcement Learning"
authors: ["Cheng Gao", "Cheng Huang", "Kangyang Luo", "Ziqing Qiao", "Shuzheng Si", "Huimin Chen", "Chaojun Xiao", "Maosong Sun"]
date: 2026-04-03
arxiv_id: "2604.22779v1"
url: "http://arxiv.org/abs/2604.22779v1"
score: 0.84
topics: [RLHF, reward model, agentic RL, RL training]
status: unread
---

# KARL: Mitigating Hallucinations in LLMs via Knowledge-Boundary-Aware Reinforcement Learning

## Summary

KARL introduces a Knowledge-Boundary-Aware Reward that estimates the model's evolving knowledge boundary online using within-group response statistics, rewarding correct answers or guided abstention dynamically rather than with a static signal. A two-stage RL training strategy first explores the knowledge boundary to escape the 'abstention trap,' then converts incorrect out-of-knowledge answers into abstentions without sacrificing accuracy. Results show superior accuracy-hallucination tradeoff across in-distribution and out-of-distribution benchmarks.

## Key Contributions

- Knowledge-Boundary-Aware Reward: online boundary estimation from within-group rollout statistics, enabling dynamic abstention rewards
- Two-stage RL training: Stage 1 explores boundary and bypasses the abstention trap; Stage 2 converts OOK incorrect answers to abstentions
- Maintains answer accuracy on in-knowledge questions while dramatically reducing hallucinations on out-of-knowledge ones
- Generalizes across in-distribution and OOD benchmarks without additional annotation

## Relevance

Directly advances the reward model and RLHF threads that have been central to the digest throughout May. The dynamic, boundary-aware reward design connects to the credit assignment cluster (PAIR, SRaR, MoCA) covered May 19, extending that thread into the factuality/hallucination domain.

## My Thoughts

<!-- Add your own notes here -->
