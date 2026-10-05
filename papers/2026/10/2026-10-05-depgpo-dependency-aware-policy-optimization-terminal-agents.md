---
title: "Credit Where It Matters: Dependency-Aware Policy Optimization for Terminal Agents"
authors: ["Yu Li", "Guangfeng Cai", "Long-Fei Li", "Shuo Han", "Shengtian Yang", "Han Luo", "Kaibing Yang", "Lei Feng"]
date: 2026-10-05
arxiv_id: "2610.03634v1"
url: "https://arxiv.org/abs/2610.03634"
score: 0.91
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Credit Where It Matters: Dependency-Aware Policy Optimization for Terminal Agents (DepGPO)

## Summary

DepGPO constructs a command dependency graph from execution traces and traces backward from the resources inspected by the task verifier, assigning credit only to writes and their supporting reads that lie on causal paths to the outcome. The resulting redistributed trajectory advantages eliminate credit assigned to commands that neither produce nor consume resources relevant to the final result. Experiments on complex terminal tasks show improved task performance and training stability over trajectory- and step-level baselines.

## Key Contributions

- Command dependency graph built from execution traces (read-write relationships between terminal commands)
- Backward trace from task-verifier-inspected resources identifies causally relevant writes and their supporting reads
- Advantage redistribution: relevant steps receive credit, irrelevant operations are zeroed out
- Outperforms both trajectory-level and uniform step-level baselines on complex coding/debugging tasks

## Relevance

This is the 12th entry in the step-credit cluster and the first to use execution-level causal tracing (read-write dependency graphs) as the credit signal. It is conceptually related to DARS (predicate-DAG with distilled annotator) — both use graph structure to identify credit-worthy steps — but DepGPO derives its graph automatically from execution traces rather than a trained annotator. The terminal/coding domain is the first non-web-agent domain in the cluster since SCA (GUI) and PF-RL (VLA), confirming that execution-trace credit is domain-independent.

## My Thoughts

<!-- Add your own notes here -->
