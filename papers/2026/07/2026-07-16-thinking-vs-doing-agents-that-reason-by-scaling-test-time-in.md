---
title: "Thinking vs. Doing: Agents that Reason by Scaling Test-Time Interaction"
authors: ["Junhong Shen", "Hao Bai", "Lunjun Zhang", "Yifei Zhou", "Amrith Setlur", "Shengbang Tong", "Diego Caples", "Nan Jiang", "Tong Zhang", "Ameet Talwalkar", "Aviral Kumar"]
date: 2025-06-09
arxiv_id: "2506.07976"
url: "https://arxiv.org/abs/2506.07976"
score: 0.82
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# Thinking vs. Doing: Agents that Reason by Scaling Test-Time Interaction

## Summary

TTI proposes scaling test-time *interaction horizon* rather than per-step inference compute, allowing agents to run richer behaviors (exploration, backtracking, dynamic re-planning) within a single rollout. A curriculum-based online RL approach trains agents by adaptively adjusting rollout lengths from short to long, enabling the model to learn when to explore vs. exploit. A Gemma 3 12B model trained with TTI achieves state-of-the-art open-source results on WebVoyager and WebArena, establishing interaction scaling as a complementary axis to per-step compute scaling.

## Key Contributions

- Formalizes test-time interaction scaling as a distinct dimension from per-step compute scaling: more steps in the environment, not more tokens per step
- Curriculum RL training that progressively extends rollout horizons, analogous to how RSPO uses dense rewards for sampling diversity; here the "density" is temporal depth
- Prompting-based interaction scaling without training already improves task success non-trivially — suggesting a strong inductive prior for interaction-time exploration
- Establishes that TTI agents can balance exploration and exploitation adaptively, and can be steered by human-provided plans

## Relevance

The vault has covered test-time scaling primarily for math/reasoning (T1, Video-RTS, KV-PRM for beam search) and sequential self-correction (VRRL, SVR-R1). TTI fills the gap on the agentic tool-use side: interaction horizon is the natural unit of compute in web/tool-use agents, not inference tokens. The curriculum RL design is structurally similar to RSPO's insight about staged training signals, applied here to rollout length instead of reward density.

## My Thoughts

<!-- Add your own notes here -->
