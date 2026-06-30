---
title: "Semantic Consistency Policy Optimization for Reinforcement Learning of LLM Agents"
authors: ["Peng Xu", "Sijia Chen", "Junzhuo Li", "Xuming Hu"]
date: 2026-06-30
arxiv_id: "2606.25852"
url: "http://arxiv.org/abs/2606.25852v1"
score: 0.84
topics: [agentic RL, GRPO, RL training, LLM agent]
status: unread
---

# Semantic Consistency Policy Optimization for Reinforcement Learning of LLM Agents

## Summary

Group-based RL ties each step's credit to the trajectory's final outcome, causing semantically near-identical intermediate steps to receive opposite gradients depending on whether their trajectory succeeded or failed — a problem SCPO calls semantic credit inconsistency. SCPO introduces value-free reward shaping that recovers step-level credit from successful sibling trajectories within the same rollout group, adding positive credit for progress unique to a failed step that also appeared in a successful sibling. On ALFWorld (93.7% success) and WebShop (74.8%) at 1.5B parameters, SCPO matches or exceeds strong group-based RL baselines with the largest gains on the hardest multi-step tasks.

## Key Contributions

- Identifies semantic credit inconsistency as a structural failure mode of group-based RL: same-meaning steps get opposite gradients depending on trajectory outcome
- Reward shaping that recovers step-level credit from successful siblings in the same rollout group without a value network
- Gains concentrated on hardest multi-step agentic tasks (ALFWorld 93.7%, WebShop 74.8% at 1.5B)
- Value-free drop-in complement to GRPO requiring no architectural changes

## Relevance

SCPO is the within-trajectory complement to DRE (Jun 19) and STRIDE (Jun 20): DRE removes unnecessary post-answer continuation, STRIDE assigns discriminative n-gram credit within groups, and SCPO assigns cross-trajectory sibling credit to rescue failed-trajectory steps — together defining a complete picture of sub-trajectory credit recovery for group-based RL. The "semantic inconsistency" framing also explains why ARBOR's zero-gradient problem (Jun 19) is harmful even beyond the missing gradient: when outcome-homogeneous groups do produce a gradient signal, the signal is semantically inconsistent across the semantically similar steps that differ only in downstream luck.

## My Thoughts

<!-- Add your own notes here -->
