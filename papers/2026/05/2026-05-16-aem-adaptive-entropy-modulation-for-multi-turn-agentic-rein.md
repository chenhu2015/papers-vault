---
title: "AEM: Adaptive Entropy Modulation for Multi-Turn Agentic Reinforcement Learning"
authors: ["Haotian Zhao", "Songlin Zhou", "Yuxin Zhang", "Stephen S. -T. Yau", "Wenyu Zhang", "Lun Tian", "Tianshu Zhu", "Yifeng Huang", "Yucheng Zeng", "Jingnan Gu", "Daxiang Dong", "Jianmin Wu"]
date: 2026-05-16
arxiv_id: "2605.00425v3"
url: "http://arxiv.org/abs/2605.00425v3"
score: 0.88
topics: [agentic RL, LLM agent, RL training, GRPO, reinforcement learning]
status: unread
---

# AEM: Adaptive Entropy Modulation for Multi-Turn Agentic Reinforcement Learning

## Summary

AEM lifts entropy dynamics from token level to response level in multi-turn agentic RL, deriving a supervision-free response-level uncertainty proxy that rescales advantages to naturally transition from exploration to exploitation. Under natural-gradient updates, entropy drift is governed by sampled-response advantage times its relative surprisal; AEM exploits this to achieve consistent gains on ALFWorld, WebShop, and SWE-bench-Verified across 1.5B–32B models without process reward models.

## Key Contributions

- Theoretical result: under natural-gradient RL, response-level entropy drift = advantage × relative surprisal of sampled response
- Practical response-level uncertainty proxy derived from this result, used to rescale advantages
- Supervision-free: no PRMs, no dense intermediate rewards, no auxiliary objectives needed
- Consistent gains across ALFWorld, WebShop, SWE-bench-Verified at 1.5B–32B; +1.4pp on state-of-the-art SWE RL framework

## Relevance

Addresses the credit assignment and exploration-exploitation balance problem in multi-turn agentic RL — a direct thread from May 12's credit assignment papers (VPR, GenAC) and May 13's curriculum RL (METIS, AdaCuRL). The response-level granularity argument is a key insight: token-level entropy is wrong for agents whose environment is affected by complete responses, not individual tokens.

## My Thoughts

<!-- Add your own notes here -->
