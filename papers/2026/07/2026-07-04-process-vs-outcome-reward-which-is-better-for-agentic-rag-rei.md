---
title: "Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning"
authors: ["Wenlin Zhang", "Xiangyang Li", "Kuicai Dong", "Yichao Wang", "Pengyue Jia", "Xiaopeng Li", "Yingyi Zhang", "Derong Xu", "Zhaocheng Du", "Huifeng Guo", "Ruiming Tang", "Xiangyu Zhao"]
date: 2026-07-04
arxiv_id: "2505.14069"
url: "https://arxiv.org/abs/2505.14069"
score: 0.75
topics: [agentic RL, RL training, LLM agent, reward model, tool use]
status: unread
---

# Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning

## Summary

ReasonRAG proposes process-supervised RL for agentic RAG, constructing high-quality process rewards for three sub-tasks — query generation, evidence extraction, and answer generation — to overcome the low exploration efficiency, gradient conflict, and sparse signals of outcome-based RAG RL (Search-R1). The automatically constructed RAG-ProGuide dataset provides process-level rewards without human labels, enabling fine-grained policy optimization where the model autonomously invokes search, generates queries, extracts evidence, and produces answers. ReasonRAG achieves superior performance on five benchmarks with only 5k training instances versus Search-R1's 90k, an 18× data efficiency gain.

## Key Contributions

- Process rewards for three distinct agentic RAG sub-task roles: query generation quality, evidence extraction relevance, and answer generation accuracy
- Automatic RAG-ProGuide dataset construction from existing trajectories without human labels, providing the three process-level reward signals for RL training
- Fine-grained process-supervised RL enabling the agent to autonomously invoke search, generate queries, extract evidence, and produce answers end-to-end
- 18× data efficiency gain over outcome-only Search-R1 (5k vs. 90k training instances) demonstrating the practical value of process supervision for agentic RAG

## Relevance

ReasonRAG applies TRIAGE's insight (Jul 2) — that role-typed credit for distinct action types reduces both regression-in-success and exploration-in-failure — to the RAG pipeline domain, where the "roles" are query/evidence/answer rather than navigation action types. The 18× data efficiency gain directly quantifies the practical cost of the sparse reward problem that PASS (Jul 1) diagnosed at the algorithm level; where PASS proposed middleware fixes for any PRM-GRPO pairing, ReasonRAG demonstrates that domain-specific process reward design (RAG sub-task roles) achieves the same improvement with simpler machinery.

## My Thoughts

<!-- Add your own notes here -->
