---
title: "Scaling Test-time Compute for LLM Agents"
authors: ["King Zhu", "Hanhao Li", "Siwei Wu", "Tianshun Xing", "Dehua Ma", "Xiangru Tang", "Minghao Liu", "Jian Yang", "Jiaheng Liu", "Yuchen Eleanor Jiang", "Changwang Zhang", "Chenghua Lin", "Jun Wang", "Ge Zhang", "Wangchunshu Zhou"]
date: 2025-06-15
arxiv_id: "2506.12928"
url: "https://arxiv.org/abs/2506.12928"
score: 0.78
topics: [agentic RL, RL training, LLM agent, RLHF]
status: unread
---

# Scaling Test-time Compute for LLM Agents

## Summary

Systematic first exploration of applying test-time scaling strategies (parallel sampling, sequential revision, verifiers, rollout diversity) to language agents. Key findings: (1) knowing when to reflect is critical — always-reflecting degrades performance; (2) list-wise verifier-and-merging outperforms point-wise approaches; (3) increasing rollout diversity consistently improves agent performance. The work bridges the TTS literature from math reasoning to agentic settings, identifying when and how compute should be allocated differently for agents.

## Key Contributions

- First systematic ablation of TTS strategies applied to language agents (not just math/coding)
- Identifies reflection timing as the decisive factor: indiscriminate reflection hurts long-horizon performance
- List-wise merging (verifier scores full ranked lists) outperforms single-candidate point-wise scoring
- Rollout diversity is the one TTS strategy that reliably improves agent task performance

## Relevance

Directly connects to the vault's LLMs-as-a-Jury finding (Jul 15) that diversity is the primary value-add over single-model verification — this paper confirms that principle in the agentic setting. The "when to reflect" finding mirrors RSPO's lesson about reward-swap: dense reflection (process rewards) at every step corrupts the optimization objective, and the same applies to agent reflection during execution. Pairs naturally with TTI (today) and General AgentBench (today) to build a complete picture of TTS for agents.

## My Thoughts

<!-- Add your own notes here -->
