---
title: "VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents"
authors: ["Kangrui Wang", "Pingyue Zhang", "Zihan Wang", "Yaning Gao", "Linjie Li", "Qineng Wang", "Hanyang Chen", "Chi Wan", "Yiping Lu", "Zhengyuan Yang", "Lijuan Wang", "Ranjay Krishna", "Jiajun Wu", "Li Fei-Fei", "Yejin Choi", "Manling Li"]
date: 2025-10-19
arxiv_id: "2510.16907v1"
url: "http://arxiv.org/abs/2510.16907v1"
score: 0.85
topics: [agentic RL, RL training, vision language models, multimodal models]
status: unread
---

# VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents

## Summary

VAGEN formulates multi-turn VLM agent training as a POMDP and demonstrates that decomposing the agent's reasoning into State Estimation ("what is the current state?") and Transition Modeling ("what comes next?") is critical for visual agent performance. A World Modeling Reward provides dense turn-level supervision for accurate state prediction, while Bi-Level GAE computes turn-aware credit assignment across the multi-step trajectory. A 3B model trained in the VAGEN framework achieves 0.82 average score across five diverse agent benchmarks, outperforming GPT-5 (0.75), Gemini 2.5 Pro (0.67), and Claude 4.5 (0.62).

## Key Contributions

- POMDP formulation of multi-turn VLM agent training with partial observability over visual observations
- Decomposed reasoning strategy: State Estimation + Transition Modeling as two explicit reasoning targets
- World Modeling Reward: dense, turn-level supervision signal for state prediction accuracy
- Bi-Level GAE: turn-aware credit assignment that propagates advantages at both turn and token granularity

## Relevance

Directly addresses multi-turn agentic RL for VLMs, combining two core profile keywords (agentic RL, VLM). The Bi-Level GAE is closely related to the credit assignment problems studied in StePPO, ProceedRL, and AEM from previous digests—extending that thread specifically to partially observable visual environments.

## My Thoughts

<!-- Add your own notes here -->
