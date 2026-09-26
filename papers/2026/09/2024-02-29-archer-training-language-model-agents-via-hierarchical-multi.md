---
title: "ArCHer: Training Language Model Agents via Hierarchical Multi-Turn RL"
authors: ["Yifei Zhou", "Andrea Zanette", "Jiayi Pan", "Sergey Levine", "Aviral Kumar"]
date: 2024-02-29
arxiv_id: "2402.19446"
url: "https://arxiv.org/abs/2402.19446"
score: 0.85
topics: [agentic RL, RL training, RLHF, PPO, LLM agent, reward model]
status: unread
---

# ArCHer: Training Language Model Agents via Hierarchical Multi-Turn RL

## Summary

ArCHer introduces a hierarchical RL framework for multi-turn LLM agents: a high-level off-policy value-based algorithm aggregates utterance-level rewards across turns, while a low-level RL algorithm uses this value function to train a token-level policy within each turn. This decoupling preserves the flexibility of single-turn methods (e.g., PPO) while enabling multi-turn credit assignment, long horizons, and delayed rewards. ArCHer achieves approximately 100x sample efficiency over prior multi-turn methods on LLM agent tasks, and scales with model capacity up to the 7B scale tested.

## Key Contributions

- Framework that runs two RL algorithms in parallel: high-level off-policy value-based RL (aggregates utterance rewards) + low-level RL (trains token policy using high-level value function)
- Decoupling enables existing single-turn methods (PPO, etc.) to be embedded as the low-level component without modification
- ~100x sample efficiency gain over existing multi-turn LLM RL methods on agent tasks
- Scales with model capacity; demonstrates the hierarchical structure generalizes across LLM sizes

## Relevance

ArCHer is a foundational multi-turn RL paper from Levine/Kumar that provides the theoretical grounding for the hierarchical value decomposition approach. The high-level/low-level split it proposes is the precursor to ideas explored in GRAFT (trajectory graph + Bellman) and ArCHer explicitly handles the delayed reward problem that GRPO workarounds (SALT, ProCredit) address differently. Worth reading as context for the full landscape.

## My Thoughts

<!-- Add your own notes here -->
