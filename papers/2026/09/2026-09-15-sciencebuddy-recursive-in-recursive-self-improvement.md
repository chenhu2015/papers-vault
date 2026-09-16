---
title: "ScienceBuddy: Recursive-in-Recursive Self-Improvement for Interactive Scientific Agents"
authors: ["Shuhan Xue", "Jianyuan Zhong", "Ziyuan Nan", "Wenbin Li", "Zhaochen Yu", "Jinchao Ding", "Qiang Gao", "Pengyu Zhan", "Yuntong Zhang", "Tian Cheng", "Zhenfei Yin", "Yingcheng Wu", "Ling Yang"]
date: 2026-09-15
arxiv_id: "2609.17523v1"
url: "http://arxiv.org/abs/2609.17523v1"
score: 0.85
topics: [agentic RL, LLM agent, RL training]
status: unread
---

# ScienceBuddy: Recursive-in-Recursive Self-Improvement for Interactive Scientific Agents

## Summary

ScienceBuddy introduces recursive-in-recursive self-improvement: an inner recursion improves the harness with the model fixed, while the outer recursion trains the model under the improved harness, coupling harness evolution with model RL. Researcher feedback and execution evidence are transformed into tasks and evaluation rubrics for continual learning, enabling sustained harness-model co-adaptation. This directly addresses the model-harness joint optimization problem (cf. Harness-RL, ECDYSIS), providing a concrete outer-loop training protocol for interactive scientific AI.

## Key Contributions

- Recursive-in-recursive paradigm: inner loop = harness improvement (model fixed), outer loop = model RL (under improved harness)
- Researcher interaction and execution evidence converted to tasks + evaluation rubrics for continual learning
- Demonstrates on 4 scientific task families with interactive case studies of harness refinement and model learning
- Joint harness-model co-adaptation as a deployable research product (science-buddy.io)

## Relevance

The open gap from Sep 12 was model-harness joint optimization (Harness-RL partial narrowing). ScienceBuddy provides the most complete treatment yet: not just joint optimization but a concrete alternating protocol — fix model, improve harness; fix harness, train model — making the two-loop structure explicit and testable. The outer-loop architecture is structurally analogous to ECDYSIS's runtime harness adaptation but adds the model RL component that ECDYSIS leaves out.

## My Thoughts

<!-- Add your own notes here -->
