---
title: "Skill1: Unified Evolution of Skill-Augmented Agents via Reinforcement Learning"
authors: ["Yaorui Shi", "Yuxin Chen", "Zhengxi Lu", "Yuchun Miao", "Shugui Liu", "Qi GU", "Xunliang Cai", "Xiang Wang", "An Zhang"]
date: 2026-05-07
arxiv_id: "2605.06130v3"
url: "http://arxiv.org/abs/2605.06130v3"
score: 0.81
topics: [agentic RL, RL training, tool use, LLM agent]
status: unread
---

# Skill1: Unified Evolution of Skill-Augmented Agents via Reinforcement Learning

## Summary

Skill1 co-evolves skill selection, utilization, and distillation under a single task-outcome reward, avoiding partial or conflicting evolution from separate reward sources. The key insight: low-frequency reward trend credits selection quality while high-frequency variation credits distillation quality — two credit signals from one scalar. Ablations on ALFWorld and WebShop confirm that removing either credit signal degrades all three co-evolved capabilities.

## Key Contributions

- Unifies skill selection, utilization, and distillation into a single policy trained on a single task-outcome reward
- Signal decomposition: low-frequency trend of the task reward → selection credit; high-frequency variation → distillation credit
- Single-model design avoids the architectural complexity of separate skill generator + task executor (contrast with Skill-R1)
- Ablations confirm co-evolution: removing any credit signal degrades all three capabilities, not just the targeted one

## Relevance

Skill1 sits in direct dialogue with Skill-R1 (also today): Skill-R1 uses an explicit bi-level GRPO with separate intra/inter-generation objectives; Skill1 derives two credit signals from one scalar by frequency decomposition. Both target the same problem (recurrent skill credit assignment) with opposite design philosophies. Skill1's single-model unification is architecturally closer to SPyCE (Aug 23), while Skill-R1's frozen-executor approach is the complement for closed-source LLM scenarios.

## My Thoughts

<!-- Add your own notes here -->
