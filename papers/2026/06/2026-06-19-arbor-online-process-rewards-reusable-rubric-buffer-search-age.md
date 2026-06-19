---
title: "ARBOR: Online Process Rewards via a Reusable Rubric Buffer for Search Agents"
authors: ["Zheng Liu", "Longxiang Zhang", "Xintong Wang", "Zhiang Xu", "Shaoxiong Zhan", "Xin Shan", "Wen Huang", "Tao Dai", "Shu-Tao Xia", "Chengfu Huo", "Liang Ding"]
date: 2026-06-19
arxiv_id: "2606.03239v1"
url: "http://arxiv.org/abs/2606.03239v1"
score: 0.87
topics: [GRPO, reward model, agentic RL, LLM agent, process reward]
status: unread
---

# ARBOR: Online Process Rewards via a Reusable Rubric Buffer for Search Agents

## Summary

GRPO-trained search agents face a zero-gradient failure mode when all trajectories in a group share the same correctness, yielding zero within-group advantage. ARBOR fixes this by maintaining a reusable rubric memory: query-local rubric drafts induced from contrastive trajectories are consolidated into cross-query common rubrics, and sparse pairwise judging applies them as process rewards supplementing the base outcome reward. This converts up to 42% of otherwise-zero-gradient training groups into informative gradient signal, raising LLM-judge accuracy by up to 4.2 points on multi-hop QA.

## Key Contributions

- Identifies GRPO's outcome-homogeneous group problem (zero within-group advantage when all trajectories correct or all incorrect) as a fundamental training failure mode for search agents
- Rubric buffer with three lifecycle stages: draft induction from contrastive trajectories, consolidation into cross-query common rubrics, and retirement as the policy evolves
- Sparse pairwise judging over a small active rubric subset scores trajectories for process reward, adding gradient signal without a costly trained verifier
- Consistently outperforms GRPO and DAPO baselines on four multi-hop QA benchmarks

## Relevance

Directly complements the process reward thread (PRISM, Distributional PRMs — Jun 13-14) by providing an *online*, self-improving process reward without a pre-trained PRM; the rubric memory grows and specializes with the policy rather than being fixed. The zero-gradient problem it solves is the same structural issue that RODS (Jun 18) addressed from the data-synthesis side — when GRPO has no within-group variance, neither credit assignment nor data selection can improve the policy. ARBOR's solution (inject process reward) is orthogonal to RODS's (select boundary-proximity data), and the two could compound.

## My Thoughts

<!-- Add your own notes here -->
