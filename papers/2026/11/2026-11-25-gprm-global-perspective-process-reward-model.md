---
title: "GPRM: Global Perspective Process Reward Model"
authors: ["Zifan Zhang", "Zhengbo Jiao", "Shaobo Wang", "Jing Zhou", "Guoyi Li", "Jiayi Chen", "Wei Wang", "Bing Zhao", "Cheng Fang", "Xiaoxiao Xu", "Hu Wei", "Linfeng Zhang", "Lin Qu"]
date: 2026-11-16
arxiv_id: "2611.20755v1"
url: "http://arxiv.org/abs/2611.20755v1"
score: 0.76
topics: [reward model, GRPO, RL training, RLHF]
status: unread
---

# GPRM: Global Perspective Process Reward Model

## Summary

GPRM jointly models the problem, all previous steps with their evaluations, the current step, and future steps for history-aware and globally-informed process reward. A four-dimensional evaluation framework (look back, look ahead, self-check, goal alignment) structures this into SFT+GRPO training data. Despite using less data and smaller models than baselines, GPRM outperforms them by 7.8 and 5.4 points on PRMBench and ProcessBench, and also surpasses GPT-4.1 on Agent Error Bench.

## Key Contributions

- Global context PRM: models problem + prior steps+evaluations + current step + future steps simultaneously
- Four-dimensional evaluation: look back (prior consistency), look ahead (future plausibility), self-check (step validity), goal alignment (task alignment)
- SFT+GRPO training pipeline; outperforms baselines with less data and smaller models
- +~4 points on test-time scaling, competitive on PPE, surpasses GPT-4.1 on Agent Error Bench

## Relevance

Extends the multimodal PRM / test-time scaling thread with a principled architecture that explicitly incorporates future-step context — most PRMs ignore what comes after the current step. The agent-error benchmark result suggests cross-task generalizability beyond math reasoning.

## My Thoughts

<!-- Add your own notes here -->
