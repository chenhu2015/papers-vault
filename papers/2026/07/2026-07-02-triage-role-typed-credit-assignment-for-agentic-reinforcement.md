---
title: "TRIAGE: Role-Typed Credit Assignment for Agentic Reinforcement Learning"
authors: ["Yuanda Xu", "Zhengze Zhou", "Hejian Sang", "Xiaomin Li", "Jiaxin Zhang", "Xinchen Du", "Zhipeng Wang", "Alborz Geramifard"]
date: 2026-07-02
arxiv_id: "2606.32017v1"
url: "https://arxiv.org/abs/2606.32017"
score: 0.92
topics: [agentic RL, credit assignment, GRPO, tool use, LLM agent]
status: unread
---

# TRIAGE: Role-Typed Credit Assignment for Agentic Reinforcement Learning

## Summary

TRIAGE adds a semantic role axis to GRPO-based agentic RL by having a structured judge classify each action segment as decisive progress, useful exploration, no-progress infrastructure, or regression, then applying fixed role-conditioned bounded process rewards. This corrects GRPO's two main outcome-credit blind spots: punishing useful exploration in failed rollouts and reinforcing regression in successful ones. Evaluated on ALFWorld, Search-QA, and WebShop, TRIAGE improves success rates and reduces environment-facing turns by 10.4–14.8% relative to GRPO.

## Key Contributions

- Four-category semantic role taxonomy (decisive progress, useful exploration, no-progress infrastructure, regression) for agentic action segments
- Fixed role-conditioned rule mapping from role labels to bounded segment-level process rewards — no learned reward model required
- Theoretical result: role-conditioned credit is the optimal segment-level correction expressible from role labels alone (projection of per-segment advantage residual onto role variable)
- Ablations isolate regression detection in successful trajectories as dominant contributor; exploration credit provides consistent secondary gain

## Relevance

TRIAGE is the natural agentic extension of the credit assignment hierarchy that FlowTracer (Jul 1, attention DAG) and SCPO (Jun 30, sibling-step credit) built on standard math/reasoning tasks. By naming regression-in-success and exploration-in-failure as the two structural blind spots of outcome-only GRPO, TRIAGE provides the missing tool-use axis to the five-axis credit hierarchy: rollout state graph (GraphGPO), attention DAG (FlowTracer), sibling-step (SCPO), trajectory-segment (DRE), and now role-typed action segment (TRIAGE). This was the exact thread queued from the Jul 1 digest: FlowTracer on math benchmarks; same approach extended to multi-step agentic tasks.

## My Thoughts

<!-- Add your own notes here -->
