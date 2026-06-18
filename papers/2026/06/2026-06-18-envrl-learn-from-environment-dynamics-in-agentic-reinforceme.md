---
title: "EnvRL: Learn from Environment Dynamics in Agentic Reinforcement Learning"
authors: ["Zhitong Wang", "Songze Li", "Hao Peng", "Shuzheng Si", "Yi Wang", "Maosong Sun", "Juanzi Li"]
date: 2026-06-18
arxiv_id: "2606.17680"
url: "https://arxiv.org/abs/2606.17680"
score: 0.79
topics: [agentic RL, GRPO, LLM agent, RL training]
status: unread
---

# EnvRL: Learn from Environment Dynamics in Agentic Reinforcement Learning

## Summary

Long-horizon agentic RL suffers from sparse outcome rewards while ignoring a dense implicit supervision signal already present in interaction trajectories: environment dynamics. EnvRL adds two auxiliary objectives — state prediction and inverse dynamics — jointly optimized with the primary GRPO objective, encouraging the agent to internalize a model of environment transition mechanisms from its own rollouts. With Qwen-2.5-1.5B-Instruct and GRPO, this lifts ALFWorld success from 72.8% to 77.4% and WebShop from 56.8% to 67.0%.

## Key Contributions

- Frames rollout interaction trajectories as implicit supervision for environment dynamics, requiring no additional data collection
- Two auxiliary objectives: state prediction (forward model: predict next state from current state + action) and inverse dynamics (backward model: predict action from state transition)
- Joint optimization with primary GRPO reward — the dynamics learning regularizes the policy toward actions consistent with the environment's actual transition structure
- Validated on ALFWorld and WebShop long-horizon agentic benchmarks with measurable improvement over GRPO-only baseline

## Relevance

Complements the sparse reward solutions in the vault from a world-model angle: where InfoMem (Jun 10) addressed sparse rewards via answer-conditioned memory rewards and ENCORE (Jun 15) via self-play curriculum, EnvRL addresses it via auxiliary environment modeling — the agent learns transition dynamics as a side effect of acting, which then constrains the policy toward valid action sequences.

## My Thoughts

<!-- Add your own notes here -->
