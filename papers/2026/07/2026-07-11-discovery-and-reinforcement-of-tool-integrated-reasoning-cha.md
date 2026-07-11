---
title: "Discovery and Reinforcement of Tool-Integrated Reasoning Chains via Rollout Trees"
authors: ["Kun Li", "Zenan Xu", "Junan Li", "Zengrui Jin", "Jinghao Deng", "Zexuan Qiu", "Bo Zhou"]
date: 2026-07-11
arxiv_id: "2601.08274"
url: "https://arxiv.org/abs/2601.08274"
score: 0.83
topics: [agentic RL, tool use, RL training, LLM agent]
status: unread
---

# Discovery and Reinforcement of Tool-Integrated Reasoning Chains via Rollout Trees

## Summary

DART constructs dynamic rollout trees during RL training to discover valid tool-use opportunities within long chain-of-thought reasoning, branching at promising positions to explore diverse tool-integrated trajectories without human annotation. A tree-based process advantage estimation then identifies and credits specific sub-trajectories where tool invocation positively contributed to the solution, reinforcing those behaviors via policy gradient. Significantly outperforms existing methods on AIME and GPQA-Diamond benchmarks.

## Key Contributions

- Dynamic rollout tree construction during training: branches at promising positions in the CoT to explore whether inserting a tool call at that point improves outcomes
- Tree-based process advantage estimation: credits sub-trajectories where tool invocation was causally beneficial, rather than assigning credit at the sequence level
- Annotation-free: discovers tool-use opportunities from RL signal alone, without step-level human labels or supervised tool-call demonstrations
- Strong results on hard reasoning benchmarks (AIME, GPQA-Diamond) that require combining computation with reasoning

## Relevance

DART is the structural complement to ARTIST (Jul 09: outcome-based RL for multi-turn tool integration without step supervision). Where ARTIST learns *when and which tool to invoke* from trajectory-level outcome rewards, DART learns *where to insert tool calls within a long CoT* via tree branching. Together they cover two complementary aspects of tool-integrated reasoning RL: pipeline-level tool selection (ARTIST) and reasoning-step-level tool insertion (DART). DART's tree-based process advantage also extends the credit assignment thread: it is the tool-use analog of GRPO-λ's eligibility traces, providing structured intra-sequence credit rather than uniform sequence-level credit.

## My Thoughts

<!-- Add your own notes here -->
