---
title: "BranPO: Scalable Contrastive Branch Sampling for Long-Horizon Agentic Reinforcement Learning"
authors: ["Yubao Zhao", "Weiquan Huang", "Sudong Wang", "Ruochen Zhao", "Chen Chen", "Yao Shu", "Chengwei Qin"]
date: 2026-02-03
arxiv_id: "2602.03719v2"
url: "http://arxiv.org/abs/2602.03719v2"
score: 0.86
topics: [agentic RL, RL training, LLM agent, agentic, GRPO]
status: unread
---

# BranPO: Scalable Contrastive Branch Sampling for Long-Horizon Agentic Reinforcement Learning

## Summary

BranPO addresses 'non-monotonic correctness' in long-horizon agentic RL — where early errors can be recovered while promising states can still fail — by constructing contrastive supervision through branching trajectories at intermediate prefixes and resampling continuations that share the same prefix but diverge in final outcomes. The value-free method avoids dense reward models, augmented with difficulty-aware sampling and Redundant Step Masking for efficiency. BranPO consistently outperforms diverse baselines across multi-hop QA benchmarks and generalizes to broader long-horizon tasks.

## Key Contributions

- Formal definition of 'non-monotonic correctness' as a fundamental challenge in long-horizon RL credit assignment
- Contrastive branch sampling: truncate at intermediate prefix, resample continuations to isolate per-decision quality
- Difficulty-aware branch sampling for efficient exploration
- Redundant Step Masking to suppress uninformative gradient updates

## Relevance

Long-horizon agentic RL credit assignment is underexplored in recent digests; directly extends the token-level credit assignment thread (GraphGPO/CovarGRPO, May 27) to the long-horizon multi-step setting where those token-level approaches break down.

## My Thoughts

<!-- Add your own notes here -->
