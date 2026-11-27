---
title: "SGR-OPSD: Learning from Subgoal Plans with Graph-Regularized Credit Assignment for Agentic Reinforcement Learning"
authors: ["Shu Liu", "Yang Chong", "WenShi Chen", "Man Lan"]
date: 2026-11-02
arxiv_id: "2611.02414v2"
url: "https://arxiv.org/abs/2611.02414"
score: 0.8
topics: [agentic RL, GRPO, LLM agent, RL training]
status: unread
---

# SGR-OPSD: Learning from Subgoal Plans with Graph-Regularized Credit Assignment for Agentic Reinforcement Learning

## Summary

SGR-OPSD extends the OPSD privileged-supervision framework with two additions: LLM-generated subgoal plans converted to per-action advantage weights via a KL-regularized objective, and a Subgoal Progress Graph that estimates empirical action returns from sampled transition frequencies to calibrate teacher credit against observed environment outcomes. Evaluated on ALFWorld, WebShop, and Search-QA with Qwen2.5-3B and 7B, improving success rates over GRPO by up to 7.6 points and reaching 85.8% on ALFWorld at 7B scale.

## Key Contributions

- Subgoal plan generation by LLM converted to advantage weights via constrained KL-regularized objective
- Subgoal Progress Graph: empirical return estimates from transition frequencies calibrate teacher credit
- Addresses OPSD limitation that teacher-student log-probability gaps reflect model preference shift, not task progress
- Consistent gains over GRPO on three diverse agentic benchmarks (navigation, shopping, search)

## Relevance

Extends the agentic credit assignment thread with a privileged-information / curriculum signal approach — using subgoal plans as a form of hindsight credit that doesn't require a separate reward model. The graph-calibration component (grounding credit in observed environmental transitions) connects to the long-horizon RL thread: empirical returns from sampled paths are more reliable than teacher-estimated advantage over long episodes.

## My Thoughts

<!-- Add your own notes here -->
