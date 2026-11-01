---
title: "SophiaVL-R1: Reinforcing MLLMs Reasoning with Thinking Reward"
authors: ["Kaixuan Fan", "Kaituo Feng", "Haoming Lyu", "Dongzhan Zhou", "Xiangyu Yue"]
date: 2026-11-01
arxiv_id: "2505.17018v2"
url: "https://arxiv.org/abs/2505.17018"
score: 0.85
topics: [multimodal models, vision language models, VLM, GRPO, reward model, RLAIF]
status: unread
---

# SophiaVL-R1: Reinforcing MLLMs Reasoning with Thinking Reward

## Summary

Adds a thinking-process reward on top of standard outcome-reward GRPO for multimodal LLMs, addressing the lack of supervision over intermediate reasoning steps. Trust-GRPO assigns a trustworthiness weight to the thinking reward based on the relative reward comparison between correct and incorrect rollouts, mitigating reward hacking; an annealing schedule then gradually reduces the thinking reward weight so the model converges on reliable rule-based outcome signals. SophiaVL-R1-7B outperforms LLaVA-OneVision-72B on most benchmarks despite 10× fewer parameters.

## Key Contributions

- Thinking reward model trained to evaluate quality of the full chain-of-thought, not just the final answer
- Trust-GRPO: per-sample trustworthiness weight computed from thinking reward comparison between correct vs. incorrect rollouts — down-weights samples where the reward model may be hacking
- Annealing strategy: thinking reward contribution decreases over training so the model relies more on verifiable outcome rewards in later stages, avoiding compounding reward model errors
- SophiaVL-R1-7B matches or exceeds models 10× larger on MathVista and MMMU benchmarks

## Relevance

Directly advances the VLM RL reward design thread that previous searches probed via step-credit vocabulary (MRPO) and failure-cascade framing (CoFire). SophiaVL-R1 attacks the same problem — providing process-level supervision in VLM RL — but from the angle of a learned thinking reward model rather than rule-based step penalties; Trust-GRPO's weighting mechanism is a novel answer to the reward hacking problem that CoFire and Beacon also identified from different angles.

## My Thoughts

<!-- Add your own notes here -->
