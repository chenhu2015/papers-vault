---
title: "Action-Value Calibration via Continuation Sharing for Long-Horizon Agentic Reinforcement Learning"
authors: ["Yingjian Chen", "Lang Zhou", "Zixin Zhao", "Pingfan Li", "Weishi Zheng", "Zhilin Zhao"]
date: 2026-11-02
arxiv_id: "2610.37195v1"
url: "http://arxiv.org/abs/2610.37195v1"
score: 0.85
topics: [agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# Action-Value Calibration via Continuation Sharing for Long-Horizon Agentic Reinforcement Learning

## Summary

ConCal addresses credit distortion in long-horizon agentic RL by recursively aggregating continuation evidence already present in the rollout batch: it matches trajectory visits by incoming state-action-state transitions, combines shared continuation evidence with each visit's own estimate, and propagates calibrated action-values backward. This reduces sensitivity to individual sampled continuations without requiring additional rollouts. ConCal improves over GiGPPO by +3.39 and +5.86 percentage points on ALFWorld and WebShop respectively using Qwen2.5-1.5B-Instruct.

## Key Contributions

- Recursive continuation-value estimator (ConCal) that reuses continuation evidence already in the rollout batch via state-action-state transition matching
- Backward propagation of calibrated values reduces dependence on individual sampled continuations without additional rollouts
- Held-out return diagnostics show lower error in within-group value differences and higher agreement with reference action orderings versus single-continuation baselines
- +3.39pp (ALFWorld) and +5.86pp (WebShop) over GiGPPO baseline

## Relevance

This paper directly extends the long-horizon agentic RL thread, addressing the same credit distortion problem that GiGPPO (from Oct 31 pool) tackled via neighbor-state rewards — ConCal attacks it through continuation aggregation rather than critic construction. The approach is orthogonal to CORD's gradient conflict management and complementary to SCOPE's step-level distillation found in today's search.

## My Thoughts

<!-- Add your own notes here -->
