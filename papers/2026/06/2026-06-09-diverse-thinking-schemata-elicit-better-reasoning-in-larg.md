---
title: "Diverse Thinking Schemata Elicit Better Reasoning in Large Language Models"
authors: ["Xinyue Liang", "Yizhe Yang", "Yu Bai", "Bin Xu", "Jiawei Li", "Yang Gao"]
date: 2026-06-09
arxiv_id: "2606.08974"
url: "https://arxiv.org/abs/2606.08974"
score: 0.74
topics: [reinforcement learning, RL training, GRPO, agentic RL]
status: unread
---

# Diverse Thinking Schemata Elicit Better Reasoning in Large Language Models

## Summary

Reasoning transitions between steps and variety in solution paths are formalized as "thinking schemata" whose diversity correlates with LLM reasoning performance. DiScO (Diverse Schemata Policy Optimization) trains with GRPO to reward diversity across both transition types and answer candidates, and further promotes diverse reasoning at inference time, consistently outperforming standard GRPO on math benchmarks while substantially improving recovery from erroneous initial attempts. This work suggests that scaling along the diversity dimension is a complementary axis to scaling compute or model size.

## Key Contributions

- "Thinking schemata" formalization: reasoning transitions + answer candidate diversity as joint optimization targets
- DiScO: three-stage framework (schemata awareness → GRPO diversity training → inference-time diversity promotion)
- Consistently outperforms standard GRPO across multiple math reasoning benchmarks
- Substantially better recovery from erroneous initial reasoning paths

## Relevance

Extends the GRPO training thread with a novel angle: rather than better reward signals or training stability (EP-GRPO, M-GRPO, KL3), DiScO targets the diversity of the reasoning process itself. Connects to the SUPERNOVA data curation thread — both address generalisation, but from opposite ends (training data composition vs. policy diversity during RL). The "diversity dimension" as a scaling axis is a fresh framing worth tracking.

## My Thoughts

<!-- Add your own notes here -->
