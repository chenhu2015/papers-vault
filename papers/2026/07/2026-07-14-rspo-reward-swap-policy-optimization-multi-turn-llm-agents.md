---
title: "RSPO: Reward-Swap Policy Optimization for Multi-Turn LLM Agents"
authors: ["Qiang Liu", "Taian Guo", "Ruizhi Qiao", "Xing Sun"]
date: 2026-07-06
arxiv_id: "2607.04713"
url: "https://arxiv.org/abs/2607.04713"
score: 0.82
topics: [agentic RL, RL training, LLM agent, GRPO, reward model]
status: unread
---

# RSPO: Reward-Swap Policy Optimization for Multi-Turn LLM Agents

## Summary

RSPO addresses sparse outcome rewards in multi-turn agents via a reward-swap mechanism: dense process rewards guide trajectory sampling diversity while the optimization objective is kept consistent with true sparse outcome rewards, avoiding the misalignment of surrogate-reward training. This dual-reward architecture is plugged into GRPO, PPO, and GiGPO and evaluated on WebShop and ALFWorld, achieving consistent multi-turn agent performance improvements over strong baselines in long-horizon tasks with sparse terminal feedback.

## Key Contributions

- Reward-swap mechanism: dense process rewards for sampling diversity, outcome rewards for optimization objective consistency
- Separates reward function for exploration (dense) from reward for optimization (outcome) — avoids surrogate misalignment
- Plug-in enhancement compatible with GRPO, PPO, and GiGPO without architectural changes
- Evaluated on multi-turn interactive agent benchmarks (WebShop, ALFWorld), not just math reasoning

## Relevance

RSPO directly addresses the credit assignment problem the vault has tracked in multi-turn agentic settings (HRM, Turn-Level Reward Jul 13, DART). The reward-swap insight is complementary to PAG's selective revision (which uses a generative verifier to gate rethinking) and Turn-Level Reward (which designs per-turn verification signals): RSPO uses dense rewards only for sampling exploration while maintaining the optimization objective's integrity. Its WebShop/ALFWorld evaluation extends the reward design thread beyond math reasoning to practical agentic tasks with real tool-use.

## My Thoughts

<!-- Add your own notes here -->
