---
title: "Stabilizing On-Policy Targeted Guidance in Agentic Reinforcement Learning"
authors: ["Kevin Frans", "Alexander M Rush", "Sergey Levine", "Pieter Abbeel", "Ashvin Nair"]
date: 2026-11-03
arxiv_id: "2611.05266v2"
url: "https://arxiv.org/abs/2611.05266"
score: 0.87
topics: [agentic RL, LLM agent, reinforcement learning, tool use, RLHF]
status: unread
---

# Stabilizing On-Policy Targeted Guidance in Agentic Reinforcement Learning

## Summary

Introduces 'targeted guidance': per-turn textual feedback from judge models is converted to a self-distillation objective alongside a per-criteria RL reward, stabilising on-policy agentic RL without degrading baseline performance. Key finding is that feedback should be restricted to turns where the policy specifically fails; this prevents entropy oscillation throughout training. Evaluated on multi-turn software-engineering tasks where naïve RL cannot explore to sufficient reward coverage.

## Key Contributions

- Self-distillation on per-turn textual feedback from judge models as a directional exploration signal
- Per-criteria RL reward combined with targeted self-distillation to prevent baseline RL degradation
- Failure-gated feedback: guidance limited to failure turns to maintain stable entropy throughout training
- Demonstrated on multi-turn software engineering agentic environment with hard-to-optimise rewards

## Relevance

Directly extends the AutoScaffold + JoMoHa adaptive scaffolding cluster from Nov 12: where AutoScaffold uses a frozen teacher to design scaffolds and JoMoHa co-trains the harness, this work addresses how to inject rich textual guidance stably without destabilising the RL objective. The failure-gating mechanism is a novel stabilisation insight that the other two papers don't address.

## My Thoughts

<!-- Add your own notes here -->
