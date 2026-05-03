---
title: "ERA: Transforming VLMs into Embodied Agents via Embodied Prior Learning and Online Reinforcement Learning"
authors: ["Hanyang Chen", "Mark Zhao", "Rui Yang", "Qinwei Ma", "Ke Yang", "Jiarui Yao", "Kangrui Wang", "Hao Bai", "Zhenhailong Wang", "Rui Pan", "Mengchao Zhang", "Jose Barreiros", "Aykut Onol", "ChengXiang Zhai", "Heng Ji", "Manling Li", "Huan Zhang", "Tong Zhang"]
date: 2026-05-03
arxiv_id: "2510.12693v1"
url: "http://arxiv.org/abs/2510.12693v1"
score: 0.79
topics: [agentic RL, VLM, RL training, vision-language, multimodal]
status: unread
---

# ERA: Transforming VLMs into Embodied Agents via Embodied Prior Learning and Online Reinforcement Learning

## Summary

ERA is a two-stage framework that converts small VLMs into capable embodied agents: an Embodied Prior Learning stage distills trajectory reasoning, in-environment grounding, and external knowledge from stronger models; an online RL stage then adds dense reward shaping, self-summarization for long-horizon context management, and turn-level policy optimization. ERA-3B surpasses GPT-4o by 8.4% on high-level planning and 19.4% on low-level manipulation benchmarks with strong generalization to unseen tasks.

## Key Contributions

- Two-stage pipeline: prior knowledge distillation (trajectory, environment, external) followed by online RL fine-tuning
- Self-summarization mechanism for managing long-horizon context within the agent's context window
- Dense reward shaping and turn-level policy optimization to address sparse rewards and training instability in embodied tasks
- ERA-3B outperforms GPT-4o on both planning (EB-ALFRED) and manipulation (EB-Manipulation) benchmarks

## Relevance

This extends the VLM+RL thread in the profile from GUI agents (covered 2026-05-01) to physically embodied settings. The turn-level policy optimization echoes the step-level credit assignment work (StePPO), suggesting a convergent design pattern across agentic RL settings that's worth tracking.

## My Thoughts

<!-- Add your own notes here -->
