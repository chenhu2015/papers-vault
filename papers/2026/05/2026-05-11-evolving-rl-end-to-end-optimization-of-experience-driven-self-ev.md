---
title: "Evolving-RL: End-to-End Optimization of Experience-Driven Self-Evolving Capability within Agents"
authors: ["Zhiyuan Fan", "Wenwei Jin", "Feng Zhang", "Bin Li", "Yihong Dong", "Yao Hu", "Jiawei Li"]
date: 2026-05-11
arxiv_id: "2605.10663v1"
url: "http://arxiv.org/abs/2605.10663v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent, GRPO, tool use]
status: unread
---

# Evolving-RL: End-to-End Optimization of Experience-Driven Self-Evolving Capability within Agents

## Summary

Evolving-RL jointly trains experience extraction (what patterns to distill from past interactions) and experience utilization (how to apply them in new tasks) by centering the learning process on extraction evaluation, using two supervisory signals from evaluation to optimize the extractor and solver in coordinated co-evolution. On ALFWorld unseen tasks, Evolving-RL achieves 98.7% relative improvement over the GRPO baseline; on Mind2Web, 35.8% improvement. Gains persist even without test-time experience accumulation, confirming successful parameter-level internalization rather than retrieval-dependent performance.

## Key Contributions

- Identifies that prior work optimizes experience utilization stage alone, neglecting extraction capability
- Jointly optimizes extractor and solver via supervisory signals derived from extraction evaluation
- Co-evolution: separate optimization targets for extraction and solving, coupled via shared evaluation
- ALFWorld unseen: 98.7% relative improvement over GRPO; Mind2Web: 35.8%; gains hold at zero test-time experience

## Relevance

Evolving-RL predates EDGE (Aug 22) and addresses the same parameter-internalization goal from a different angle: where EDGE uses reverse-KL distillation and positive marginal gains, Evolving-RL uses end-to-end supervised co-evolution of the extractor and solver. The comparison reveals two design axes for experience internalization: (1) whether to separate extraction from utilization (Evolving-RL: yes; EDGE: unified), and (2) whether internalization happens via KL distillation (EDGE) or supervised co-evolution (Evolving-RL). Neither paper cites the other, suggesting independent development of the "internalize experiences into parameters" idea.

## My Thoughts

<!-- Add your own notes here -->
