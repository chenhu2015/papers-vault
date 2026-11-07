---
title: "SGR-OPSD: Learning from Subgoal Plans with Graph-Regularized Credit Assignment for Agentic Reinforcement Learning"
authors: ["Shu Liu", "Yang Chong", "WenShi Chen", "Man Lan"]
date: 2026-11-02
arxiv_id: "2611.02414v1"
url: "https://arxiv.org/abs/2611.02414"
score: 0.83
topics: [agentic RL, GRPO, reinforcement learning, LLM agent, agentic, tool use]
status: unread
---

# SGR-OPSD: Learning from Subgoal Plans with Graph-Regularized Credit Assignment for Agentic Reinforcement Learning

## Summary

SGR-OPSD augments OPSD with two components: LLM-generated subgoal plans that convert privileged-information teacher signals into action-level advantage weights via a KL-regularized objective, and a Subgoal Progress Graph that estimates empirical action returns from sampled transition frequencies to calibrate those weights. The graph compares empirical returns against per-state averages, grounding credit in observed outcomes rather than model preference shifts. Evaluated on ALFWorld, WebShop, and Search-QA at Qwen2.5-3B and 7B scales, SGR-OPSD improves GRPO success rates by up to 7.4pp, reaching 85.8% on ALFWorld with Qwen2.5-7B.

## Key Contributions

- Subgoal supervision: LLM-generated subgoal plans converted to per-action advantage weights via constrained KL-regularized objective — denser than outcome-only GRPO
- Subgoal Progress Graph: empirical return estimation from sampled transition frequencies, grounding credit calibration in actual outcomes rather than model preference
- Addresses OPSD's key flaw: teacher–student log-probability gaps reflect model preference shifts rather than true task progress
- +7.4pp over GRPO on ALFWorld; 85.8% with Qwen2.5-7B across ALFWorld/WebShop/Search-QA

## Relevance

SGR-OPSD adds a subgoal-plan + graph-regularized axis to the step-credit cluster (prior work: ProAS uses ARG, GCA decomposes search/answer, EG-GRPO uses evidence annotations). The key novelty is explicitly grounding privilege-information teacher signals in empirical state-transition data via a graph, rather than raw model logprob ratios — a principled fix for OPSD's known flaw.

## My Thoughts

<!-- Add your own notes here -->
