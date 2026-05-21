---
title: "MARCH: Multi-Agent Reinforced Self-Check for LLM Hallucination"
authors: ["Zhuo Li", "Yupeng Zhang", "Pengyu Cheng", "Jiajun Song", "Mengyu Zhou", "Hao Li", "Shujie Hu", "Yu Qin", "Erchao Zhao", "Xiaoxi Jiang", "Guanjun Jiang"]
date: 2026-03-25
arxiv_id: "2603.24579v1"
url: "http://arxiv.org/abs/2603.24579v1"
score: 0.82
topics: [LLM agent, agentic RL, RLAIF, reinforcement learning]
status: unread
---

# MARCH: Multi-Agent Reinforced Self-Check for LLM Hallucination

## Summary

MARCH addresses confirmation bias in RAG hallucination detection by orchestrating three specialized agents—Solver, Proposer, and Checker—where the Checker validates atomic propositions in isolation, deprived of the Solver's original output. This deliberate information asymmetry breaks self-confirmation bias, and multi-agent RL trains all three agents to co-evolve toward factual alignment. An 8B model with MARCH achieves performance competitive with powerful closed-source models on hallucination benchmarks.

## Key Contributions

- Deliberate information asymmetry design: Checker sees only propositions + evidence, never the Solver's original response
- Multi-agent RL (MARL) enables Solver/Proposer/Checker to co-evolve and specialize
- Proposition decomposition by Proposer into atomic claim-level verifiable units
- 8B model matches closed-source frontier performance on hallucination benchmarks

## Relevance

Connects the multi-agent RL thread (May 6, May 9 MARTI) with the credit assignment and hallucination reduction threads. The information asymmetry mechanism is a novel structural constraint on MARL that hasn't appeared in prior digests.

## My Thoughts

<!-- Add your own notes here -->
