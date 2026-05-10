---
title: "Milestone-Guided Policy Learning for Long-Horizon Language Agents"
authors: ["Zixuan Wang", "Yuchen Yan", "Hongxing Li", "Teng Pan", "Dingming Li", "Ruiqing Zhang", "Weiming Lu", "Jun Xiao", "Yueting Zhuang", "Yongliang Shen"]
date: 2026-05-07
arxiv_id: "2605.06078"
url: "http://arxiv.org/abs/2605.06078v1"
score: 0.90
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Milestone-Guided Policy Learning for Long-Horizon Language Agents

## Summary

BEACON addresses two root causes of RL failure on long-horizon agentic tasks — credit misattribution (early correct actions penalized by terminal failures) and sample inefficiency (sparse successes yield near-zero learning signal) — by partitioning trajectories at milestone boundaries and applying temporal reward shaping within segments. Dual-scale advantage estimation (segment-level and global) prevents distant failures from corrupting local action evaluation, achieving 92.9% on ALFWorld versus GRPO's 53.5% while improving effective sample utilization from 23.7% to 82.0%.

## Key Contributions

- Identifies credit misattribution and sample inefficiency as the two root causes of RL failure on long-horizon agentic tasks
- BEACON framework: trajectory partitioning at milestone boundaries + temporal reward shaping within segments
- Dual-scale advantage estimation that isolates local-action credit from distant terminal outcomes
- 92.9% success on long-horizon ALFWorld (vs 53.5% GRPO), effective sample utilization 23.7%→82.0%

## Relevance

Directly advances the user's core interest in agentic RL training — this paper explains *why* GRPO fails on multi-step tasks and introduces a principled fix. It complements today's MiRA paper (also milestone-based rewards) with a more mechanistic credit-assignment framing, and connects to prior digest coverage of step-level credit assignment (StePPO, ProceedRL from May 1–4).

## My Thoughts

<!-- Add your own notes here -->
