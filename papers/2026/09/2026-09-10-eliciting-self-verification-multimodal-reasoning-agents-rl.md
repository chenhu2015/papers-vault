---
title: "Eliciting Self-Verification in Multimodal Reasoning Agents with Reinforcement Learning"
authors: ["Vishwas Sathish", "Viresh Ranjan", "Xinliang Zhu", "Arnab Dhua", "Douglas Gray"]
date: 2026-09-10
arxiv_id: "2609.08025v1"
url: "https://arxiv.org/abs/2609.08025v1"
score: 0.83
topics: [VLM, vision-language, multimodal, GRPO, agentic RL, tool use, LLM agent]
status: unread
---

# Eliciting Self-Verification in Multimodal Reasoning Agents with Reinforcement Learning

## Summary

SVRL is an RL-only finetuning framework (GRPO-based) that trains multimodal agents (Qwen-2.5-VL-7B) to self-verify and filter retrieved web evidence within their own reasoning traces, removing reliance on external verifiers. It introduces a search-aware penalty discouraging unnecessary tool calls and a query-diversity reward encouraging varied, well-formed search queries. Training on only 5,000 visual QA examples yields consistent gains in multi-hop VQA generalization and tool efficiency, narrowing the gap to much larger proprietary models.

## Key Contributions

- **SVRL**: RL-only (no SFT cold-start) training for multimodal web-search agents via GRPO
- **Search-aware penalty**: discourages redundant or unnecessary tool calls at inference time, improving tool efficiency
- **Query-diversity reward**: encourages diverse, well-formed search queries to improve evidence quality
- **Data efficiency**: 5,000 VQA training examples sufficient; competitive with much larger proprietary models on multi-hop benchmarks

## Relevance

Squarely addresses the SFT-free VLM RL open gap: SVRL demonstrates GRPO-only (no SFT cold-start) training of a multimodal agent with tool use, using a multi-component reward (outcome correctness + search penalty + diversity). The search-aware penalty is a novel addition to the reward engineering thread for agentic RL, complementing the execution-based rewards in ExecCritic and ERPO with a tool-efficiency dimension.

## My Thoughts

<!-- Add your own notes here -->
