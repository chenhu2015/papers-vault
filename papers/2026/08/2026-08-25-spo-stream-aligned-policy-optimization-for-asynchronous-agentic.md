---
title: "SPO++: Stream-Aligned Policy Optimization for Asynchronous Agentic RL"
authors: ["Kai Ruan", "Jinghao Lin", "Qianshan Wei", "Ziqi Zhou", "Zihe Huang"]
date: 2026-08-25
arxiv_id: "2608.24870v1"
url: "http://arxiv.org/abs/2608.24870v1"
score: 0.82
topics: [agentic RL, GRPO, RL training, tool use, PPO]
status: unread
---

# SPO++: Stream-Aligned Policy Optimization for Asynchronous Agentic RL

## Summary

SPO++ identifies that Single-stream Policy Optimization (which removes GRPO's sibling rollout dependency for long tool-use trajectories) applies trajectory centering that does not actually center the token-weighted quantity consumed by the actor, and fixes this by standardizing terminal-outcome advantages under the action-token measure. It additionally organizes prompt evidence by the policy event that generated it rather than learner receipt order, improving causal alignment between experience and gradient. On ALFWorld at two model scales and Math-TIR, SPO++ improves online learning efficiency over SPO, with action-token-measure normalization identified as the strongest component via paired ablation.

## Key Contributions

- Formal diagnosis: trajectory centering ≠ centering of the token-weighted actor loss in SPO
- Fix: standardize terminal-outcome advantages under the action-token measure rather than trajectory mean
- Prompt evidence organized by policy-event generation order rather than learner receipt order
- Evaluated on ALFWorld (two scales) and Math-TIR; ablations isolate action-token normalization as key contributor

## Relevance

SPO++ is a precision engineering paper that sits at the GRPO → SPO lineage: GRPO (group-relative, requires sibling rollouts) → SPO (removes sibling dependency, adds persistent value estimate) → SPO++ (fixes SPO's normalization bug). The missing-old-logits problem (2605.12070v2, also in this digest) identifies a parallel correctness issue in async PPO pipelines; together these two papers constitute a systematic audit of the correctness assumptions in asynchronous agentic RL training at the algorithm level.

## My Thoughts

<!-- Add your own notes here -->
