---
title: "RetireOPD: Self-Retiring On-Policy Distillation for Agentic Reinforcement Learning"
authors: ["Yan Yu", "Zhengxi Lu", "Yizhou Liu", "Yichen Pan", "Aozhe Wang", "Qipeng Chen", "Hua Yang", "Wenqi Zhang", "Weiming Lu", "Qianglong Chen", "Yongliang Shen"]
date: 2026-09-17
arxiv_id: "2609.20784v1"
url: "http://arxiv.org/abs/2609.20784v1"
score: 0.83
topics: [agentic RL, RL training, LLM agent, RLAIF]
status: unread
---

# RetireOPD: Self-Retiring On-Policy Distillation for Agentic Reinforcement Learning

## Summary

RetireOPD addresses the finding that teacher reliability in OPD is not guaranteed by privilege alone and that distillation benefit is stage-dependent. It first trains a decoupled skill-conditioned teacher with environment rewards, then trains a skill-free student jointly with RL and OPD; the student self-detects when to retire the teacher by monitoring discrepancy convergence and success-rate fraction, after which training continues with RL alone. Across Qwen2.5 1.5B–7B, RetireOPD outperforms RL-only baseline by 14.1–18.8% on ALFWorld and 11.8–19.0% on WebShop, and surpasses its own skill-conditioned teacher in every setting.

## Key Contributions

- Decoupled teacher optimization: teacher is skill-conditioned and optimized independently with environment rewards before student training begins — avoids the feedback loop where a jointly trained teacher is unreliable
- Adaptive Retirement: student self-detects the transition from distillation-dominated to RL-dominated training by monitoring discrepancy and success fraction — no predefined schedule
- Empirical finding: privilege alone is insufficient for teacher reliability; stage-dependence is the load-bearing variable that prior OPD methods miss
- Scales across 1.5B–7B Qwen2.5 with consistent gains; student surpasses its own teacher in every configuration

## Relevance

RetireOPD is directly related to STRIDE (Sep 18, same day), which also targets multi-turn agentic OPD acceleration — but from a different angle: STRIDE accelerates rollouts using structural regularities in teacher endorsement, while RetireOPD redesigns the teacher-student coupling. Both papers independently arrive at the conclusion that static distillation schedules are suboptimal in agentic settings; RetireOPD's contribution is the self-detection mechanism, STRIDE's is the prefix-buffer data-curriculum. Together they narrow the gap toward adaptive OPD for multi-turn agents.

## My Thoughts

<!-- Add your own notes here -->
