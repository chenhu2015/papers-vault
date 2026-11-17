---
title: "Skill-SD: Skill-Conditioned Self-Distillation for Multi-turn LLM Agents"
authors: ["Hao Wang", "Guozhi Wang", "Han Xiao", "Yufeng Zhou", "Yue Pan", "Jichao Wang", "Ke Xu", "Yafei Wen", "Xiaohu Ruan", "Xiaoxin Chen", "Honggang Qi"]
date: 2026-04-12
arxiv_id: "2604.10674"
url: "https://arxiv.org/abs/2604.10674"
score: 0.87
topics: [agentic RL, LLM agent, tool use, RLHF, OPSD, multi-turn]
status: unread
---

# Skill-SD: Skill-Conditioned Self-Distillation for Multi-turn LLM Agents

## Summary

Extends OPSD to multi-turn agentic settings by converting completed agent trajectories into compact natural-language skills (behaviors, mistakes, workflows) that serve as dynamic privileged information conditioning the teacher, while the student always acts under the plain task prompt. Stabilizes training with an importance-weighted reverse-KL distillation loss and dynamic teacher-student synchronization; achieves +14.0%/+10.9% over vanilla GRPO on AppWorld/Sokoban and +42.1%/+40.6% over vanilla OPD.

## Key Contributions

- Dynamic skill-based PI: instead of fixed ground-truth answers, uses trajectory-derived natural-language skills as privileged information — capturing diverse valid strategies in agent tasks
- Importance-weighted reverse-KL loss for gradient-correct token-level distillation, preventing training collapse when combining OPSD with RL
- Dynamic teacher-student synchronization to track the improving student
- Large gains over both vanilla GRPO and vanilla OPD on AppWorld/Sokoban multi-turn benchmarks

## Relevance

SAGE-OPD (Nov 16) was the first multi-turn OPD paper in the vault, using verifier-free turn-level selective intervention. Skill-SD is the second, using a fundamentally different approach: rather than selecting which teacher turns to apply, it changes the nature of the teacher's PI itself — from fixed ground-truth to trajectory-derived skills. Together, SAGE-OPD + Skill-SD provide two orthogonal multi-turn OPSD mechanisms (selective intervention vs. dynamic PI generation). Directly addresses the November search goal of multi-turn agentic OPD depth.

## My Thoughts

<!-- Add your own notes here -->
