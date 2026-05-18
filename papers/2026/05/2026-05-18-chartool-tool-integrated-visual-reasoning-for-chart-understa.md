---
title: "CharTool: Tool-Integrated Visual Reasoning for Chart Understanding"
authors: ["Situo Zhang", "Yifan Zhang", "Zichen Zhu", "Da Ma", "Lei Pan", "Danyang Zhang", "Zihan Zhao", "Lu Chen", "Kai Yu"]
date: 2026-04-03
arxiv_id: "2604.02794v1"
url: "http://arxiv.org/abs/2604.02794v1"
score: 0.85
topics: [VLM, agentic RL, tool use, multimodal, vision-language]
status: unread
---

# CharTool: Tool-Integrated Visual Reasoning for Chart Understanding

## Summary

CharTool equips MLLMs with image-cropping and code-execution tools for chart reasoning, then trains them via agentic RL on DuoChart — a dual-source pipeline combining synthesized and real-world charts. The RL training loop grounds tool use in chart content rather than surface pattern matching, yielding +8.0% on CharXiv (Reasoning) and +9.78% on ChartQAPro, with positive generalization transfer to out-of-domain visual math reasoning benchmarks.

## Key Contributions

- DuoChart: dual-source data pipeline combining synthesized charts with real-world charts for high-quality, diverse training coverage
- Two tools: image cropping for localized visual perception; code-based computation for precise numerical reasoning over charts
- Agentic RL training teaches the model when and how to invoke tools, grounded in chart content
- CharTool-7B outperforms substantially larger and proprietary models and generalizes out-of-domain to visual math reasoning

## Relevance

Combines two core interest profile threads — VLM/multimodal and agentic RL with tool use — in a structured visual domain. A natural companion to the multi-turn tool-use RL papers from May 16 (AEM, CM2), now applied to chart understanding specifically. Agentic RL for visual tool use is a productive subthread first surfaced by VAGEN (May 5) and now substantially extended.

## My Thoughts

<!-- Add your own notes here -->
