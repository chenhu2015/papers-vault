---
title: "IAPO: Influence-Aware Policy Optimization for Credit Assignment in Multi-Turn Service Agents"
authors: ["Bo Ren", "Yirong Mao", "Yi Yang", "Wenhui Que"]
date: 2026-08-25
arxiv_id: "2608.24588v2"
url: "http://arxiv.org/abs/2608.24588v2"
score: 0.84
topics: [agentic RL, RL training, reward model, LLM agent, tool use]
status: unread
---

# IAPO: Influence-Aware Policy Optimization for Credit Assignment in Multi-Turn Service Agents

## Summary

IAPO represents each RL rollout as a typed influence-dependency graph over trainable agent actions, with user and tool observations as evidence nodes, then converts support-use and failed-use structure into routing weights that redistribute the same trajectory-level advantage to individual turns without additional rollouts or external step-level supervision. Evaluated with Qwen3-4B and Qwen3-8B on τ²-Bench, UserBench, and AgentChangeBench, IAPO outperforms multi-turn RL baselines while preserving BFCL-v4 multi-turn function-calling performance. The graph-based redistribution addresses what SPA-RL's progress estimator tried to solve — but from a causal graph rather than a trained value function.

## Key Contributions

- Influence-dependency graph over completed rollout: typed edges between agent actions and user/tool evidence nodes
- Support-use and failed-use classification converts graph structure to advantage routing weights
- No additional rollouts or external step-level supervision required; operates on a single completed trajectory
- Evaluated on service-agent benchmarks (τ²-Bench, UserBench, AgentChangeBench) with Qwen3-4B/8B

## Relevance

IAPO adds a fourth approach to the vault's credit-assignment taxonomy: SPA-RL (trained progress estimator), MileGPO (PCC criterion), DataPRM (environment-aware generative verifier), and now IAPO (influence-dependency graph). Like the "Credit Without Ground Truth" (Aug 21) critique of SPA-RL, IAPO avoids training a value function — but rather than counterfactual comparison, it uses the causal structure already present in the completed rollout. The empirical comparison (IAPO vs. SPA-RL progress estimator vs. MileGPO PCC on shared benchmarks) remains an open gap.

## My Thoughts

<!-- Add your own notes here -->
