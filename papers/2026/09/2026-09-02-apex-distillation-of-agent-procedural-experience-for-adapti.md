---
title: "APEx: Distillation of Agent Procedural Experience for Adaptive Deep Research Question Answering"
authors: ["Jie Ding", "Rui Sun", "Xinyuan Zhang", "Zeyu Zhang", "Xin Liu"]
date: 2026-09-02
arxiv_id: "2609.02253v1"
url: "http://arxiv.org/abs/2609.02253v1"
score: 0.83
topics: [agentic RL, RL training, LLM agent, GRPO, tool use]
status: unread
---

# APEx: Distillation of Agent Procedural Experience for Adaptive Deep Research Question Answering

## Summary

APEx organizes agent interaction history into instance-level trajectory memories and category-level procedural skills, coupling them through a closed-loop Executor–Distiller–Planner architecture optimized via three-stage alternating GRPO. At test time, distilled skills serve as procedural priors for skill-guided test-time RL adaptation without ground-truth labels, using skill-alignment regularization to prevent policy drift. APEx surpasses GPT-5.4 by 14.7 points and the strongest memory-augmented baseline by 3.0 points across 7 benchmarks.

## Key Contributions

- Two-level experience hierarchy: instance-level trajectory memories + category-level procedural skills
- Three-stage alternating GRPO: Executor, Distiller, Planner each receive GRPO training in staged rounds, enabling reward-guided skill distillation
- Ground-truth-free test-time adaptation: skill-guided TTL with skill-alignment regularization prevents policy drift without labels
- +14.7 over GPT-5.4, +3.0 over strongest memory-augmented baseline across 7 benchmarks

## Relevance

APEx sits at the intersection of the memory-agent thread (MemAgent, Learning-to-Remember) and the agentic OPD thread (STRIDE, RetireOPD), adding a skill-distillation layer that bridges the two. Its test-time RL adaptation without ground-truth labels also partially addresses the SFT-free VLM RL gap in the reasoning-agent domain.

## My Thoughts

<!-- Add your own notes here -->
