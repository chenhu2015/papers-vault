---
title: "Dependency-Aware Reward Shaping for Agentic Reinforcement Learning"
authors: ["Ziyi Chen", "Yan Zhang", "Jianhui Wei", "Daoan Zhang", "Zuozhu Liu"]
date: 2026-10-01
arxiv_id: "2610.01207v1"
url: "http://arxiv.org/abs/2610.01207v1"
score: 0.84
topics: [agentic RL, RL training, reward model, LLM agent, tool use]
status: unread
---

# Dependency-Aware Reward Shaping for Agentic Reinforcement Learning

## Summary

DARS assigns step-level credit by representing task progress as predicates linked by prerequisite dependencies, discounting credit for steps that build on uncorrected mistakes while leaving independent steps unaffected. A distilled 8B annotator marks predicate verification, invalidation, and repair at inference time, enabling DARS to run without a frontier API judge. Integrated with GiGPO and ARPO/AEPO, DARS improves success by up to 10 points on ALFWorld and raises WebShop and QA accuracy.

## Key Contributions

- Predicate-DAG representation of task progress: each step either verifies, invalidates, or repairs predicates; credit discounted by graph distance from the nearest broken prerequisite
- Fixed potential converts predicate annotations into signed per-step rewards compatible with any RL optimizer (GiGPO, ARPO/AEPO tested)
- Distilled 8B annotator matches frontier API annotator on ALFWorld, removing the API cost
- Ablations confirm step-level credit, dependency attenuation, and graph topology each independently contribute

## Relevance

DARS is the most structurally explicit step-credit paper in this cluster: while SIPO corrects selection bias in branch value estimates and T2SPO uses regression from past trajectories, DARS builds an explicit causal graph of task dependencies. The distilled annotator design directly answers the "no-annotation" challenge raised by TGPO's automatic PRM: instead of learning a reward model, DARS distills an annotator — a distinct design point. The "work built on uncorrected mistakes is wasted" insight is a crisp formalization of why flat trajectory-level advantage credit fails on long-horizon tasks.

## My Thoughts

<!-- Add your own notes here -->
