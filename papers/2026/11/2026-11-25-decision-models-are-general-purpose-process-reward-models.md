---
title: "Decision Models Are General-Purpose Process Reward Models"
authors: ["Jiajun Fan", "Qinglong Zheng", "Ziwen Wang", "Bangji Yang", "Neil He", "Ruihan Guo", "Chaoran Cheng", "Ge Liu"]
date: 2026-11-20
arxiv_id: "2611.27068v1"
url: "http://arxiv.org/abs/2611.27068v1"
score: 0.82
topics: [agentic RL, reward model, GRPO, LLM agent, tool use]
status: unread
---

# Decision Models Are General-Purpose Process Reward Models

## Summary

DM-PRM converts a frozen decision model into a zero-shot process reward model by asking one yes/no question per step ("Is executing this action the right decision?") and adding standardized answers to the GRPO advantage—no step labels, no fine-tuning, one model per environment. Applied to Qwen2.5-1.5B with GRPO, it lifts performance by 20+ points on ALFWorld and 10+ on WebShop, outperforming critic-based PPO and state-of-the-art GiGPO/HGPO/GraphGPO. The result shows that step credit in agentic RL can be derived by querying rather than learning.

## Key Contributions

- Zero-shot process reward from a frozen decision model: no step labels, no fine-tuning, no critic training
- One question per step (binary yes/no: "right decision?"), standardized answer pooled into the GRPO advantage
- Plugs into any policy-gradient method; a single model with one question text per environment generalizes across household tasks, web shopping, multiple RL methods
- 20+ point lift on ALFWorld, 10+ on WebShop vs. GRPO baseline; outperforms critic-based PPO and GiGPO/HGPO/GraphGPO

## Relevance

This paper directly answers the open question from the tool-use RL cluster (Nov 24): can process reward for individual tool calls/steps be obtained without training a step-level critic? DM-PRM says yes — query a frozen decision model. The approach is orthogonal to TACA/AOVO/StateAlign (which focus on outcome credit assignment failure modes) and suggests that step-level process reward need not be learned from step labels.

## My Thoughts

<!-- Add your own notes here -->
