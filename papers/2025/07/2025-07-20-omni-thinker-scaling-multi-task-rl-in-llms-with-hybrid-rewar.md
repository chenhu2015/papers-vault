---
title: "Omni-Thinker: Scaling Multi-Task RL in LLMs with Hybrid Reward and Task Scheduling"
authors: ["Derek Li", "Jiaming Zhou", "Leo Maxime Brunswic", "Abbas Ghaddar", "Qianyi Sun", "Liheng Ma", "Yu Luo", "Dong Li", "Mark Coates", "Jianye Hao", "Yingxue Zhang"]
date: 2025-07-20
arxiv_id: "2507.14783v3"
url: "http://arxiv.org/abs/2507.14783v3"
score: 0.80
topics: [agentic RL, RL training, RLHF, reward model]
status: unread
---

# Omni-Thinker: Scaling Multi-Task RL in LLMs with Hybrid Reward and Task Scheduling

## Summary

Omni-Thinker scales LLM RL across heterogeneous tasks by combining hybrid rewards (rule-based verifiable signals + LLM-as-Judge preference evaluations) with backward-transfer-guided (BWT) task scheduling that reduces catastrophic forgetting. The BWT scheduler prioritizes tasks in order of measured accuracy backward transfer, enabling multi-task training of both structured reasoning and open-ended generation domains simultaneously. Experiments across four domains show 6.2% gains over joint training and 12.4% over model merging.

## Key Contributions

- Hybrid reward design: integrates deterministic rule-based rewards (for structured tasks) with LLM-as-Judge preference signals (for open-ended tasks) in a single RL framework
- BWT-aware scheduler: orders task introduction using backward transfer measurements to minimize forgetting when adding new task domains
- Theoretical grounding: shows simple accuracy-transfer assumptions yield accurate curriculum outcome predictions; entropy dynamics explain deviations in generative tasks
- 6.2% over joint training and 12.4% over model merging across four task domains

## Relevance

Surfaced from the open-ended reward intrinsic motivation search (2026-09-23). Fills the practical angle of the open-ended agent RL reward design gap: instead of intrinsic bonuses, it uses LLM-as-Judge as a differentiable preference signal for open-ended domains, enabling uniform RL training across structured + generative tasks. The BWT scheduling angle is a complementary framing to ACLArena's continual learning recipe.

## My Thoughts

<!-- Add your own notes here -->
