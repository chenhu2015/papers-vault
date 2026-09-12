---
title: "Shared Prefixes, Better Credit: Adaptive Routing for Multi-Agent Reasoning"
authors: ["Yiqing Liu", "Zihao Wang", "Hantao Yao", "Wu Liu", "Yongdong Zhang"]
date: 2026-08-03
arxiv_id: "2608.02291v1"
url: "http://arxiv.org/abs/2608.02291v1"
score: 0.83
topics: [agentic RL, RL training, LLM agent, GRPO]
status: unread
---

# Shared Prefixes, Better Credit: Adaptive Routing for Multi-Agent Reasoning

## Summary

TreeCredit constructs shared-prefix collaboration trees for multi-agent reasoning (MAR) by expanding candidate operators from the same intermediate state, then estimates operator utility via state-matched downstream comparisons rather than query-level labels or trajectory-level returns. Each state-operator pair receives a correctness-prioritized suffix credit (terminal correctness + cumulative additional cost of its complete continuation), which trains a lightweight pairwise state router for dynamic operator selection at inference. On six reasoning benchmarks, TreeCredit modestly improves accuracy while substantially reducing inference cost over representative MAR methods.

## Key Contributions

- State-matched downstream comparison as operator utility estimator: expands multiple operators from the same intermediate state and compares downstream outcomes — avoids coarse trajectory-level attribution
- Correctness-prioritized suffix credit: terminal correctness takes priority; cumulative additional cost is secondary — the credit formula respects the hierarchical importance of correctness over efficiency
- Shared-prefix collaboration tree: a principled data structure for multi-agent credit computation, generalizing T-STAR's cognitive tree to the operator-routing setting
- Lightweight pairwise state router: converts structured credits into state-local operator preferences; models routing as a per-state classification problem rather than a global policy

## Relevance

TreeCredit connects T-STAR's cross-rollout cognitive tree structure (mentioned in Sep 09 digest) with the SRPO multi-agent action thread (Sep 10). Where SRPO addresses the optimization objective for multi-agent LLM pipelines (active-set cardinality normalization), TreeCredit addresses the credit assignment problem for routing decisions within those pipelines. Together they define a more complete picture of multi-agent LLM RL.

## My Thoughts

<!-- Add your own notes here -->
