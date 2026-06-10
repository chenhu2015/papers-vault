---
title: "From Player to Master: Enhancing Test-Time Learning of LLM Agents via Reinforcement Learning over Memory"
authors: ["Yishuo Cai", "Xingyu Guo", "Xuancheng Huang", "Jinhua Du", "Can Huang", "Wenxuan Huang", "Wenhan Ma", "Yuyang Hu", "Aohan Zeng", "Jie Tang", "Xu Sun"]
date: 2026-06-07
arxiv_id: "2606.08656v1"
url: "http://arxiv.org/abs/2606.08656v1"
score: 0.80
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# From Player to Master: Enhancing Test-Time Learning of LLM Agents via Reinforcement Learning over Memory

## Summary

MemoPilot trains a plug-in memory-update copilot for frozen LLM agents by formulating memory updating as a multi-turn decision problem optimised end-to-end with multi-turn GRPO, introducing turn-wise reward signals and context-independent turn-level advantage estimation for stable multi-turn credit assignment. The approach adapts the memory-update process to downstream objectives without touching the frozen player model, enabling progressive test-time learning from sequential interactions. On multi-round Rock-Paper-Scissors and Limit Texas Hold'em, MemoPilot achieves top Elo ratings (1762 on LHE, 1590 on RPS) and outperforms all baselines including DeepSeek-V3.2.

## Key Contributions

- Memory-update copilot as a separate trainable module around a frozen LLM player
- Multi-turn GRPO with turn-wise rewards for memory decision optimisation
- Context-independent turn-level advantage estimation for finer-grained credit assignment
- Top Elo performance on two sequential game testbeds without modifying the player model

## Relevance

Directly extends the agentic RL thread (SIRI/ECPO — Jun 8) by separating the memory-management problem from the action-taking problem. Where SIRI internalises skills into the policy weights, MemoPilot internalises the *memory-update strategy* into a separate copilot — preserving flexibility of the frozen base agent while still enabling RL-based improvement. Also connects to InfoMem (today) which approaches memory-augmented RL from the reward-design side.

## My Thoughts

<!-- Add your own notes here -->
