---
title: "AEM: Adaptive Entropy Modulation for Multi-Turn Agentic Reinforcement Learning"
authors: ["Haotian Zhao", "Yuxin Zhang", "Songlin Zhou", "Stephen S. -T. Yau", "Wenyu Zhang", "Lun Tian", "Tianshu Zhu", "Yifeng Huang", "Yucheng Zeng", "Jingnan Gu", "Daxiang Dong", "Jianmin Wu"]
date: 2026-05-01
arxiv_id: "2605.00425v1"
url: "http://arxiv.org/abs/2605.00425v1"
score: 0.88
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# AEM: Adaptive Entropy Modulation for Multi-Turn Agentic Reinforcement Learning

## Summary

AEM proposes a supervision-free credit assignment method for multi-turn agentic RL by adaptively modulating entropy dynamics during training. Elevating entropy analysis from token level to response level, the authors derive a practical proxy — the product of advantage and relative response surprisal — that naturally transitions the policy from exploration to exploitation without process reward models or auxiliary self-supervised signals. On SWE-bench-Verified, AEM yields a +1.4% gain over a SOTA baseline across models ranging from 1.5B to 32B parameters.

## Key Contributions

- Elevates entropy analysis from token level to response level, reducing token sampling variance in multi-turn settings
- Derives a closed-form proxy (advantage × relative response surprisal) that governs entropy drift under natural gradients
- Achieves supervision-free credit assignment without process reward models or self-supervised auxiliary signals
- Demonstrates +1.4% on SWE-bench-Verified and consistent gains across 1.5B–32B models and multiple agentic benchmarks

## Relevance

The core problem — how to assign credit across steps in sparse-reward agentic RL without a process reward model — directly intersects with earlier papers in the vault (StepPO, ProceedRL, Segmental Advantage Estimation). AEM's entropy-modulation angle is complementary to those step-level MDP and segment-boundary approaches, and its supervision-free nature makes it the most practically deployable among them.

## My Thoughts

<!-- Add your own notes here -->
