---
title: "Cycle-Consistent Search: Question Reconstructability as a Proxy Reward for Search Agent Training"
authors: ["Sohyun An", "Shuibenyang Yuan", "Hayeon Lee", "Cho-Jui Hsieh", "Alexander Min"]
date: 2026-09-30
arxiv_id: "2604.12967v1"
url: "http://arxiv.org/abs/2604.12967v1"
score: 0.72
topics: [agentic RL, LLM agent, RLAIF, reward model]
status: unread
---

# Cycle-Consistent Search: Question Reconstructability as a Proxy Reward for Search Agent Training

## Summary

Cycle-Consistent Search (CCS) trains search agents without gold-label supervision by using question reconstructability as a reward signal: an optimal search trajectory encodes enough information to recover the original question, so a high reconstruction score proxies trajectory quality. Information bottlenecks (exclude final response, NER masking of queries) prevent surface-level leakage and force the reward to reflect informational adequacy. CCS achieves performance comparable to supervised baselines while requiring no ground-truth answers.

## Key Contributions

- **Cycle-consistency hypothesis**: optimal search trajectory is a lossless encoding of question intent — reconstruction accuracy proxies trajectory adequacy without requiring a labelled answer
- **Information bottleneck design**: two bottlenecks prevent leakage — final response exclusion and NER masking of query tokens — forcing reward signal to reflect structural retrieval quality
- **Gold-supervision-free training**: achieves comparable performance to supervised RL baselines and outperforms prior unsupervised approaches on question-answering benchmarks
- **Scalable paradigm**: directly applicable to domains where gold answers are unavailable or expensive to collect

## Relevance

CCS offers a concrete response to the "Credit Without Ground Truth" challenge: if ground-truth labels are unavailable, cycle-consistency provides a principled unsupervised reward signal grounded in information theory rather than proxy judgements (LLM-judge, logprob ratio). This complements the counterfactual credit thread (ASCT, CRR, TEMPO) which assumes verifiable rewards exist; CCS applies when they do not.

## My Thoughts

<!-- Add your own notes here -->
