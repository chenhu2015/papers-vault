---
title: "Signal Reshaping for GRPO in Weak-Feedback Agentic Code Repair"
authors: ["Jia Li", "Yuxin Su", "Ting Peng", "Hailiang Huang", "Yuetang Deng", "Michael R. Lyu"]
date: 2026-05-08
arxiv_id: "2605.07276v1"
url: "http://arxiv.org/abs/2605.07276v1"
score: 0.82
topics: [agentic RL, GRPO, tool use, LLM agent, reward model]
status: unread
---

# Signal Reshaping for GRPO in Weak-Feedback Agentic Code Repair

## Summary

This paper diagnoses why GRPO fails under weak feedback in agentic code repair: rollout signals capture necessary but not sufficient conditions, making within-group comparison meaningless without signal reshaping. It proposes three orthogonal reshaping operations — layered outcome rewards to recover semantic ranking, step-level process scores for intra-trajectory credit, and failure-cause-aware rollout governance for within-group comparability — improving strict compile-and-semantic accuracy from 0.385 to 0.535. The analysis also shows that token-level distillation cannot substitute for outcome semantics or process credit in long tool-use trajectories.

## Key Contributions

- Formal diagnosis of GRPO failure under weak feedback: identifies three conditions (outcome ranking, within-trajectory credit, within-group comparability) that must all be reshaped for GRPO's group-normalized advantage to be meaningful
- Layered reward design (compile + semantic) that recovers semantic trajectory ranking lost when only compile-pass is observable
- Step-level process scoring outside group normalization for within-trajectory credit assignment without distorting the group advantage
- Failure-cause-aware rollout governance ensures within-group comparability; ablations confirm all three conditions are independently necessary

## Relevance

Connects to the multi-turn agentic RL thread (May 16) with a rigorous theoretical framing for why standard GRPO breaks in tool-use settings. The three-condition framework generalizes beyond code repair to any weak-feedback agentic environment — directly relevant to CM2, AEM, and other multi-turn GRPO papers.

## My Thoughts

<!-- Add your own notes here -->
