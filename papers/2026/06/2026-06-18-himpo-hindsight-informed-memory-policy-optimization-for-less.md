---
title: "HiMPO: Hindsight-Informed Memory Policy Optimization for Less-Entangled Credit in Long-Horizon Agents"
authors: ["Jiangze Yan", "Yi Shen", "Wenjing Zhang", "Jieyun Huang", "Zhaoxiang Liu", "Ning Wang", "Kai Wang", "Shiguo Lian"]
date: 2026-06-18
arxiv_id: "2606.16285"
url: "https://arxiv.org/abs/2606.16285"
score: 0.80
topics: [agentic RL, LLM agent, tool use, RL training]
status: unread
---

# HiMPO: Hindsight-Informed Memory Policy Optimization for Less-Entangled Credit in Long-Horizon Agents

## Summary

Long-horizon agents face a credit assignment problem specific to memory-writing actions: downstream tool failures and reasoning errors causally entangle credit with memory updates that may be independently correct, causing agents to discard useful evidence or preserve irrelevant information. HiMPO estimates the local utility of each memory update by comparing task-relevant information recoverable from pre/post-write memory states, then applies hindsight relevance as a bounded retrospective filter that attenuates memory credit when local utility is unsupported by the final outcome, applying this memory-specific advantage only to memory tokens while standard trajectory-level rewards optimize the rest.

## Key Contributions

- Identifies "causally entangled credit" as the core failure mode for memory optimization in long-horizon RL: memory updates penalized for downstream tool/reasoning failures they didn't cause
- Local utility estimation: compares task-relevant information recoverable from previous vs. updated memory under the same pre-write state
- Hindsight relevance filter: bounded retrospective signal that attenuates memory credit when local utility isn't supported by outcome, preventing blame leakage from tool errors
- Memory-specific advantage applied only to memory tokens, leaving trajectory-level RL intact for other action types

## Relevance

Extends the credit assignment thread (HiPER Jun 14, AT-RL Jun 14, R3L Jun 14, RReDCoT Jun 8) into the memory dimension — those papers addressed credit for reasoning tokens; HiMPO addresses credit for the distinct class of memory-writing tokens, which have a causally decoupled relationship to outcome that standard trajectory rewards fail to capture. Complements MemoPilot (Jun 10) and InfoMem (Jun 10) which addressed what to memorize, not how to assign credit to memory writes.

## My Thoughts

<!-- Add your own notes here -->
