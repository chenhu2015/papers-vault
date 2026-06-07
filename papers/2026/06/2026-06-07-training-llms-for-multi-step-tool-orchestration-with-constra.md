---
title: "Training LLMs for Multi-Step Tool Orchestration with Constrained Data Synthesis and Graduated Rewards"
authors: ["Cheng Jiayang", "Xin Liu", "Zhihan Zhang", "Haoyang Wen", "Zixuan Zhang", "Qingyu Yin", "Shiyang Li", "Priyanka Nigam", "Bing Yin", "Chao Zhang", "Yangqiu Song"]
date: 2026-06-07
arxiv_id: "2603.24709v2"
url: "http://arxiv.org/abs/2603.24709v2"
score: 0.79
topics: [tool use, agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# Training LLMs for Multi-Step Tool Orchestration with Constrained Data Synthesis and Graduated Rewards

## Summary

This paper addresses two core bottlenecks in RL training for multi-step tool orchestration: lack of environments supporting complex real-world API dependencies, and sparse binary rewards that miss partial correctness. It constructs a deterministic environment backed by a large real-API response cache for constrained multi-step trace synthesis, and introduces graduated rewards decomposing correctness into atomic validity (call-level correctness at increasing granularity) and orchestration consistency (sequencing with dependency respect). Cross-benchmark evaluation on BFCL v4 shows orchestration skills transfer to entirely different API ecosystems, confirming generalizable tool-use RL.

## Key Contributions

- Deterministic environment backed by real API response caches enabling constrained synthesis of valid multi-step API traces with controllable complexity
- Graduated reward decomposing into atomic validity (call-level correctness at increasing granularity) and orchestration consistency (correct sequencing with dependency respect)
- Substantial improvement on ComplexFuncBench turn accuracy; ablations confirm both reward components are essential
- Cross-ecosystem transfer on BFCL v4: learned orchestration skills generalise to agentic web search and memory management APIs

## Relevance

Extends the tool-use RL thread from June 1 (EchoRL/DARTS/AdaptR1) with a focus on the multi-step orchestration subproblem — specifically the reward design and training environment challenges that prior work glossed over. The graduated reward design resonates with DeepTool's Action-Centric Process Reward (May 31) but targets API dependency graphs rather than single-tool reasoning chains.

## My Thoughts

<!-- Add your own notes here -->
