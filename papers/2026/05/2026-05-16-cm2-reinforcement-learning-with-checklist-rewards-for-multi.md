---
title: "CM2: Reinforcement Learning with Checklist Rewards for Multi-Turn and Multi-Step Agentic Tool Use"
authors: ["Zhen Zhang", "Kaiqiang Song", "Xun Wang", "Yebowen Hu", "Weixiang Yan", "Chenyang Zhao", "Henry Peng Zou", "Haoyun Deng", "Sathish Reddy Indurthi", "Shujian Liu", "Simin Ma", "Xiaoyang Wang", "Xin Eric Wang", "Song Wang"]
date: 2026-05-16
arxiv_id: "2602.12268v2"
url: "http://arxiv.org/abs/2602.12268v2"
score: 0.85
topics: [tool use, agentic RL, LLM agent, reward model, GRPO, RL training]
status: unread
---

# CM2: Reinforcement Learning with Checklist Rewards for Multi-Turn and Multi-Step Agentic Tool Use

## Summary

CM2 replaces verifiable outcome rewards with checklist rewards that decompose each turn's intended behavior into fine-grained binary criteria with explicit evidence grounding, turning open-ended judging into stable classification-style decisions. Using sparse reward assignment but dense evaluation criteria within an LLM-simulated tool environment, CM2 improves over SFT by +8pp on tau-Bench, +10pp on BFCL-V4, and +12pp on ToolSandbox from an 8B model trained on 8k examples.

## Key Contributions

- Checklist reward design: each turn's behavior decomposed into fine-grained binary criteria with structured metadata and evidence grounding
- Strategy of sparse reward assignment + dense evaluation criteria to balance stability and informativeness
- LLM-simulated tool environment avoids heavy engineering for large tool sets, enabling scale
- +8pp tau-Bench, +10pp BFCL-V4, +12pp ToolSandbox from 8B Base with 8k RL examples; matches or beats similarly-sized open-source baselines

## Relevance

Directly addresses tool use and agentic RL (core interest profile keywords) in the realistic multi-turn, multi-step setting where verifiable rewards are unavailable. The checklist approach is a concrete alternative to the "rubric decomposition" idea in May 14's RubricEM (which used rubrics for meta-RL in deep research); CM2 applies the same decomposition principle but at the per-turn reward level rather than the meta-policy level.

## My Thoughts

<!-- Add your own notes here -->
