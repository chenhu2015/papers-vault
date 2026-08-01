---
title: "On-Policy Distillation with Curriculum Turn-level Guidance for Multi-turn Agents"
authors: ["Gengsheng Li", "Mao Zheng", "Mingyang Song", "Ruiqi Liu", "Tianyu Yang", "Jie Sun", "Qiyong Zhong", "Haiyun Guo", "Junfeng Fang", "Dan Zhang", "Jinqiao Wang"]
date: 2026-06-14
arxiv_id: "2606.15912"
url: "https://arxiv.org/abs/2606.15912"
score: 0.73
topics: [agentic RL, LLM agent]
status: unread
---

# On-Policy Distillation with Curriculum Turn-level Guidance for Multi-turn Agents

## Summary

Guided-OPD identifies a compound error failure mode in on-policy distillation for multi-turn agents: student errors compound across turns and push trajectories off the teacher's distribution exactly where the student most needs guidance. It mixes teacher- and student-generated turns within each rollout and schedules teacher intervention probability along a curriculum that decays to zero, recovering purely on-policy behavior at inference. Improves over vanilla OPD by 21.1% Score and 25.5% Success Rate on ALFWorld, ScienceWorld, and WebShop, with larger gains for smaller students.

## Key Contributions

- **Compound error diagnosis**: formalizes why vanilla on-policy distillation fails for multi-turn agents — student errors push trajectories off-distribution at exactly the turns where teacher supervision is most needed
- **Mixed-trajectory rollouts**: teacher- and student-generated turns interleaved within each rollout, keeping trajectories partially on the teacher's distribution even as student errors accumulate
- **Curriculum teacher decay**: teacher intervention probability scheduled to decay to zero, transitioning from teacher-anchored to fully student-on-policy behavior over training
- Gains scale inversely with student size: largest improvements on the smallest (weakest) students where compounding error is most severe

## Relevance

Addresses a multi-turn distillation failure mode that is structurally distinct from the credit assignment challenges in the IG-based family: rather than asking which turns to reward more (credit assignment), Guided-OPD asks how to prevent teacher supervision from becoming unreliable during the distillation process itself, connecting to SkillRise's cross-task skill evolution (Jul 31) and to the broader question of how knowledge is reliably transferred across capability levels in agentic RL settings.

## My Thoughts

<!-- Add your own notes here -->
