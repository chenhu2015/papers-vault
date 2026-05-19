---
title: "GrandCode: Achieving Grandmaster Level in Competitive Programming via Agentic Reinforcement Learning"
authors: ["DeepReinforce Team", "Xiaoya Li", "Xiaofei Sun", "Guoyin Wang", "Songqiao Su", "Chris Shum", "Jiwei Li"]
date: 2026-04-03
arxiv_id: "2604.02721v1"
url: "http://arxiv.org/abs/2604.02721v1"
score: 0.82
topics: [agentic RL, GRPO, LLM agent, RL training, tool use]
status: unread
---

# GrandCode: Achieving Grandmaster Level in Competitive Programming via Agentic Reinforcement Learning

## Summary

GrandCode is the first AI system to consistently beat all human participants in live Codeforces competitions, placing first in three consecutive rounds including against legendary grandmasters. It orchestrates modular agentic components (hypothesis, solver, test generator, summarizer) and introduces Agentic GRPO specifically designed for multi-stage rollouts with delayed rewards and severe off-policy drift prevalent in agentic settings. Both post-training and online test-time RL are applied jointly to all agent modules.

## Key Contributions

- Agentic GRPO: novel policy optimization algorithm that handles multi-stage rollouts with delayed rewards and the off-policy drift that accumulates over long agent trajectories
- Multi-agent architecture with specialized modular components trained jointly through post-training and online test-time RL
- First AI system to place first in live competitive programming contests against all human participants including top grandmasters
- Demonstrates that joint RL training of all agent modules (not just the policy) is necessary for the system-level performance gain

## Relevance

Landmark result for agentic RL — the first live grandmaster-beating system using GRPO. Agentic GRPO directly extends the GRPO/multi-turn agentic RL thread (CM2, ActFocus, Signal Reshaping) to long-horizon multi-stage agent pipelines, addressing off-policy drift at scale. Provides a concrete upper bound on what agentic GRPO can achieve.

## My Thoughts

<!-- Add your own notes here -->
