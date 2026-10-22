---
title: "Reinforcement Fine-Tuning for Reasoning towards Multi-Step Multi-Source Search in Large Language Models"
authors: ["Wentao Shi", "Yiqing Shen"]
date: 2026-10-22
arxiv_id: "2506.08352v1"
url: "http://arxiv.org/abs/2506.08352v1"
score: 0.82
topics: [agentic RL, tool use, LLM agent, GRPO, RL training]
status: unread
---

# Reinforcement Fine-Tuning for Reasoning towards Multi-Step Multi-Source Search in Large Language Models

## Summary

R-Search unifies multi-step planning, multi-source search execution, and answer synthesis in a single LLM using GRPO with a multi-component reward function covering answer correctness, structural validity of a DAG search plan, and output format adherence. The structured output (<think>, <search>, <result>, <answer>) enables explicit supervision over the reasoning-to-search pipeline. Achieves 70% reduction in context tokens and ~50% latency drop vs. multi-agent baselines on FinSearchBench-24 and SearchExpertBench-25.

## Key Contributions

- Single-LLM architecture replacing multi-agent search pipelines via structured output decomposition into four explicit components
- Multi-component GRPO reward: answer correctness + DAG structural validity + format adherence — distributes credit across planning and execution
- DAG-based search plan representation enabling multi-source parallel queries within one inference step
- Demonstrated efficiency gains (70% context token reduction, ~50% latency) without sacrificing accuracy

## Relevance

Directly advances the agentic RL + tool use thread: R-Search applies GRPO with structured reward decomposition to search as a tool, making it a clean example of how multi-component credit assignment can train single-LLM agents to plan and execute multi-step tool use. Connects to the step-credit cluster via its DAG-structured partial rewards and to the multi-turn agentic RL thread (State-Space Exploration, CoD) as a complementary approach to long-horizon search.

## My Thoughts

<!-- Add your own notes here -->
