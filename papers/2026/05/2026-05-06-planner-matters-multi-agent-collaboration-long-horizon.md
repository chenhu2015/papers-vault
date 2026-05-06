---
title: "Planner Matters! An Efficient and Unbalanced Multi-agent Collaboration Framework for Long-horizon Planning"
authors: ["Wenyi Wu", "Sibo Zhu", "Kun Zhou", "Biwei Huang"]
date: 2026-05-04
arxiv_id: "2605.02168v1"
url: "https://arxiv.org/abs/2605.02168v1"
score: 0.81
topics: [agentic RL, LLM agent, tool use, reward model]
status: unread
---

# Planner Matters! An Efficient and Unbalanced Multi-agent Collaboration Framework for Long-horizon Planning

## Summary

This work provides a systematic compute-allocation analysis of multi-agent LLM systems (planner, actor, memory manager), finding that planning is the dominant factor for task performance while execution and memory management require far less model capacity. It introduces planner-centric RL that exclusively optimises the planner using trajectory-level rewards from a VLM-as-judge while freezing executor and memory components, avoiding wasted compute on non-bottleneck roles. Evaluated on web navigation, OS control, and tool-use benchmarks, the approach achieves robust and compute-efficient improvements in long-horizon agent automation.

## Key Contributions

- Systematic compute-allocation analysis showing planning dominates performance; execution/memory are not bottlenecks
- Planner-centric RL: only the planner is trained via RL; other components are frozen, focusing compute and gradient flow
- VLM-as-judge provides trajectory-level rewards without requiring dense per-step reward functions
- Demonstrated on web navigation, OS control, and tool use — practical agentic benchmarks

## Relevance

This paper connects to the multi-agent orchestration thread (RL for LLM MAS) but from a practical compute-allocation angle: it validates that not all components of a multi-agent system deserve RL training, echoing the hierarchical RL approach of HeRL and complementing the credit-assignment focus of AEM and ProceedRL. The VLM-as-judge reward is the multi-agent counterpart of Oracle-RLAIF's oracle ranker.

## My Thoughts

<!-- Add your own notes here -->
