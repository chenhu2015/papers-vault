---
title: "Bidirectional Context Self-Distillation for Reinforcement Learning of Skill-Based LLM Agents"
authors: ["Tianjun Pan", "Yuan Li", "Hongda Wang", "Linbo Jin", "Mengfei Song", "Lei Gao", "Qiming Shi", "Shaokang Fu", "Jiarong Zhao", "Chengyu Wang", "Chengfu Huo"]
date: 2026-08-10
arxiv_id: "2608.09555v1"
url: "http://arxiv.org/abs/2608.09555v1"
score: 0.72
topics: [agentic RL, LLM agent, reinforcement learning]
status: unread
---

# Bidirectional Context Self-Distillation for Reinforcement Learning of Skill-Based LLM Agents

## Summary

BCSD (Bidirectional Context Self-Distillation) addresses the underexplored problem of skill utilization quality in skill-based LLM agents: task-level RL rewards offer no direct signal for whether the policy uses provided skills effectively. It evaluates each trajectory from two complementary context views — an augmented view (with higher-level Meta-Skill guidance) and a reduced view (with general guidance pruned to task-specific skills) — and rescales the RL advantage by combining their token-level divergence signals. Experiments on ALFWorld and WebShop show consistent improvements across model scales.

## Key Contributions

- Identifies **skill utilization gap**: external skills improve agent performance in principle, but RL with task-level rewards cannot supervise *how* effectively the policy uses those skills
- **Augmented context view**: introduces Meta-Skill guidance (higher-level abstraction of available skills) to provide richer skill context for the distillation teacher
- **Reduced context view**: prunes general guidance to highlight task-specific skills, providing a contrastive minimal-guidance signal
- Combines both views' token-level divergence signals to rescale the RL advantage; demonstrated on ALFWorld and WebShop across model scales

## Relevance

BCSD connects directly to Gap #21 (complexity threshold for skill management): it is the first paper in the vault that explicitly supervises skill utilization quality during RL training rather than treating skill selection/scheduling as the primary problem. The bidirectional context views (augmented vs. reduced) provide a contrastive signal about skill relevance that is analogous to the SSOPD correct/wrong branch contrast — both use within-trajectory contrast to extract dense supervision without external labels. The Meta-Skill augmentation also echoes the vault's UCOB skill evolution thread.

## My Thoughts

<!-- Add your own notes here -->
