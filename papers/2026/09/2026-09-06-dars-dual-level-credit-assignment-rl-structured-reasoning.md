---
title: "DARS: Dual-Level Credit Assignment RL with Structured Reasoning for Instruction-Based Image Editing"
authors: ["Haoxiang Cao", "Jiajiong Cao", "Xuanpu Zhang"]
date: 2026-09-06
arxiv_id: "2608.20161"
url: "https://arxiv.org/abs/2608.20161"
score: 0.82
topics: [VLM, multimodal models, vision-language, GRPO, reward model, RL training, agentic RL]
status: unread
---

# DARS: Dual-Level Credit Assignment RL with Structured Reasoning for Instruction-Based Image Editing

## Summary

DARS introduces dual-level credit assignment for a VLM planner + diffusion renderer pipeline: at the module level, multi-plan multi-render rollouts estimate between-plan and within-plan reward variability for soft module routing and adaptive curriculum; at the planner level, four-field structured reasoning output enables prefix-gated reward and token-level advantage reweighting. The structured reasoning axis mirrors StructReward's dense process design, while token-level advantage reweighting mirrors OTB, making DARS the first paper to empirically combine both principles in a multimodal RL pipeline. Outperforms Joint RL with identical backbone/data/reward/rollout budget across five benchmarks.

## Key Contributions

- Module-level credit assignment: between-plan and within-plan reward variability estimation via multi-plan multi-render rollouts for soft module routing
- Adaptive curriculum derived from rollout mean rewards as hardness estimates — connecting to SCALECUA's Frontier Sampling (Sep 05)
- Planner-level structured reasoning: four-field output enabling prefix-gated reward (StructReward-style) and token-level advantage reweighting (OTB-style)
- First paper to empirically combine StructReward dense process reward + OTB token-level advantage reweighting in a multimodal RL pipeline

## Relevance

DARS partially closes the "StructReward + OTB combination" open gap by implementing both principles simultaneously in the image editing domain, confirming their composability. The cross-module credit assignment axis (planner vs. renderer routing) is novel — prior agentic RL work (GAP, HARTS, SINKFLEX-RL) addresses tool-use efficiency but not cross-module credit attribution in a heterogeneous pipeline (LLM planner + diffusion renderer). The prefix-gated reward mechanism is a new variant of dense process reward that operates on structured reasoning field boundaries rather than step boundaries.

## My Thoughts

<!-- Add your own notes here -->
