---
title: "EVA: Efficient Reinforcement Learning for End-to-End Video Agent"
authors: ["Yaolun Zhang", "Ruohui Wang", "Jiahao Wang", "Yepeng Tang", "Xuanyu Zheng", "Haonan Duan", "Hao Lu", "Hanming Deng", "Lewei Lu"]
date: 2026-03-24
arxiv_id: "2603.22918v2"
url: "https://arxiv.org/abs/2603.22918v2"
score: 0.83
topics: [agentic RL, GRPO, VLM, multimodal, RL training]
status: unread
---

# EVA: Efficient Reinforcement Learning for End-to-End Video Agent

## Summary

EVA presents an end-to-end video agent that inverts the standard perception-first paradigm with planning-before-perception: the agent autonomously decides what to watch, when, and how, driven by the query via iterative summary-plan-action-reflection reasoning. Training uses a three-stage pipeline of SFT, Kahneman-Tversky Optimization (KTO), and GRPO, bridging supervised imitation and RL with high-quality stage-specific datasets. On six video understanding benchmarks EVA achieves 6–12% improvement over general MLLM baselines and 1–3% over prior adaptive agent methods.

## Key Contributions

- Planning-before-perception paradigm: query-driven agent decides what/when/how to watch, avoiding redundant full-video processing
- Three-stage training pipeline: SFT (imitation) → KTO (preference alignment) → GRPO (RL); each stage with dedicated high-quality data
- Iterative summary-plan-action-reflection reasoning loop for long-form video understanding
- Consistent 6–12% improvement over passive-recogniser MLLM baselines across six benchmarks

## Relevance

EVA is the video analog of the multi-turn agentic RL framework established by StePPO, ProceedRL, and Odysseus — but applied to query-driven video understanding instead of decision games or tool use. The SFT→KTO→GRPO training pipeline mirrors the staged approach of earlier LLM RL work and demonstrates that planning-before-perception is a viable architectural choice for long-form video agents.

## My Thoughts

<!-- Add your own notes here -->
