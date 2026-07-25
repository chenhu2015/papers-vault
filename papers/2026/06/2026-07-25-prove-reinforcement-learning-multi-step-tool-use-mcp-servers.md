---
title: "Synthesize and Reward -- Reinforcement Learning for Multi-Step Tool Use in Live Environments"
authors: ["Ibrahim Abdelaziz", "Asim Munawar", "Kinjal Basu", "Maxwell Crouse", "Chulaka Gunasekara", "Suneet Katrekar", "Pavan Kapanipathi"]
date: 2026-06-02
arxiv_id: "2606.03892v2"
url: "http://arxiv.org/abs/2606.03892v2"
score: 0.80
topics: [agentic RL, RL training, tool use, LLM agent, GRPO]
status: unread
---

# Synthesize and Reward -- Reinforcement Learning for Multi-Step Tool Use in Live Environments

## Summary

PROVE provides 20 stateful MCP servers (343 tools) for live-execution GRPO training with session-scoped state isolation, a state-machine data synthesis pipeline that grounds multi-turn queries in live-sampled server state to prevent stale-reference execution failures, and an adaptive efficiency penalty that specifically counters the verbosity incentive created by recall-based rewards. Training Qwen3-4B, Qwen3-8B, Qwen2.5-7B, and Granite-4.1-8B with GRPO on ~13K trajectories yields improvements of +10.2, +6.8, and +6.5 on BFCL Multi-Turn, tau2-bench, and T-Eval respectively.

## Key Contributions

- 20 stateful MCP servers, 343 tools for live-execution RL; session-scoped state isolation enables parallel rollout without state contamination
- State-machine data synthesis: queries grounded in live-sampled server state → generated tool calls reference entities that actually exist, eliminating silent execution failures from stale data
- Adaptive efficiency penalty: counters recall-based reward's verbosity incentive by penalizing redundant tool calls proportional to current policy verbosity level
- Consistent gains across two model families (Qwen, Granite) on three multi-step tool-use benchmarks

## Relevance

PROVE completes the MCP-server RL training picture alongside ToolVerse (Jul 24). ToolVerse addressed environment scale (400 MCP servers, 4500 tools, dependency-graph task generation); PROVE addresses training trajectory quality (state-machine synthesis grounded in live state, verbosity penalty). Together they cover the two orthogonal challenges of agentic RL at scale: what does the agent train on (environment design, ToolVerse) and how does training data avoid silent failures (synthesis grounding, PROVE). The adaptive efficiency penalty is a reward-level solution to the verbosity failure mode — structurally different from APO's STCR (length penalty on negative VLM samples, Jul 24) but targeting the same underlying pathology: models learn to pad responses because partial recall credit incentivizes verbosity over precision.

## My Thoughts

<!-- Add your own notes here -->
