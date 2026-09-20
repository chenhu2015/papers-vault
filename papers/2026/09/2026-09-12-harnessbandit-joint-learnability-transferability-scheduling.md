---
title: "HarnessBandit: Joint Learnability-Transferability Scheduling for Multi-Harness Agentic Reinforcement Learning"
authors: ["Hongliang Wei", "Xiaobing Tu", "Yinggui Wang", "Zhengxi Liu", "Rongkun Xue", "Jinkui Ren", "Xiantao Zhang", "Debin Zhao", "Xiaopeng Fan"]
date: 2026-09-12
arxiv_id: "2609.13739v1"
url: "http://arxiv.org/abs/2609.13739v1"
score: 0.83
topics: [agentic RL, GRPO, LLM agent, tool use]
status: unread
---

# HarnessBandit: Joint Learnability-Transferability Scheduling for Multi-Harness Agentic Reinforcement Learning

## Summary

HarnessBandit frames multi-harness training as an online scheduling problem: a shared policy trains across diverse harnesses (differing in system prompts, tool schemas, control loops, and trajectory formats) by selecting the harness with the best learning signal per optimizer step. The scheduler fuses learnability (mean absolute advantage on the batch) and transferability (gradient cosine between harnesses) after sliding-window normalization with a visit-dependent exploration bonus. Training Qwen3.5-2B across six harnesses shows improvement over mixed-batch multi-harness training on both in-distribution and held-out harness benchmarks.

## Key Contributions

- Formalizes multi-harness agentic RL as an online scheduling problem rather than a data-mixing problem
- Learnability signal: mean absolute GRPO advantage on the current batch (measures useful learning gradient)
- Transferability signal: cosine between a low-dimensional gradient sketch of the current harness and EMAs of other harnesses (measures cross-harness generalization)
- Visit-dependent exploration bonus with explicit exploration floor prevents harness starvation

## Relevance

Extends the Polar/HarnessForge cluster (Sep 18/19 digests) by addressing harness diversity as a *scheduling* problem rather than an *adaptation* problem. Polar focuses on black-box API proxying for a single harness; HarnessForge jointly evolves harness and policy; HarnessBandit asks how to allocate optimizer steps across harnesses when all are available simultaneously. Found via black-box harness RL convergence search (Sep 20).

## My Thoughts

<!-- Add your own notes here -->
