---
title: "EvoCUA-1.5: Online Reinforcement Learning for Multi-turn Computer-Use Agents"
authors: ["Mianqiu Huang", "Taofeng Xue", "Chong Peng", "Jinrui Ding", "Jie Yang", "Sicheng Fan", "Jiale Hong", "Yufei Gao", "Xiaocheng Zhang", "Linsen Guo", "Xin Yang", "Dengchang Zhao", "Yuchen Xie", "Peng Pei", "Xunliang Xie", "Xipeng Qiu"]
date: 2026-07-07
arxiv_id: "2607.09773v2"
url: "https://arxiv.org/abs/2607.09773"
score: 0.85
topics: [agentic RL, LLM agent, tool use, RL training, PPO]
status: unread
---

# EvoCUA-1.5: Online Reinforcement Learning for Multi-turn Computer-Use Agents

## Summary

Extends computer-use agents from offline imitation to online RL in sandbox environments via STEPO (Step-Level Policy Optimization that preserves trajectory-level advantage balance after decomposition into per-step samples), DTAC curriculum (combining learnable tasks, difficult-positive replay, and controlled infeasible-task exposure), and fully asynchronous infrastructure with staleness control. Achieves 63.2% on OSWorld-Verified, outperforming comparable open-weight 32B/35B models and approaching much larger ones.

## Key Contributions

- STEPO: step-level decomposition of trajectory advantages without losing trajectory-level balance, solving the sparse-terminal-reward challenge for long multi-turn episodes
- DTAC (Dynamic Tri-Adaptive Curriculum): simultaneously handles learnable-task selection, difficult-positive replay, and infeasible-task exposure — a three-component curriculum for computer use
- Asynchronous rollout infrastructure with staleness control and mini-group batching for GPU efficiency during slow environment feedback
- 63.2% on OSWorld-Verified, strong relative to scale

## Relevance

Directly relevant to the agentic RL thread — provides a concrete implementation of online RL for long-horizon tool-use agents that the ACLArena / MATCH / PAC curriculum papers study abstractly. DTAC is a real-world instance of the multi-level curriculum gap identified in prior digests, making this a useful empirical grounding point. STEPO's step-level advantage decomposition is relevant to the ECHO credit assignment thread.

## My Thoughts

<!-- Add your own notes here -->
