---
title: "How Does Reasoning Flow? Tracing Attention-Induced Information Flow for Targeted RL in LLMs"
authors: ["Zhichen Dong", "Yang Li", "Yuhan Sun", "Weixun Wang", "Yijia Luo", "Zinian Peng", "Taiheng Ye", "Chao Yang", "Wenbo Su", "Yu Cheng", "Bo Zheng", "Junchi Yan"]
date: 2026-06-09
arxiv_id: "2606.10646v1"
url: "http://arxiv.org/abs/2606.10646v1"
score: 0.82
topics: [agentic RL, GRPO, reward model, RL training]
status: unread
---

# How Does Reasoning Flow? Tracing Attention-Induced Information Flow for Targeted RL in LLMs

## Summary

FlowTracer assigns token-level RL credit by tracing information flow on an attention-induced directed acyclic graph (DAG), where aggregated attention-weight edge capacities are reweighted to retain only influence that can reach the answer region under local flow conservation. Flow-throughput scores identify high-impact hubs and aggregation checkpoints mediating long-range dependencies, which are used as token-level reward shaping signals for RL with consistent gains across diverse reasoning benchmarks.

## Key Contributions

- Attention-induced DAG construction: tokens as nodes, aggregated attention weights as edge capacities, answer region as the target sink
- Flow conservation constraint: edges reweighted so intermediate tokens neither lose nor gain effective influence mass due to path length or irrelevant branches
- Flow-throughput scoring: identifies tokens that route information toward (or away from) correct answers as the high-impact RL credit targets
- Information-flow backbone visualization: exposes which tokens are structural hubs vs. filler, providing interpretable credit attribution distinct from heuristic saliency maps

## Relevance

FlowTracer extends the credit assignment hierarchy (token-level AT-RL Jun 14, segment DRE Jun 19, sibling-step SCPO Jun 30, cross-trajectory GraphGPO Jun 30) with a structurally different approach: instead of rollout state graphs (GraphGPO) or n-gram contrast (STRIDE), it uses the model's own attention patterns to define credit, making it complementary to and compatible with any of the existing methods. It is also the closest mechanistic correlate of the ReasonMaxxer/SWITCH finding (RL concentrates at high-entropy positions) — FlowTracer shows that those positions are precisely the attention hubs where information flow converges.

## My Thoughts

<!-- Add your own notes here -->
