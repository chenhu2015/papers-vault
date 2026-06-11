---
title: "TRACE: A Unified Rollout Budget Allocation Framework for Efficient Agentic Reinforcement Learning"
authors: ["Heming Zou", "Qi Wang", "Yun Qu", "Yuhang Jiang", "Lizhou Cai", "Yixiu Mao", "Ru Peng", "Xin Xu", "Weijie Liu", "Kai Yang", "Saiyong Yang", "Xiangyang Ji"]
date: 2026-06-11
arxiv_id: "2606.11119v1"
url: "http://arxiv.org/abs/2606.11119v1"
score: 0.81
topics: [agentic RL, GRPO, RLVR, LLM agent, RL training]
status: unread
---

# TRACE: A Unified Rollout Budget Allocation Framework for Efficient Agentic Reinforcement Learning

## Summary

RLVR for multi-turn agentic tasks suffers from insufficient reward contrast: trivially easy and impossible prompts both yield zero-variance feedback, and outcome-only rewards assign the same terminal signal to every turn in a rollout. TRACE models each ReAct thought-action-observation turn as a semantic tree node and allocates rollout budget to both prompt roots and intermediate turn-level prefixes most likely to yield mixed terminal rewards, guided by a shared conditional success probability predictor. The resulting tree-structured rollouts improve Qwen3-14B Multi-Hop QA accuracy by 2.8 points over competitive baselines at equal sampling cost.

## Key Contributions

- Tree-structured rollout model: each ReAct turn treated as a semantically distinct node with budget continuations
- Budget allocation extends from prompt roots to intermediate turn-level prefixes (not just prompt level)
- Shared generalizable predictor estimates conditional success probability from prefix histories
- +2.8 Multi-Hop QA accuracy over competitive baselines at equal cost for Qwen3-14B

## Relevance

Extends the SUPERNOVA (Jun 7) and query recycling insights from prompt-level to turn-level: contrast is the bottleneck, and it needs to be managed across the full tree of multi-turn interactions, not just at the prompt root. TRACE and query recycling are complementary — TRACE identifies the highest-contrast allocation targets, recycling ensures previously zero-contrast prompts get another chance.

## My Thoughts

<!-- Add your own notes here -->
