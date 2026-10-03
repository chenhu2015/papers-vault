---
title: "My FAULT: Self-Diagnosis as Credit Assignment in Self-Evolving Agentic Reinforcement Learning"
authors: ["Yihua Zhu", "Qianying Liu", "Weixu Qiao", "Xuan Ren", "Weiwei Xu", "Wenbo Li", "Wei Wang", "Ruijia Chen", "Xinmiao Luan", "Yin Luo", "Hao Huang", "Xiang Zheng", "Hidetoshi Shimodaira"]
date: 2026-10-01
arxiv_id: "2610.01161"
url: "https://arxiv.org/abs/2610.01161"
score: 0.88
topics: [agentic RL, RL training, GRPO]
status: unread
---

# My FAULT: Self-Diagnosis as Credit Assignment in Self-Evolving Agentic Reinforcement Learning

## Summary

FAULT addresses two fundamental credit-assignment failures in agentic RL: same-outcome rollout groups yield no gradient signal from terminal rewards, and trajectory-level rewards cannot localize which specific decisions caused failure. The method converts self-diagnosed errors into explicit step-level credit anchored by terminal outcomes — checking diagnostic evidence and learning relative error costs from task outcomes online — while the policy and self-diagnoser co-evolve during training. Achieves 95% signal coverage on ALFWorld vs. 41% for GRPO and 72% for GiGPO, with strong improvements on long-horizon ALFWorld and WebShop tasks.

## Key Contributions

- Identifies and directly addresses same-outcome group problem (41% GRPO signal coverage) by using self-diagnosis to differentiate trajectories reaching the same terminal reward
- Self-diagnoser proposes step-level error attributions; FAULT anchors these to observed terminal outcomes to correct unreliable diagnoses
- Error costs learned online from recent outcomes; policy and diagnoser co-evolve throughout training
- 95% signal coverage on ALFWorld demonstrates the practical severity of the same-outcome problem that GRPO/GiGPO leave unaddressed

## Relevance

Adds a co-evolutionary dimension to the step-credit cluster — unlike T2SPO (regression from past successes), DARS (predicate-DAG), or TASPO (PI-weighted mean), FAULT's diagnoser adapts alongside the policy. The self-diagnosis approach is also related to the HaPRL human-process-annotation thread: where HaPRL uses human annotations for process credit, FAULT uses the model's own self-generated diagnoses, updated online.

## My Thoughts

<!-- Add your own notes here -->
