---
title: "Are Tools Always Beneficial? Learning to Invoke Tools Adaptively for Dual-Mode Multimodal LLM Reasoning"
authors: ["Qinghe Ma", "Zhen Zhao", "Yiming Wu", "Jian Zhang", "Lei Bai", "Yinghuan Shi"]
date: 2026-07-07
arxiv_id: "2605.19852v2"
url: "http://arxiv.org/abs/2605.19852v2"
score: 0.80
topics: [agentic RL, tool use, multimodal, vision-language, VLM, LLM agent]
status: unread
---

# Are Tools Always Beneficial? Learning to Invoke Tools Adaptively for Dual-Mode Multimodal LLM Reasoning

## Summary

AutoTool identifies over-invocation of tools as an under-studied failure mode in MLLM reasoning: redundant or mismatched tool calls increase overhead and mislead predictions. It introduces a dual-mode RL framework — tool-assisted vs. text-centric — with mode-specific reward functions, jointly exploring both modes throughout training and promoting free exploration in later stages to prevent premature mode bias. On V* benchmark, AutoTool achieves a 21.8% accuracy gain over the base model and a 44.9% efficiency improvement over existing tool-augmented methods on POPE benchmark.

## Key Contributions

- Identifies over-invocation as a complementary failure mode to under-invocation in MLLM tool use
- Dual-mode reasoning strategy with explicit mode-specific RL reward functions guiding adaptive decisions
- Joint multi-mode exploration during training followed by free exploration in later stages to prevent early mode collapse
- 21.8% accuracy gain on V* + 44.9% efficiency improvement over tool-augmented methods on POPE

## Relevance

Directly extends the agentic RL + tool use thread from the interest profile, addressing the question of *when* not to use tools — a constraint that existing agentic RL work (including ReLook, Search 4 today) implicitly ignores by assuming tool use is always additive. The dual-mode RL design is structurally related to the RL-PLUS hybrid-policy from Jul 6 (on-policy vs. off-policy switching), generalizing that idea to tool/no-tool mode switching with domain-specific reward.

## My Thoughts

<!-- Add your own notes here -->
