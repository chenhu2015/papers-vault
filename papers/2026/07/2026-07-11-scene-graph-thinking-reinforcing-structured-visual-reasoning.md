---
title: "Scene Graph Thinking: Reinforcing Structured Visual Reasoning for Multimodal Large Language Models"
authors: ["Zhiwei Yang", "Yuanchen Wu", "Nan Zhang", "Yucong Meng", "Ke Yan", "Shouhong Ding"]
date: 2026-07-11
arxiv_id: "2607.05716"
url: "https://arxiv.org/abs/2607.05716"
score: 0.80
topics: [multimodal models, VLM, vision-language, RLVR]
status: unread
---

# Scene Graph Thinking: Reinforcing Structured Visual Reasoning for Multimodal Large Language Models

## Summary

SaGe introduces scene-graph-based structured visual reasoning for multimodal LLMs, using an automated data engine to convert flat image-text corpora into hierarchical scene graphs where entities are nodes and visual relations define edges. Two-stage post-training applies SFT to internalize structured reasoning followed by reinforcement fine-tuning with node-as-proxy graph rewards that consolidate efficient graph exploration. Achieves significant improvements across eight multimodal benchmarks, particularly on fine-grained perception and spatial reasoning tasks.

## Key Contributions

- Automated scene-graph data engine: converts flat image-text corpora into structured hierarchical graphs (120K high-quality training samples) without manual annotation
- Node-as-proxy graph rewards for RL: uses identified graph nodes as verifiable proxies to reward correct visual reasoning paths, enabling RLVR in the structured visual domain
- Two-stage post-training: SFT for skill acquisition (structured scene graph reasoning), RL for skill consolidation (efficient graph exploration)
- Strong multi-benchmark generalization: improvements across 8 benchmarks including spatial reasoning and fine-grained perception tasks where unstructured VLMs struggle

## Relevance

SaGe is the scene-graph analog of SR-GRPO's internal-geometry reward (Jul 10): both use structured representations derived from model internals or graph structure as verifiable reward signals rather than scalar outcome rewards. SaGe specifically addresses the navigational failure mode in VLMs — focusing on isolated objects while ignoring relational structure — which is the visual counterpart of the exploratory primitive suppression failure mode identified in "When RL Suppresses Its Own Vocabulary" (Jul 10). Both papers use structured representations to restore a capability the model loses under naive RL.

## My Thoughts

<!-- Add your own notes here -->
