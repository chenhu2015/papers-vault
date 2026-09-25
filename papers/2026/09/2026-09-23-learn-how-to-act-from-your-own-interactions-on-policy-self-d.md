---
title: "Learn How to Act from Your Own Interactions: On-Policy Self-Distillation for GUI Agents"
authors: ["Yan Zhang", "Daiqing Wu", "Huawen Shen", "Liang Li", "Gang Cao", "Zhi Gong", "Wei Dai", "Xiaode Zhang", "Can Ma", "Yu Zhou"]
date: 2026-09-23
arxiv_id: "2609.27307v1"
url: "https://arxiv.org/abs/2609.27307"
score: 0.74
topics: [agentic RL, LLM agent, multimodal models]
status: unread
---

# Learn How to Act from Your Own Interactions: On-Policy Self-Distillation for GUI Agents

## Summary

GUI-SD-v2 extends on-policy self-distillation (OPSD) from GUI grounding to full multi-turn GUI interaction by addressing limited privilege-following ability and insufficient privileged guidance in prior OPSD methods. A two-stage training framework jointly optimizes rollouts with and without privileged guidance, then selectively distills step-specific reasoning and memory guidance through a privilege-conditioned self-teacher. Results on AndroidWorld and MobileWorld outperform prior OPSD baselines and state-of-the-art methods in both Pass@1 and Pass@3.

## Key Contributions

- Identifies two bottlenecks in applying OPSD to multi-turn GUI agents: (1) limited privilege-following ability of self-teachers; (2) insufficient privileged guidance for multi-turn step-specific reasoning and memory
- Two-stage training: Stage 1 strengthens privilege-following by jointly optimizing rollouts with and without privileged guidance from the same GUI states; Stage 2 selectively distills step-specific reasoning and memory guidance through a privilege-conditioned self-teacher
- Achieves state-of-the-art on AndroidWorld and MobileWorld benchmarks in both Pass@1 and Pass@3, outperforming prior OPSD baselines
- Extends a dense token-level supervision approach (from [[2026-08-17-le-critique-privileged-value-functions-for-llm-reinforcemen]]) into the multi-turn GUI grounding setting

## Relevance

Connects to the agentic RL thread via on-policy self-distillation (related to EvoCUA-1.5 STEPO and Le Critique's privileged value functions). The multi-turn GUI agent setting with step-specific memory guidance is adjacent to the ECHO turn-selective memory and GRAFT/SALT step-level credit threads. Weaker connection than GRAFT/SALT but relevant to the multimodal + agentic intersection.

## My Thoughts

<!-- Add your own notes here -->
