---
title: "SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn Reinforcement Learning"
authors: ["Bo Liu", "Leon Guertler", "Simon Yu", "Zichen Liu", "Penghui Qi", "Daniel Balcells", "Mickel Liu", "Cheston Tan", "Weiyan Shi", "Min Lin", "Wee Sun Lee", "Natasha Jaques"]
date: 2025-06-30
arxiv_id: "2506.24119"
url: "https://arxiv.org/abs/2506.24119"
score: 0.82
topics: [agentic RL, RL training, reinforcement learning, LLM agent, RLHF]
status: unread
---

# SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn Reinforcement Learning

## Summary

SPIRAL trains LLMs to reason by having them play multi-turn zero-sum games (TicTacToe, Kuhn Poker, Simple Negotiation) against progressively stronger versions of themselves, providing an automatic curriculum without human supervision. The key algorithmic contribution is role-conditioned advantage estimation (RAE), which stabilises multi-agent RL by conditioning advantage estimates on each agent's role. Multi-game training outperforms single-game training, yielding up to 10% gains across 8 reasoning benchmarks on 4 model families including DeepSeek-R1-Distill variants.

## Key Contributions

- Role-conditioned advantage estimation (RAE) for stable multi-agent RL training — solves the credit assignment instability when one model plays multiple roles
- Fully online multi-turn multi-agent RL system for LLMs, eliminating need for expert game trajectories
- Multi-game curriculum (TicTacToe + Kuhn Poker + Negotiation) yields stronger transfer than single-game training
- Reasoning gains transfer broadly across diverse benchmarks and model architectures, including already-RLVR-trained models like DeepSeek-R1-Distill-Qwen-7B

## Relevance

Directly advances the agentic RL thread: SPIRAL shows that zero-sum self-play games can replace verifiable-reward RLVR as a training signal, generating a natural curriculum. The RAE stabilisation technique is directly applicable to any multi-agent RL training setup for LLMs, complementing the GRPO/DAPO curriculum papers (METIS, AdaCuRL, VCRL) from May 13 by providing an entirely orthogonal curriculum source.

## My Thoughts

<!-- Add your own notes here -->
