---
title: "TRIAGE: Role-Typed Credit Assignment for Agentic Reinforcement Learning"
authors: ["Yuanda Xu", "Zhengze Zhou", "Hejian Sang", "Xiaomin Li", "Jiaxin Zhang", "Xinchen Du", "Sen Na", "Zhipeng Wang", "Alborz Geramifard"]
date: 2026-10-04
arxiv_id: "2606.32017"
url: "https://arxiv.org/abs/2606.32017"
score: 0.92
topics: [agentic RL, RL training, reward model, GRPO, LLM agent]
status: unread
---

# TRIAGE: Role-Typed Credit Assignment for Agentic Reinforcement Learning

## Summary

TRIAGE adds a semantic role axis to standard GRPO outcome credit by having a structured judge classify each trajectory segment as decisive progress, useful exploration, no-progress infrastructure, or regression, then mapping these labels to bounded role-conditioned process rewards. The key insight is that outcome-only credit has two structural blind spots: punishing useful exploration in failed rollouts and reinforcing regressive actions in successful ones; role typing corrects both simultaneously. TRIAGE improves success rates over GRPO on ALFWorld, Search-QA, and WebShop while reducing environment-facing turns by 10.4–14.8%.

## Key Contributions

- Four semantic role labels (decisive progress, useful exploration, no-progress infrastructure, regression) assigned by a structured judge to each trajectory segment
- Fixed role-conditioned rules map labels to bounded segment-level process rewards, keeping verifier outcomes as the optimization direction
- Bayes-optimal role-measurable correction is the L2 projection of per-segment advantage residual onto the role variable; TRIAGE's fixed role constants approximate this, reducing advantage estimation error
- Consistent success-rate gains over GRPO and outperforms both a scalar judge-derived process reward and an outcome-supervised shared-backbone value baseline across three agentic benchmarks

## Relevance

TRIAGE is the tenth entry in the step-credit cluster (joining ProVer, FAULT, SHARPO, SCA, ASCT, TEMPO, SIPO, DARS, T2SPO, TASPO), and the most taxonomically complete design: it explicitly names the four role categories that all prior work implicitly addresses in isolation. The regression-inside-successful-trajectory detection is the dominant gain (the same finding ProVer's outcome-rate verification targets from a different angle), while exploration credit provides a secondary consistent gain — confirming the dual-blind-spot framing across two independent papers.

## My Thoughts

<!-- Add your own notes here -->
