---
title: "SCOPE: Selective Critical-Step On-Policy Self-Distillation for Agentic Reinforcement Learning"
authors: ["Qirui Liu", "Wei Cao", "Yu Mi", "Yichen Sun", "Xuekun Zhang", "Lei Liu", "Yue Shen", "Zhixuan Chu"]
date: 2026-11-02
arxiv_id: "2610.38391v1"
url: "http://arxiv.org/abs/2610.38391v1"
score: 0.84
topics: [agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# SCOPE: Selective Critical-Step On-Policy Self-Distillation for Agentic Reinforcement Learning

## Summary

SCOPE tackles outcome-based RL's coarse supervision for long-horizon LLM agents by generating step-specific hindsight skills from trajectory self-analysis and distilling guidance only at identified error steps. A bounded signed teacher-student coefficient stabilizes updates while a success-relative pairwise length reward promotes efficiency. On ALFWorld with Qwen2.5-3B, SCOPE achieves 97.7% (seen) and 89.6% (unseen) success, outperforming GRPO by +23.2pp on unseen tasks with 46.7% fewer interactions; at Qwen3-32B scale, 99.2% seen and 94.0% unseen.

## Key Contributions

- Selective distillation: hindsight skills generated only for error steps, avoiding off-target distillation signals from trajectory-level skill shifts at unrelated steps
- Bounded signed teacher-student coefficient stabilizes auxiliary distillation updates while preserving RL positive reinforcement and negative correction
- Success-relative pairwise length reward encourages efficient task completion
- 97.7% ALFWorld / 85.2% WebShop with Qwen2.5-3B; +23.2pp over GRPO on unseen tasks with 46.7% fewer interactions

## Relevance

SCOPE sits at the intersection of the long-horizon agentic RL thread and the agentic RL self-improvement / skill thread. Its selective distillation addresses a specific failure of trajectory-level distillation (off-target signals at correct steps) that RSIPO's skill co-evolution also tries to solve from a different angle (recursive self-improving rather than hindsight). The 46.7% interaction reduction also connects to the RL rollout efficiency thread.

## My Thoughts

<!-- Add your own notes here -->
