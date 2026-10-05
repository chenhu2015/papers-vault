---
title: "Making Every Tool Call Count: Necessary Tool-Evidence Path Rewards for Agentic Vision-Language Models"
authors: ["Xingming Long", "Yu Liu", "Zhiwei Yang", "Hanqi Feng", "Shaojie Zhang", "Barnabas Poczos", "Chao Jiang", "Zhenbo Luo", "Lei Jiang", "Pei Fu"]
date: 2026-10-05
arxiv_id: "2609.03493v1"
url: "https://arxiv.org/abs/2609.03493"
score: 0.83
topics: [agentic RL, vision language models, VLM, tool use, LLM agent, reward model]
status: unread
---

# Making Every Tool Call Count: Necessary Tool-Evidence Path Rewards for Agentic Vision-Language Models (NTEP-R)

## Summary

NTEP-R introduces the Necessary Tool-Evidence Path (NTEP) annotation scheme that explicitly specifies the essential external evidence and required tool calls for each query, then trains agentic VLMs with rewards that verify both pre-call intent alignment with a necessary evidence goal and post-call observation alignment with the necessary evidence. A non-repeated-goal regularizer penalizes redundant calls that revisit already-satisfied evidence goals. The 8B instantiation (NTEP-8B) significantly improves search-oriented accuracy and tool-use efficiency across seven image-grounded benchmarks.

## Key Contributions

- NTEP annotation scheme: specifies necessary external evidence and the tool calls required to gather it, creating ground truth for tool-use step credit
- Reward signal decomposes into: pre-call intent alignment (does the model intend to gather necessary evidence?) + post-call observation alignment (did the tool call actually retrieve the necessary evidence?)
- Non-repeated-goal regularizer prevents redundant tool calls that revisit already-satisfied NTEP goals
- NTEP-8B improves both search-oriented accuracy and tool-use efficiency across seven image-grounded benchmarks in a three-tool framework (image crop, image search, text search)

## Relevance

NTEP-R introduces tool-call step credit for agentic VLMs — a new sub-thread not yet represented in the vault. Where the step-credit cluster (ASCT through AdaStep/DepGPO) addresses *action-level* credit in text agents, NTEP-R addresses *tool-call-level* credit in multimodal agents: the credit signal is defined by whether the tool call was necessary and whether it retrieved the right evidence. This is the direct agentic VLM counterpart to BRIDGE's retriever+LLM bilevel credit, but at the per-call level rather than the parameter-level.

## My Thoughts

<!-- Add your own notes here -->
