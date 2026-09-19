---
title: "HarnessForge: Joint Harness and Policy Evolution for Adaptive Agent Systems"
authors: ["mingju-c et al."]
date: 2026-06-01
arxiv_id: "2606.01779v1"
url: "http://arxiv.org/abs/2606.01779v1"
score: 0.85
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# HarnessForge: Joint Harness and Policy Evolution for Adaptive Agent Systems

## Summary

HarnessForge formulates agent systems as a harness–policy pair and performs joint co-evolution through fault-guided harness tailoring (updating execution structure based on failure analysis) and harness-conditioned policy alignment (training the reasoning policy relative to the current harness). This addresses the compatibility gap that harness-only or policy-only adaptation leaves open, with up to 12.0% gain over the strongest baseline across 5 benchmarks on both Qwen3-4B and Qwen3-8B.

## Key Contributions

- Harness–policy formulation: explicitly defines the adaptation space as the product of execution structure (harness) and reasoning behavior (policy)
- Fault-guided harness tailoring: updates harness structure by diagnosing failure modes rather than random search
- Harness-conditioned policy alignment: policy optimization conditions on the current harness state, maintaining executable compatibility
- Up to 12.0% improvement over harness-only and policy-only adaptation baselines on 5 diverse benchmarks

## Relevance

HarnessForge directly extends the ScienceBuddy (Sep 15) model-harness joint optimization thread: where ScienceBuddy uses recursive self-improvement loops to couple model and harness evolution, HarnessForge provides a formal adaptation space and fault-guided mechanism. The two papers are complementary characterizations of the same joint optimization problem.

## My Thoughts

<!-- Add your own notes here -->
