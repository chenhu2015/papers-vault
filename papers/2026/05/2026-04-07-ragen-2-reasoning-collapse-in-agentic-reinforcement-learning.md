---
title: "RAGEN-2: Reasoning Collapse in Agentic Reinforcement Learning"
authors: []
date: 2026-04-07
arxiv_id: "2604.06268"
url: "https://arxiv.org/abs/2604.06268"
score: 0.90
topics: [agentic-RL, RL-training, reward-model, GRPO, LLM-agent]
status: unread
---

# RAGEN-2: Reasoning Collapse in Agentic Reinforcement Learning

## Summary

Identifies "template collapse" — a failure mode where models produce superficially diverse but input-agnostic reasoning during RL training, making entropy a misleading training quality metric. Introduces a mutual information proxy and SNR-Aware Filtering to select high-signal prompts per training iteration, preventing collapse.

## Key Contributions

- Diagnosis of template collapse as a systematic failure mode in agentic RL
- Shows entropy is insufficient as a training quality metric
- Mutual information proxy for detecting input-agnostic reasoning
- SNR-Aware Filtering to select informative training prompts per iteration

## Relevance

Critical diagnostic paper for anyone training agentic LLMs via GRPO or similar RL methods. Directly relevant to GRPO, RL training, and understanding failure modes in agentic RL.

## My Thoughts

<!-- Add your own notes here -->
