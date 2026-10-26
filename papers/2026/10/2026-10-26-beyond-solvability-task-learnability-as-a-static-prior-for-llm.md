---
title: "Beyond Solvability: Task Learnability as a Static Prior for LLM RL Post-Training"
authors: ["Ting Zhou", "Zhenqing Ling", "Daoyuan Chen", "Qianli Shen", "Yilun Huang", "Ying Shen", "Yaliang Li"]
date: 2026-08-10
arxiv_id: "2608.09217v1"
url: "http://arxiv.org/abs/2608.09217v1"
score: 0.83
topics: [GRPO, RL training, reinforcement learning, reward model]
status: unread
---

# Beyond Solvability: Task Learnability as a Static Prior for LLM RL Post-Training

## Summary

This paper distinguishes task solvability (current pass rate) from task learnability (regime-conditional expected positive response to further training), showing that tasks with similar solvability can differ substantially in learnability. TrajVal approximates per-task learnability from a short probe run and two endpoint evaluations, providing a lightweight static prior usable before or during training. Experiments across math and logical reasoning benchmarks show TrajVal improves data efficiency over uniform sampling and provides complementary gains when combined with online schedulers.

## Key Contributions

- Formal distinction between solvability and learnability; shows higher pre-RLVR accuracy does not guarantee higher post-RLVR accuracy
- Learnability shown to be reproducible across independently sampled training contexts
- TrajVal: lightweight probe-based estimator computing learnability from a short probe run + two endpoint evaluations
- Demonstrated complementarity with online scheduling methods (additive, not redundant)

## Relevance

Directly extends the RL rollout efficiency cluster with a distinct angle: VIGOR/LEEPS/HIVE select prompts based on current training state signals; TrajVal provides a static prior *before* training begins, with the key insight that solvability and learnability decouple — the same gap identified from the IsoCompute sharpening/coverage dichotomy but operationalized as a practical pre-training probe.

## My Thoughts

<!-- Add your own notes here -->
