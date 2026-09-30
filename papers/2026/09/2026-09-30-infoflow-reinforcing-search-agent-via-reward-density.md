---
title: "InfoFlow: Reinforcing Search Agent Via Reward Density Optimization"
authors: ["Kun Luo", "Hongjin Qian", "Zheng Liu", "Ziyi Xia", "Shitao Xiao", "Siqi Bao", "Jun Zhao", "Kang Liu"]
date: 2026-09-30
arxiv_id: "2510.26575v1"
url: "http://arxiv.org/abs/2510.26575v1"
score: 0.76
topics: [agentic RL, LLM agent, reward model, tool use]
status: unread
---

# InfoFlow: Reinforcing Search Agent Via Reward Density Optimization

## Summary

InfoFlow formalises the sparse-reward problem in deep search as Reward Density Optimization and attacks it from three angles: subproblem decomposition assigns process rewards along the trajectory, failure-guided hints inject corrective signals into stalled rollouts, and a dual-agent refiner compresses search history to reduce apparent exploration cost. Applied to agentic deep search benchmarks, lightweight LLMs with InfoFlow match performance of advanced proprietary models.

## Key Contributions

- **Reward Density Optimization framework**: formally defines the challenge as maximising reward per unit exploration cost, rather than simply treating it as sparse reward
- **Subproblem decomposition**: breaks long-range search tasks into subtasks with intermediate process rewards — denser training signal for multi-hop retrieval
- **Failure-guided hints**: injects corrective guidance into stalled trajectories, increasing the probability of successful outcomes without off-policy demonstrations
- **Dual-agent refinement**: a refiner agent synthesises search history before the researcher agent, compressing perceived trajectory length and boosting reward density

## Relevance

InfoFlow addresses the same "reward too sparse for long-horizon agents" problem that credit assignment papers (ASCT, CRR, TEMPO) tackle, but from the reward shaping side rather than the credit assignment side. The subproblem decomposition is architecturally adjacent to PilotRL's staged curriculum; both try to provide denser learning signal for agentic RL without requiring a verifiable step-level oracle.

## My Thoughts

<!-- Add your own notes here -->
