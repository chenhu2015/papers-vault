---
title: "Think or Not? Selective Reasoning via Reinforcement Learning for Vision-Language Models"
authors: ["Jiaqi Wang", "Kevin Qinghong Lin", "James Cheng", "Mike Zheng Shou"]
date: 2025-05-22
arxiv_id: "2505.16854"
url: "https://arxiv.org/abs/2505.16854"
score: 0.84
topics: [agentic RL, reinforcement learning, GRPO, VLM, multimodal models]
status: unread
---

# Think or Not? Selective Reasoning via Reinforcement Learning for Vision-Language Models

## Summary

TON enables VLMs to selectively decide when to reason using a two-stage strategy: SFT with "thought dropout" (randomly replacing reasoning traces with empty thoughts) for cold start, followed by GRPO that lets the model freely explore think-or-not decisions. It reduces completion length by up to 90% vs vanilla GRPO while maintaining or improving task performance, and demonstrates models progressively learn to skip unnecessary reasoning steps across LLM, VLM, and agentic tasks.

## Key Contributions

- "Thought dropout" SFT cold start: randomly replace reasoning traces with empty thoughts to prime the model for the think-or-not format before RL
- Two-stage training (SFT → GRPO) where GRPO rewards are purely task-outcome based, not length-penalized
- Up to 90% reduction in completion length vs vanilla GRPO without sacrificing accuracy on GSM8K, CLEVR, GeoQA, and AITZ (agentic)
- Progressive learning dynamics: models increasingly skip reasoning for easy questions as GRPO training advances

## Relevance

Directly extends the ThinkWise/DR-BOLT adaptive reasoning thread opened on Nov 20: where ThinkWise uses perception-conditioned length regulation and DR-BOLT uses dual-reference offline optimization, TON uses thought-dropout cold start + unconstrained GRPO exploration to achieve selective reasoning. TON is simpler and broader (covers agentic AITZ tasks, not just VQA), making it a strong complement.

## My Thoughts

<!-- Add your own notes here -->
