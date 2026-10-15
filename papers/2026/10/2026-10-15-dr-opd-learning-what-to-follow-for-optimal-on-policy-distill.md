---
title: "Dr. OPD: Learning What to Follow for Optimal On-Policy Distillation of Large Language Models"
authors: ["Zhenyu Wang", "Tianze Wang", "Linjun Zhang", "Yifan Hu"]
date: 2026-10-15
arxiv_id: "2609.38025v1"
url: "https://arxiv.org/abs/2609.38025"
score: 0.80
topics: [RL training, RLHF, reward model, LLM agent]
status: unread
---

# Dr. OPD: Learning What to Follow for Optimal On-Policy Distillation of Large Language Models

## Summary

Dr. OPD frames token-level weighted on-policy distillation as a bilevel optimisation problem: token weights are selected to maximise the student's expected reward rather than simply match teacher output. The iterative solver alternates between closed-form weight updates and gradient steps on the weighted OPD objective, with a proof that this achieves higher expected reward than vanilla OPD. On strong-to-weak distillation, Dr. OPD improves average math performance by 9.7 points over vanilla OPD and enables the smaller student to surpass its larger teacher.

## Key Contributions

- Bilevel formulation: outer problem selects token weights to maximise student reward; inner problem learns from the weighted OPD objective
- Closed-form weight update alternating with gradient steps — efficient iterative solver without additional models
- Theoretical guarantee: weighted update achieves strictly higher expected reward than vanilla OPD under regularity conditions
- Strong-to-weak distillation: smaller student surpasses larger teacher on math benchmarks with this weighting

## Relevance

Connected to the token-level credit assignment thread — Dr. OPD's reward-maximising token weights are the distillation-side analogue of LVRL's value-estimated step-level credit. Together they suggest that the right question for both RL and distillation is "which tokens matter for outcome?" rather than "which tokens did the teacher predict confidently?"

## My Thoughts

<!-- Add your own notes here -->
