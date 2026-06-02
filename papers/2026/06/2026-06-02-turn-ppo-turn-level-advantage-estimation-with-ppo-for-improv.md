---
title: "Turn-PPO: Turn-Level Advantage Estimation with PPO for Improved Multi-Turn RL in Agentic LLMs"
authors: ["Junbo Li", "Peng Zhou", "Rui Meng", "Meet P. Vadera", "Lihong Li", "Yang Li"]
date: 2025-12-18
arxiv_id: "2512.17008v2"
url: "http://arxiv.org/abs/2512.17008v2"
score: 0.87
topics: [agentic RL, RL training, PPO, LLM agent, agentic]
status: unread
---

# Turn-PPO: Turn-Level Advantage Estimation with PPO for Improved Multi-Turn RL in Agentic LLMs

## Summary

Turn-PPO reformulates multi-turn LLM agent training as a turn-level MDP rather than the standard token-level MDP, finding that GRPO's limitations in long-horizon agentic tasks stem partly from this inappropriate temporal abstraction. PPO outperforms GRPO in multi-turn settings, and turn-PPO further improves by computing advantages at the turn boundary rather than per-token. Results on WebShop and Sokoban validate the approach with and without long-reasoning components.

## Key Contributions

- Turn-level MDP formulation for multi-turn LLM agent RL (as opposed to standard token-level)
- Empirical comparison showing PPO outperforms GRPO in multi-turn agentic settings
- Turn-PPO variant of PPO operating at turn boundaries for improved advantage signal
- Validation on WebShop (web shopping) and Sokoban (planning) with and without CoT

## Relevance

Directly fills the multi-agent/multi-turn LLM RL carry-forward that failed for 3+ consecutive days; complements TRACER (May 31, cooperative multi-LLM) and CoRe-Code (May 29) with a PPO-focused multi-turn perspective, and provides a theoretical basis for why turn-level vs token-level abstraction matters.

## My Thoughts

<!-- Add your own notes here -->
