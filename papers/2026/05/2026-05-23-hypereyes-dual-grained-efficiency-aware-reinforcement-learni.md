---
title: "HyperEyes: Dual-Grained Efficiency-Aware Reinforcement Learning for Parallel Multimodal Search Agents"
authors: ["Guankai Li", "Jiabin Chen", "Yi Xu", "Xichen Zhang", "Yuan Lu"]
date: 2026-05-23
arxiv_id: "2605.07177v2"
url: "http://arxiv.org/abs/2605.07177v2"
score: 0.84
topics: [agentic RL, tool use, multimodal models, vision language models, RL training]
status: unread
---

# HyperEyes: Dual-Grained Efficiency-Aware Reinforcement Learning for Parallel Multimodal Search Agents

## Summary

HyperEyes trains a parallel multimodal search agent that dispatches multiple grounded queries concurrently rather than sequentially, using a two-level efficiency-aware RL framework. At the trajectory level, TRACE (Tool-use Reference-Adaptive Cost Efficiency) applies a tightening reward to suppress superfluous tool calls; at the token level, on-policy distillation injects dense corrective signals on failed rollouts to address credit-assignment sparsity. HyperEyes-30B outperforms the strongest open-source search agent by 9.9% accuracy with 5.3× fewer tool-call rounds on a new IMEB benchmark that jointly evaluates accuracy and inference cost.

## Key Contributions

- TRACE: trajectory-level efficiency reward with monotonically tightening reference during training, suppressing redundant tool calls without restricting genuine multi-hop search
- On-policy distillation from an external teacher on failed rollouts, providing dense token-level corrective signals to compensate sparse outcome rewards
- Parallel-Amenable Data Synthesis Pipeline for cold-start supervision covering multi-entity visual and multi-constraint textual queries
- IMEB benchmark (300 instances) jointly evaluating search accuracy and inference cost — the first benchmark to penalise tool-call overhead

## Relevance

Directly advances the agentic RL + tool-use thread, which has been a persistent focus (ActFocus, AEM, CM2, ParaVT, PAIR). The dual-grained efficiency reward is a novel contribution to the credit assignment problem in multi-turn tool-use agents, complementing May 22's ParaVT (which also tackled parallel tool dispatch in video RL).

## My Thoughts

<!-- Add your own notes here -->
