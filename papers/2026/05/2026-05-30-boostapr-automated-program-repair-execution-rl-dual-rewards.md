---
title: "BoostAPR: Boosting Automated Program Repair via Execution-Grounded Reinforcement Learning with Dual Reward Models"
authors: ["Yuanhao Li", "Hongbo Wang", "Xiaotang Shang", "Xunzhu Tang", "Yiming Cao", "Xuhong Chen"]
date: 2026-05-09
arxiv_id: "2605.09134"
url: "http://arxiv.org/abs/2605.09134v3"
score: 0.83
topics: [PPO, reward model, RL training, agentic, RLHF]
status: unread
---

# BoostAPR: Boosting Automated Program Repair via Execution-Grounded Reinforcement Learning with Dual Reward Models

## Summary

BoostAPR trains dual reward models from execution outcomes — a sequence-level assessor and a line-level credit allocator — then uses PPO to redistribute rewards to critical edit regions at a granularity naturally suited to code diffs. Achieving 40.7% on SWE-bench Verified (+22.9pp over base) and strong cross-language transfer to Defects4J (Python→Java), it sets a new state of the art for RL-driven automated program repair.

## Key Contributions

- Dual reward model architecture: sequence-level assessor + line-level credit allocator from execution outcomes
- PPO with line-level credit redistribution at edit-region granularity intermediate between token and trajectory
- 40.7% on SWE-bench Verified (+22.9pp), 24.8% on Defects4J, 84.5% HumanEval-Java, 95.0% QuixBugs
- Strong cross-language generalization (Python → Java) without language-specific fine-tuning

## Relevance

Fresh angle on code RL (May 29) — automated program repair rather than code generation — with dual reward models that provide intermediate-granularity credit assignment, a distinct contribution from the May 29 code RL papers.

## My Thoughts

<!-- Add your own notes here -->
