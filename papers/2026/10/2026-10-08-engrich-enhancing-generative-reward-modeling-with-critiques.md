---
title: "EnGRICH: Enhancing Generative Reward Modeling with Critiques from Humans"
authors: ["Xuancheng Li", "Beining Wang", "Haitao Li", "Heng Wang"]
date: 2026-10-08
arxiv_id: "2610.05370v2"
url: "http://arxiv.org/abs/2610.05370v2"
score: 0.73
topics: [reward model, RLHF, RLAIF]
status: unread
---

# EnGRICH: Enhancing Generative Reward Modeling with Critiques from Humans

## Summary

EnGRICH improves generative reward model (GRM) training by pairing the GRM with a MetaCritic trained on a small set of human critiques; the MetaCritic constructs response-specific rubrics and evaluates evidence coverage and correctness of the GRM's generated critiques, providing process rewards for fine-grained credit assignment. The MetaCritic is jointly optimized to generalize human-grounded evaluative criteria to outcome-only data, so the GRM at inference requires no external critic. The approach consistently outperforms competitive baselines across seven reward-model benchmarks.

## Key Contributions

- MetaCritic: auxiliary model trained on a small set of human critiques to provide process rewards for GRM training
- Response-specific rubric construction to evaluate evidence coverage and correctness of generated critiques
- Joint MetaCritic optimization to generalize human criteria to outcome-only data at scale
- Consistent improvement across seven reward-model benchmarks without inference-time critic overhead

## Relevance

Complements BoT-GRPO and RewardWeaver: where those papers ask how to use process rewards in RL training, EnGRICH asks how to make the process rewards themselves more reliable by grounding them in human critique criteria. The MetaCritic's rubric construction is a lightweight form of the "validated capability space" in RewardWeaver, applied to reward modeling rather than agent training.

## My Thoughts

<!-- Add your own notes here -->
