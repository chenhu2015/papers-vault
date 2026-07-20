---
title: "Stop Rewarding Hallucinated Steps: Faithfulness-Aware Step-Level Reinforcement Learning for Small Reasoning Models"
authors: ["Shuo Nie", "Hexuan Deng", "Chao Wang", "Ruiyu Fang", "Xuebo Liu", "Shuangyong Song", "Yu Li", "Min Zhang", "Xuelong Li"]
date: 2026-02-05
arxiv_id: "2602.05897"
url: "http://arxiv.org/abs/2602.05897v2"
score: 0.82
topics: [RLHF, reward model, RL training, reinforcement learning]
status: unread
---

# Stop Rewarding Hallucinated Steps: Faithfulness-Aware Step-Level Reinforcement Learning for Small Reasoning Models

## Summary

FaithRL addresses faithfulness hallucinations in intermediate reasoning steps of small reasoning models (SRMs), where outcome-based RL rewards can reinforce unfaithful CoT when the final answer happens to be correct. It introduces step-level supervision via explicit faithfulness rewards from a process reward model, combined with an implicit truncated resampling strategy that generates contrastive signals from faithful prefixes to mitigate reward hacking from step-level rewards. Experiments on multiple SRMs and Open-Book QA benchmarks show consistently reduced hallucinations in both CoT and final answers.

## Key Contributions

- Identifies that outcome-based RL rewards reinforce unfaithful intermediate reasoning steps when the final answer is correct — a text-only small-model analogue of CORA's thinking-answer inconsistency in VLMs
- Explicit faithfulness rewards from a PRM at the step level, providing fine-grained signal beyond trajectory-level outcomes
- Truncated resampling strategy: generates contrastive signals from faithful prefixes to mitigate reward hacking that step-level rewards can introduce
- Consistent hallucination reduction in both intermediate CoT steps and final answers across multiple SRM architectures and Open-Book QA benchmarks

## Relevance

FaithRL closes the text-only counterpart gap identified from CORA (Jul 19): CORA showed that thinking-answer semantic inconsistency persists throughout multimodal GRPO training; FaithRL shows the same failure mode exists in text-only SRMs and provides a step-level PRM-based fix. Together they establish that reasoning trace faithfulness is a general RL training failure mode across modalities and model sizes, not a VLM-specific artifact.

## My Thoughts

<!-- Add your own notes here -->
