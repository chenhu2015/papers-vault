---
title: "Process Advantage Signal Shaping: A Paradigm-Agnostic Middleware for Process-Supervised RL in LLM Reasoners"
authors: ["Chao Wang", "Hongtao Tian", "Tao Yang", "Yunsheng Shi", "Ting Yao", "Wenbo Ding"]
date: 2026-06-28
arxiv_id: "2606.29296v1"
url: "http://arxiv.org/abs/2606.29296v1"
score: 0.84
topics: [agentic RL, GRPO, reward model, RLHF]
status: unread
---

# Process Advantage Signal Shaping: A Paradigm-Agnostic Middleware for Process-Supervised RL in LLM Reasoners

## Summary

PASS identifies three structural pathologies when layering PRM signals on GRPO: channel contamination (mixed advantage streams before group standardization), resolution mismatch (step-level signal credited at wrong granularity), and cumulative trap (return-to-go summation causing length inflation or truncated exploration). The middleware addresses each with Advantage Fusion (independent per-stream standardization), Chunk-by-Value (value-homogeneous chunks for broadcast credit), and Divide-Length (average-value-density objective), delivering consistent pass@1 gains across both learned PRM and on-policy KL distillation paradigms.

## Key Contributions

- Formal characterization of three structural failure modes that emerge when any step-level process signal is naively layered on top of GRPO's group-standardized advantage
- Advantage Fusion: standardizes process, outcome, and format reward streams independently within each group before combining, eliminating cross-stream contamination
- Chunk-by-Value: derives value-homogeneous chunks from the process signal itself and broadcasts credit within chunks, matching credit granularity to logical decision units
- Divide-Length: converts the cumulative return-to-go objective into average-value-density, preventing length inflation and exploration truncation simultaneously

## Relevance

PASS directly addresses the architectural gap between the credit assignment hierarchy established by June digests (token-level AT-RL, segment-level DRE, sibling-step SCPO) and the process reward signal pipeline (ARES/ARBOR/EvoRubrics). The three pathologies it names explain why simply plugging a PRM into GRPO underperforms expectations — they are structural, not hyperparameter issues — making PASS the missing connector between the rubric-reward and credit-assignment threads.

## My Thoughts

<!-- Add your own notes here -->
