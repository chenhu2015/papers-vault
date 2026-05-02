---
title: "Explore with Long-term Memory: A Benchmark and Multimodal LLM-based Reinforcement Learning Framework for Embodied Exploration"
authors: ["Sen Wang", "Bangwei Liu", "Zhenkun Gao", "Lizhuang Ma", "Xuhong Wang", "Yuan Xie", "Xin Tan"]
date: 2026-01-11
arxiv_id: "2601.10744v2"
url: "http://arxiv.org/abs/2601.10744v2"
score: 0.79
topics: [multimodal models, vision language models, agentic RL, RL training]
status: unread
---

# Explore with Long-term Memory: A Benchmark and Multimodal LLM-based Reinforcement Learning Framework for Embodied Exploration

## Summary

MemoryExplorer fine-tunes a multimodal LLM via RL with a multi-task reward covering action prediction, frontier selection, and VQA to encourage proactive memory querying in long-horizon embodied settings. LMEE-Bench unifies multi-goal navigation and memory-based QA for comprehensive evaluation of embodied exploration. Demonstrates significant advantages over state-of-the-art embodied exploration models.

## Key Contributions

- MemoryExplorer: multimodal LLM fine-tuned via RL specifically to encourage active memory querying during exploration
- Multi-task reward combining action prediction, frontier selection, and question answering
- LMEE-Bench: new benchmark unifying multi-goal navigation + memory-based QA for lifelong learning evaluation
- Demonstrates proactive exploration with long-term episodic memory across long-horizon tasks

## Relevance

Bridges the VLM + agentic RL interest threads in a direction not covered yesterday (GUI agents). Uses RL to teach a multimodal model when and how to use long-term memory in embodied settings — a natural neighbour to the GUI agent RL survey from yesterday but with an embodied/navigation angle and an explicit memory component.

## My Thoughts

<!-- Add your own notes here -->
