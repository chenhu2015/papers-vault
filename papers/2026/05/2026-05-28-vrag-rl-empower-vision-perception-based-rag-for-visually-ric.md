---
title: "VRAG-RL: Empower Vision-Perception-Based RAG for Visually Rich Information Understanding via Iterative Reasoning with Reinforcement Learning"
authors: ["Qiuchen Wang", "Ruixue Ding", "Yu Zeng", "Zehui Chen", "Lin Chen", "Shihang Wang", "Pengjun Xie", "Fei Huang", "Feng Zhao"]
date: 2025-05-28
arxiv_id: "2505.22019v2"
url: "https://arxiv.org/abs/2505.22019"
score: 0.81
topics: [multimodal, VLM, vision-language, agentic RL, tool use, LLM agent]
status: unread
---

# VRAG-RL: Empower Vision-Perception-Based RAG for Visually Rich Information Understanding via Iterative Reasoning with Reinforcement Learning

## Summary

VRAG-RL applies RL to VLMs for visually rich document understanding, defining an action space tailored for visual inputs (cropping, scaling, query rewriting) and a reward combining retrieval quality with a model-based evaluator. VLMs interact with a search engine over multi-turn trajectories using visual perception tokens, with RL jointly optimising retrieval strategy and visual reasoning. The framework addresses two root causes of failure in multimodal RAG: insufficient reasoning token allocation for vision and inability to formulate effective retrieval queries.

## Key Contributions

- Visual action space for VLM-RAG: crop/scale perception actions plus query rewriting trained end-to-end with RL
- Visual perception tokens enable coarse-to-fine information gathering during retrieval-reasoning interleaving
- Hybrid reward combining retrieval performance with model-based quality evaluation
- Addresses insufficient visual reasoning allocation and poor query articulation as distinct failure modes

## Relevance

Bridges the VLM alignment thread and the agentic RL + tool-use thread in the interest profile; while the paper is from May 2025, VRAG-RL's visual action space design is a natural extension of the "tool use" keyword and prefigures more recent work on visual reasoning agents (LAT, Patho-AgenticRAG found in same search).

## My Thoughts

<!-- Add your own notes here -->
