---
title: "Ecdysis: Efficient and Effective Training of Runtime Harnesses for LLM Agents"
authors: ["Ruiqing Yue", "Yu Cui", "Zhuoyu Sun", "Sicheng Pan", "Xianhong Xue", "Tingyu Li", "Ting Li", "Wenzhuo Zhu", "Yi Chen", "Yifei Liu", "Baohan Huang", "Zhe Cui", "Haibin Zhang", "Cong Zuo"]
date: 2026-09-10
arxiv_id: "2609.11677v1"
url: "https://arxiv.org/abs/2609.11677"
score: 0.80
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# Ecdysis: Efficient and Effective Training of Runtime Harnesses for LLM Agents

## Summary

Ecdysis addresses the harness evolution bottleneck by identifying lack of principled failure diagnosis as the key issue: individual failures can reflect model-specific deficiencies or systematic harness deficiencies, and directly optimizing against individual failures risks unnecessary model-specific accommodation. It introduces batch-level cross-instance failure aggregation to jointly analyze failure evidence across multiple tasks, coupled with Failure-Driven Collaborative Refinement (multi-role diagnosis + iterative harness modification). Achieves 1.84x speedup in harness training with 18.56% improvement in reasoning accuracy over prior harness evolution methods.

## Key Contributions

- Model-specific vs. harness-level failure distinction: formal identification that an observed failure can reflect model deficiency (no harness fix needed) or systematic harness deficiency (harness fix needed) — existing methods conflate the two
- Cross-instance failure aggregation: batch-level joint analysis of failure evidence across multiple task instances to identify recurring cross-task failure patterns — surfaces systematic harness deficiencies that single-instance analysis misses
- Failure-Driven Collaborative Refinement: multi-role diagnosis (failure cause attribution) + iterative harness modification specifications — addresses systematic patterns rather than individual failure patches
- 1.84x speedup + 18.56% accuracy improvement over existing harness evolution methods

## Relevance

Ecdysis directly addresses the model-harness compatibility gap identified Sep 08-09 (from Co-Evolving Harnesses): the distinction between model-specific accommodation and harness-level repair is the precise operationalization of "compatibility as an explicit training objective" that was missing. While Ecdysis does not jointly optimize model weights and harness (the core gap remains open), it provides the diagnostic mechanism (cross-instance failure aggregation) that would be necessary for joint optimization. This positions Ecdysis as the diagnosis layer for a future joint optimization system.

## My Thoughts

<!-- Add your own notes here -->
