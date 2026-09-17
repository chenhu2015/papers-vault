---
title: "HiMPO: Hindsight-Informed Memory Policy Optimization for Less-Entangled Credit in Long-Horizon Agents"
authors: ["Jiangze Yan", "Yi Shen", "Wenjing Zhang", "Jieyun Huang", "Zhaoxiang Liu", "Ning Wang", "Kai Wang", "Shiguo Lian"]
date: 2026-06-15
arxiv_id: "2606.16285v2"
url: "http://arxiv.org/abs/2606.16285v2"
score: 0.88
topics: [agentic RL, RL training, LLM agent, reward model, RLHF]
status: unread
---

# HiMPO: Hindsight-Informed Memory Policy Optimization for Less-Entangled Credit in Long-Horizon Agents

## Summary

HiMPO addresses the distinct credit assignment problem for memory-writing actions in long-horizon agents: final rewards conflate memory quality with execution errors and environmental noise. It estimates local utility of a memory update by comparing task-relevant information recoverable from the pre- and post-write memories under the same state, then uses hindsight relevance as a bounded retrospective filter that attenuates memory credit when local utility is unsupported by the outcome. Memory-specific advantages are applied only to memory tokens, reducing blame leakage from tool failures while transferring effectively across backbone models.

## Key Contributions

- Formulates memory-writing credit assignment as distinct from general RL credit: memory writes have a unique entanglement problem where downstream failures (tool errors, env noise) contaminate the memory signal
- Local utility estimation via comparative information recovery: measures what task-relevant information is recoverable from memory before and after a write, under the same pre-write state
- Hindsight relevance as a bounded retrospective filter: attenuates memory credit when local utility is not corroborated by the target outcome — filtering, not eliminating
- Memory-specific advantage application: applies the resulting signal only to memory tokens while trajectory-level rewards continue to optimise the rest of agent behaviour

## Relevance

Adds a sixth method to the hindsight-informed credit redistribution cluster (TRIAL, T-STAR, TASPO, CRISP, VICT) but with a distinct focus: memory-action credit rather than general step credit. The attribute-before-memorize principle mirrors VICT's verifier-trace attribution but applies to self-generated memory rather than external verifier outputs. The unified treatment gap noted on Sep 12 (and still open) now has a sixth entry point.

## My Thoughts

<!-- Add your own notes here -->
