---
title: "Reinforcement Learning with Robust Rubric Rewards"
authors: ["Ya-Qi Yu", "Hao Wang", "Fangyu Hong", "Xiangyang Qu", "Gaojie Wu", "Qiaoyu Luo", "Nuo Xu", "Huixin Wang", "Wuheng Xu", "Yongxin Liao", "Zihao Chen", "Haonan Li", "Ziming Li", "Dezhi Peng", "Minghui Liao", "Jihao Wu", "Haoyu Ren", "Dandan Tu"]
date: 2026-05-28
arxiv_id: "2605.30244"
url: "http://arxiv.org/abs/2605.30244v1"
score: 0.80
topics: [VLM, multimodal, reward model, RLHF, GRPO]
status: unread
---

# Reinforcement Learning with Robust Rubric Rewards

## Summary

RLR³ extends RLVR from task-level to criterion-level verification by routing instance-specific rubrics through LLM-extractor+deterministic-verifier or LLM-as-Judge pipelines, with a minimal exposure strategy (masking ground truths from extractors, images from judges) and hierarchical aggregation to prevent score saturation. On Qwen3-VL-30B-A3B across 15 benchmarks, RLR³ yields a 4.7-point improvement over the base model, exceeding the official instruct-to-thinking model gap.

## Key Contributions

- Criterion-level verification extending RLVR to partially-verifiable vision-language tasks
- Dual execution path routing: LLM-extractor + deterministic verifier OR LLM-as-Judge
- Minimal exposure strategy to prevent exploitable false positives in rubric scoring
- Hierarchical aggregation prioritizing essential criteria; 4.7-point gain across 15 benchmarks

## Relevance

Addresses partial-verifiability in multimodal RL — a key limitation when applying RLVR to vision-language tasks where not all criteria can be automatically checked; complements rubric-based reward threads.

## My Thoughts

<!-- Add your own notes here -->
