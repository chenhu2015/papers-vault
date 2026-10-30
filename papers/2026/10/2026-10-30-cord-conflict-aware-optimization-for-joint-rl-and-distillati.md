---
title: "CORD: Conflict-Aware Optimization for Joint RL and Distillation in Agents"
authors: ["Wenhao Yu", "Zhengcheng Wang", "Jiahong Liu", "Zexuan Qiu", "Minda Hu", "Shaohang Wei", "Jiafei Lyu", "Junyan Lyu", "Haobo Fu", "Irwin King"]
date: 2026-10-30
arxiv_id: "2610.29965v1"
url: "http://arxiv.org/abs/2610.29965v1"
score: 0.85
topics: [agentic RL, RL training, LLM agent, reinforcement learning]
status: unread
---

# CORD: Conflict-Aware Optimization for Joint RL and Distillation in Agents

## Summary

CORD is a general framework for conflict-aware gradient optimization when jointly training agents with RL task rewards and dense distillation supervision, whose gradients can partially cancel. A nearest-point projection formulation yields a closed-form per-mini-batch update that selectively removes conflicting gradient components, separating the choice of protected objective from the projection trigger. Applied across three joint training recipes on ALFWorld, CORD improves success by 1.5–15.9 percentage points; on WebShop SDAR rises from 60.7% to 64.6%.

## Key Contributions

- Identifies gradient conflict between RL task rewards and dense teacher distillation as a key obstacle in agent training
- Nearest-point projection gives a closed-form gradient update that removes conflict while preserving protected objective direction
- Separates the protection direction from the conflict detection condition — prior approaches conflate these
- Improves across three distinct joint training recipes; ALFWorld +1.5–15.9pp; WebShop SDAR +3.9pp

## Relevance

Complements the long-horizon agentic RL thread by addressing a fundamental optimization-level problem: when RL and distillation are combined (as in RSIPO, TSRL, and other papers in the vault), gradient conflicts can silently reduce performance. CORD provides a general mechanism applicable to any joint RL+distillation recipe, making it broadly relevant to the entire agentic RL and RL training threads.

## My Thoughts

<!-- Add your own notes here -->
