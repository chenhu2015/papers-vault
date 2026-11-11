---
title: "Understanding Evolution Strategies for LLM Reasoning: Broader Reasoning Coverage than GRPO"
authors: ["Yunpeng Ba", "Zhi Zheng", "Yue Xie", "Jiaqing Li", "Xialiang Tong", "Tao Zhong", "Mingxuan Yuan", "Zhichao Lu", "Xuyang Wu", "Zhenkun Wang"]
date: 2026-11-11
arxiv_id: "2608.27351v2"
url: "http://arxiv.org/abs/2608.27351v2"
score: 0.78
topics: [reinforcement learning, RL training, GRPO]
status: unread
---

# Understanding Evolution Strategies for LLM Reasoning: Broader Reasoning Coverage than GRPO

## Summary

This paper shows that Evolution Strategies (ES) produce broader reasoning coverage (higher Pass@K) than GRPO because verifier-projected Jensen-Shannon diversity across the ES population improves solution diversity while GRPO exhibits entropy collapse. ES updates exhibit functional sparsity — large parameter drift with capability changes concentrated in a sparse subset of larger-magnitude updates. A sequential GRPO-ES training strategy combines GRPO's Pass@1 strength with ES's Pass@K coverage gains.

## Key Contributions

- Establishes ES vs GRPO comparison: ES improves Pass@1 while sustaining higher Pass@K; GRPO improves Pass@1 but collapses entropy / Pass@K
- Verifier-projected Jensen-Shannon diversity across the ES population is theoretically linked to Pass@K performance
- Functional sparsity finding: large whole-model parameter drift in ES does not imply widespread functional change — capability gains are sparse and don't cause catastrophic forgetting
- Sequential GRPO-ES strategy: GRPO first (Pass@1 gains), then ES (diversity recovery); hyperparameter finding: smaller population needed for larger LLMs

## Relevance

Connects to the GRPO training dynamics thread (entropy collapse dimension — Nov 7 Controlling Sharpening, Collective Dynamics) and the RLVR exploration cluster (TGRL, EDEN, PSRA today). ES's JS diversity signal is thematically adjacent to TGRL's JS divergence credit; this paper provides a full theoretical and empirical framing for why diversity matters for coverage. The functional sparsity finding is also relevant to the parameter-efficient RL cluster (T-Router, GrowRL).

## My Thoughts

<!-- Add your own notes here -->
