---
title: "Efficient Agentic Reinforcement Learning with On-Policy Intrinsic Knowledge Boundary Enhancement"
authors: ["Dingwei Chen", "Zefang Zong", "Zhipeng Ma", "Leo Luo", "Yang Li", "Chengming Li", "Peng Chen", "Jie Jiang"]
date: 2026-05-26
arxiv_id: "2605.26952"
url: "http://arxiv.org/abs/2605.26952v1"
score: 0.87
topics: [agentic RL, tool use, RL training, reward model, LLM agent]
status: unread
---

# Efficient Agentic Reinforcement Learning with On-Policy Intrinsic Knowledge Boundary Enhancement

## Summary

AKBE uses dual-path rollouts (with-tool vs. no-tool) during on-policy agentic RL to dynamically probe the model's intrinsic knowledge boundary and categorize trajectories, constructing fine-grained supervisory signals that guide efficient tool use rather than blanket suppression. On seven QA benchmarks, AKBE improves accuracy by +1.85 on average while reducing tool calls by 18%, yielding 25% higher tool productivity with no accuracy-efficiency trade-off.

## Key Contributions

- Dual-path rollout framework (with-tool / no-tool) to define per-instance knowledge boundary
- Trajectory categorization producing targeted supervisory signals beyond coarse reward shaping
- 18% tool call reduction + +1.85 average accuracy gain across 7 QA benchmarks
- Plug-and-play compatibility across different RL algorithms

## Relevance

Addresses the tool-use efficiency problem in agentic RL — a core theme in the interest profile — from a novel intrinsic knowledge boundary angle distinct from reward-shaping approaches seen in earlier digests.

## My Thoughts

<!-- Add your own notes here -->
