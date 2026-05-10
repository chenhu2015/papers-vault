---
title: "Teaching Thinking Models to Reason with Tools: A Full-Pipeline Recipe for Tool-Integrated Reasoning"
authors: ["Qianjia Cheng", "Yuchen Zhang", "Zhilin Wang", "Yuxin Zuo", "Shunkai Zhang", "Yuchen Fan", "Yu Qiao", "Bowen Zhou", "Ning Ding", "Yu Cheng", "Yun Luo", "Ganqu Cui"]
date: 2026-05-07
arxiv_id: "2605.06326"
url: "http://arxiv.org/abs/2605.06326v1"
score: 0.83
topics: [agentic RL, RL training, tool use, GRPO, LLM agent]
status: unread
---

# Teaching Thinking Models to Reason with Tools: A Full-Pipeline Recipe for Tool-Integrated Reasoning

## Summary

A systematic TIR recipe for injecting tool-use into strong thinking models without sacrificing no-tool reasoning: SFT learnability depends on selecting inherently tool-suited problems; tool-use trajectory proportion controls catastrophic forgetting; RLVR with mode-collapse safeguards then provides robust improvement. Applied to Qwen3 thinking models, the recipe achieves 96.7% (4B) and 99.2% (30B) on AIME 2025, SOTA among open-source models.

## Key Contributions

- Observation: tool-enabled evaluation degrades reasoning even when thinking models make almost no tool calls — paradox requiring a careful recipe
- SFT stage: learnability of teacher trajectories (problems inherently suited to tool use) matters more than volume; proportion control prevents forgetting
- RLVR stage: stable training with verifiable rewards + mode-collapse safeguards; optimizing pass@k and response length over training loss
- 96.7% (4B) and 99.2% (30B) on AIME 2025 — SOTA open-source performance for tool-integrated thinking models

## Relevance

Directly extends the tool-use RL thread from May 5 (VISTA-R1) with a full SFT+RLVR recipe rather than just the environment. The insight about catastrophic forgetting via trajectory proportion is practically important and connects to data curation findings (OpenSearch-VL from May 7). Mode-collapse safeguards in RLVR align with reward over-optimization concerns seen throughout the digest series.

## My Thoughts

<!-- Add your own notes here -->
