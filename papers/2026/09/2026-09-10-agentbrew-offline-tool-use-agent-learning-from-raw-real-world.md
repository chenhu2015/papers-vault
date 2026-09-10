---
title: "AgentBrew: Offline Tool-Use Agent Learning from Raw Real-World Trajectories"
authors: ["Zhiyi Lyu", "Yewen Li", "Longtao Zheng", "Shengtian Yang", "Lang Feng", "Lei Feng", "Peng Jiang", "Kun Gai", "Qingpeng Cai", "Bo An"]
date: 2026-09-10
arxiv_id: "2609.05837v1"
url: "https://arxiv.org/abs/2609.05837v1"
score: 0.83
topics: [agentic RL, tool use, LLM agent, RLAIF]
status: unread
---

# AgentBrew: Offline Tool-Use Agent Learning from Raw Real-World Trajectories

## Summary

AgentBrew trains tool-use LLM agents offline from a single batch of raw interaction trajectories, without task verifiers or simulators. It uses retrospective task inference (reconstruct the task instruction from the trajectory's actual outcome) combined with PMI-based credit assignment (decompose the trajectory's total information into per-action credits via pointwise mutual information) to weight the policy training objective. On three real-world MCP applications (GitHub, Notion, PostgreSQL), fine-tuning Qwen3-32B with AgentBrew surpasses the prompted Qwen3-235B and outperforms rejection-sampling baselines.

## Key Contributions

- **Retrospective task inference**: for each raw trajectory, an aligned instruction is reconstructed from its actual outcome rather than requiring pre-specified tasks
- **PMI-based per-action credit assignment**: decomposes trajectory's total mutual information with the inferred instruction into additive per-action credits, amplifying informative actions and suppressing ineffective ones
- **No verifier, no simulator, no iterative rollout**: training works from a single batch of unfiltered real-world trajectories
- **Real-world MCP validation**: GitHub, Notion, PostgreSQL benchmarks; Qwen3-32B post-trained with AgentBrew outperforms prompted Qwen3-235B (+2.3 Acc / +4.4 Score) and rejection sampling

## Relevance

Directly addresses the SFT-free VLM RL open gap from an offline credit-assignment angle: AgentBrew avoids both task verifiers and online rollouts by inferring supervision from trajectory outcomes, making it a complementary approach to DMPO (occupancy-measure multi-turn DPO) and Auto-Dreamer (offline GRPO memory). The PMI credit assignment is also structurally related to the execution-artifact credit thread (ExecCritic, ERPO) but applied to raw multi-turn tool-use trajectories.

## My Thoughts

<!-- Add your own notes here -->
