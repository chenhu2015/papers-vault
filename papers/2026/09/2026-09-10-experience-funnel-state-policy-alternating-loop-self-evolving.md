---
title: "Experience Funnel: A State-Policy Alternating Loop for Self-Evolving Agents"
authors: ["Wenbo Gao", "Zhaomou Song", "Zhiyuan Ji", "Renxi Liu", "Xing Li", "Xianzhi Yu", "Xiaoguang Li", "James Chung-wai Cheung", "Weizhe Lin", "Yaoyuan Wang"]
date: 2026-09-10
arxiv_id: "2609.08919v1"
url: "https://arxiv.org/abs/2609.08919v1"
score: 0.80
topics: [agentic RL, LLM agent, RL training]
status: unread
---

# Experience Funnel: A State-Policy Alternating Loop for Self-Evolving Agents

## Summary

Experience Funnel couples fast explicit state adaptation (skills and agent harness) with slow parametric policy consolidation in an alternating loop: trajectories are first distilled into a textual state for rapid, human-editable adaptation, then state-enabled behaviors that survive state revision are selectively consolidated into the policy via transition-aware distillation, and new rollouts close the loop for the next round. This avoids persistent context dependence (pure state) and slow update latency (pure policy) simultaneously, outperforming both state-only evolution and direct policy internalization across diverse agent benchmarks.

## Key Contributions

- **Dual-speed adaptation**: explicit textual state (fast, context-dependent) + parametric policy (slow, reusable) in alternating loop
- **Transition-aware distillation**: selectively identifies state-enabled behaviors that remain useful across state revisions for policy consolidation
- **Self-closing loop**: updated state-policy pair generates new rollouts for next round, enabling continual self-improvement
- **Beats both extremes**: outperforms state-only evolution (no policy learning) and direct policy internalization (no state adaptation) across diverse benchmarks

## Relevance

Experience Funnel is structurally related to the model-harness compatibility gap surfaced by Co-Evolving Harnesses (Sep 09): it directly formalizes how explicit state (harness/skills) and implicit policy can co-evolve, and its transition-aware distillation is the inverse of Co-Evolving Harnesses' on-policy correction (which recovers policy from harness evolution). Together they suggest a broader design space of state-policy co-evolution that no single paper has explored jointly.

## My Thoughts

<!-- Add your own notes here -->
