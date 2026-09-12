---
title: "Learning Where Outcomes Change: Credit-Addressable Reasoning for Multimodal Geometry"
authors: ["Jiani Guo", "Junjie Wang", "Jie Wu", "Pengxiang Zhao", "Dongdong Zhang", "Shaohan Huang", "Yujiu Yang", "Furu Wei"]
date: 2026-08-31
arxiv_id: "2608.30457v1"
url: "http://arxiv.org/abs/2608.30457v1"
score: 0.87
topics: [VLM, vision-language, multimodal, GRPO, agentic RL]
status: unread
---

# Learning Where Outcomes Change: Credit-Addressable Reasoning for Multimodal Geometry

## Summary

CE-GRPO introduces the credit-addressable reasoning principle: semantic inference units exposed during inference also define where RL compares alternatives and assigns credit. Concretely, Code-CoT represents visual relations as line-addressable executable code organized into typed events; CE-GRPO selects event boundaries via structural priors and type-normalized entropy, samples continuations from shared prefixes, and converts outcome differences into localized advantages. Across nine geometry benchmarks, CE-GRPO achieves 76.04% average accuracy, outperforming Qwen3-VL-8B by 8.09pp and trajectory-level GRPO by 3.43pp, with relative advantage increasing with the number of intermediate events.

## Key Contributions

- Credit-addressable reasoning principle: representation and optimization share semantic unit boundaries — credit goes where inference decisions are made
- Code-CoT: visual relations represented as line-addressable executable code with typed event structure (diagram → relation → reasoning → conclusion)
- CE-GRPO: event-boundary credit assignment using structural priors + type-normalized entropy for boundary selection; shared-prefix sampling; localized advantages from outcome differences
- Representation-optimization co-design: relative advantage over trajectory-level GRPO increases with intermediate event count, validating the principle

## Relevance

CE-GRPO is the VLM-specific realization of the credit-addressable reasoning approach, connecting the VLM + GRPO training thread (SVRL, Sep 10) with the structured credit assignment thread (CRISP, TASPO, Sep 11). Distinctively, it makes representation itself the credit assignment unit rather than annotating an existing free-form trace — closer to PLVR's typed program primitives (Sep 11) than to CRISP's backward evidence labeling, but applied to visual geometry rather than code execution.

## My Thoughts

<!-- Add your own notes here -->
