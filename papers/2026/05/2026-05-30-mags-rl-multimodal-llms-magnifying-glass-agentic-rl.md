---
title: "Mags-RL: Wearing Multimodal LLMs a Magnifying Glass via Agentic Reinforcement Learning For Complex Scene Reasoning"
authors: ["Xuanzhao Dong", "Wenhui Zhu", "Peijie Qiu", "Xiwen Chen", "Xiaobing Yu", "Xin Li", "Zhipeng Wang", "Shao Tang", "Gen Li", "Yujian Xiong", "Hao Wang", "Yanxi Chen", "Prayag Tiwari", "Yalin Wang"]
date: 2026-05-27
arxiv_id: "2605.27960"
url: "http://arxiv.org/abs/2605.27960v1"
score: 0.88
topics: [agentic RL, VLM, tool use, multimodal, GRPO]
status: unread
---

# Mags-RL: Wearing Multimodal LLMs a Magnifying Glass via Agentic Reinforcement Learning For Complex Scene Reasoning

## Summary

Mags-RL equips MLLMs with an external super-resolution tool-use agent: the model autonomously identifies regions of interest in a first reasoning round, then invokes a magnifying-glass agent to crop and upscale them for fine-grained inspection before producing a final answer. Trained with agentic GRPO via curriculum learning using as few as 40 samples, it outperforms recent strong methods on VSR, TallyQA, and GQA subsets requiring high-resolution visual grounding.

## Key Contributions

- Two-round agentic reasoning: initial rationale + ROI identification → super-resolution crop invocation → revised final answer
- External super-resolution tool-use integration into MLLM agentic RL loop without extra annotations
- Curriculum RL training strategy enabling data-efficient GRPO with only 40 training samples
- Superior performance against strong competing methods on dense-scene visual QA benchmarks

## Relevance

Directly advances the multimodal agentic tool-use RL thread that has been a 2-day carry-forward (May 28–29) due to arxiv rate-limiting; a clean example of the VLM + agentic RL + tool-use pattern that the interest profile prioritizes.

## My Thoughts

<!-- Add your own notes here -->
