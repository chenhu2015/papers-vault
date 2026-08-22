---
title: "Correlation or Causation: Analyzing the Causal Structures of LLM and LRM Reasoning Process"
authors: ["Zhizhang FU", "Guangsheng Bao", "Hongbo Zhang", "Chenkai Hu", "Yue Zhang"]
date: 2026-08-22
arxiv_id: "2509.17380v1"
url: "https://arxiv.org/abs/2509.17380"
score: 0.73
topics: [RLHF, RLAIF, reinforcement learning, reward model, LLM agent]
status: unread
---

# Correlation or Causation: Analyzing the Causal Structures of LLM and LRM Reasoning Process

## Summary

A systematic structural-causal-model analysis of LLMs vs. LRMs shows that RLVR-trained LRMs develop reasoning processes that align with ideal causal structures — reducing spurious correlations between problem, thinking, and answer — while distilled LRMs fail to fix the same causality deficits present in base LLMs. The causal improvements in RLVR training are correlated with reduced spurious features throughout the training process. This provides a causal-mechanistic explanation for why RLVR improves faithfulness and reduces bias beyond what distillation achieves.

## Key Contributions

- **SCM analysis framework**: four-variable structural causal model (problem instruction, thinking process, reasoning steps, answer) applied across LLMs and LRMs to assess causal alignment
- **RLVR vs. distillation finding**: RLVR-trained LRMs align with ideal causal structures; distilled LRMs share the same causality deficits as base LLMs — the training objective determines causal structure, not performance on benchmarks alone
- **Spurious correlation reduction**: RLVR training consistently reduces spurious correlations and strengthens genuine causal pathways; improvement tracks with reduced spurious features during training
- **Practical implication**: faithfulness and bias reduction in reasoning models are consequences of causal structure, not surface performance metrics

## Relevance

This paper provides the theoretical underpinning for the Aug 19 "illusory distillation" finding (OPD is sampling efficiency, not capability expansion) at the causal-mechanistic level: why does RLVR create better models than distillation even when distillation matches RLVR's average performance? Because RLVR builds genuine causal reasoning structure while distillation does not. This connects the OPD thread with the causal credit assignment thread (opened by "Credit Without Ground Truth" Aug 21) — and suggests that the causal quality of the reasoning process, not just its accuracy, should be an evaluation criterion for agentic RL training methods.

## My Thoughts

<!-- Add your own notes here -->
