---
title: "What You Think is What You See: Driving Exploration in VLM Agents via Visual-Linguistic Curiosity"
authors: ["Haoxi Li", "Qinglin Hou", "Jianfei Ma", "Jinxiang Lai", "Tao Han", "Sikai Bai", "Jingcai Guo", "Jie Zhang", "Song Guo"]
date: 2026-05-05
arxiv_id: "2605.03782"
url: "http://arxiv.org/abs/2605.03782v1"
score: 0.80
topics: [agentic RL, LLM agent, VLM, multimodal models, reinforcement learning]
status: unread
---

# What You Think is What You See: Driving Exploration in VLM Agents via Visual-Linguistic Curiosity

## Summary

GLANCE enables curiosity-driven RL exploration in VLM agents by grounding the model's linguistic world model predictions into stable visual representations from an evolving target network, using the linguistic-visual prediction discrepancy as an intrinsic curiosity reward. This signal steers agents to actively explore regions where their internal world model is uncertain, enabling effective exploration in sparse-reward partially-observable environments where passive CoT reasoning fails.

## Key Contributions

- Visual-linguistic curiosity: discrepancy between linguistic prediction and visual reality as intrinsic reward
- Evolving target network for stable visual representations that ground the linguistic world model
- Unified framework bridging CoT-based world modeling with curiosity-driven RL exploration
- Demonstrated on agentic tasks in partially-observable environments with sparse rewards

## Relevance

This directly extends the agentic RL exploration thread from prior digests (deep dense exploration, AEM) to the multimodal domain, adding an intrinsic curiosity mechanism grounded in vision-language consistency. The focus on sparse-reward partially-observable environments is relevant to long-horizon agents.

## My Thoughts

<!-- Add your own notes here -->
