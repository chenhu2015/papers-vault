---
title: "ARES: Automated Rubric Synthesis for Scalable LLM Reinforcement Learning"
authors: ["Xiaoyuan Li", "Keqin Bao", "Moxin Li", "Yubo Ma", "Yichang Zhang", "Wenjie Wang", "Fuli Feng", "Dayiheng Liu"]
date: 2026-06-19
arxiv_id: "2605.23454v2"
url: "http://arxiv.org/abs/2605.23454v2"
score: 0.80
topics: [RLHF, reward model, RL training, RLAIF, LLM agent]
status: unread
---

# ARES: Automated Rubric Synthesis for Scalable LLM Reinforcement Learning

## Summary

Rubric-based rewards extend RL beyond verifiable-answer tasks, but expert-written rubrics and manual question construction do not scale. ARES automatically synthesizes rubric-based RL training data from raw pretraining documents — converting source knowledge into self-contained question-answer pairs co-generated with question-specific weighted rubrics for instance-level open-ended reward supervision. At 100K instances across 10 domains, rubric-based RL with ARES outperforms continual pretraining, SFT, and binary-reward RL, with the largest gains on multi-dimensional open-ended tasks such as healthcare and instruction following.

## Key Contributions

- Converts raw pretraining documents into self-contained question-answer pairs with co-generated question-specific weighted rubrics (rather than task-level fixed rubrics)
- Domain labels and persona conditioning improve diversity and quality; validation filters check question self-containment, answer faithfulness, and rubric validity
- 100K rubric-annotated instances across 10 domains generated automatically without human annotation
- Rubric-based RL with ARES beats CPT, SFT, and binary-reward RL across 7 benchmarks; largest gains on open-ended multi-dimensional tasks

## Relevance

Complements ARBOR (today) at the data pipeline level: ARBOR generates rubrics online from contrastive trajectories during training; ARES generates rubrics offline from pretraining documents before training. Together they address the two bottlenecks of rubric-based RL — the need for expert-written rubrics (ARES) and the zero-gradient problem in homogeneous groups during GRPO training (ARBOR). Also connects to the RLAIF keyword from the interest profile: ARES's auto-generated rubrics are a form of AI-generated supervision signal, avoiding both human annotation (RLHF) and binary verifier judgment (RLVR).

## My Thoughts

<!-- Add your own notes here -->
