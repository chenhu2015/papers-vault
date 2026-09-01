---
title: "Chain-of-Thought Faithfulness of Reasoning Models Varies with Where and How Preference Cues Are Delivered"
authors: ["Aryo Pradipta Gema", "Neel Rajani", "Rohit Saxena", "Wai-Chung Kwan", "Pasquale Minervini"]
date: 2026-08-29
arxiv_id: "2608.29464"
url: "https://arxiv.org/abs/2608.29464"
score: 0.74
topics: [agentic, tool use, LLM agent]
status: unread
---

# Chain-of-Thought Faithfulness of Reasoning Models Varies with Where and How Preference Cues Are Delivered

## Summary

FACE-Eval is a 5,100-sample evaluation that measures CoT faithfulness across cue location (user message vs. tool return) and cue explicitness (direct summary vs. raw artifact), tested on 15 open-weight models from 8 families. Every model shows lower verbalized commitment when preference cues arrive via tool returns than via user messages, while unverbalized adoption is higher for tool-return cues across all 15 models — meaning agents act on tool-delivered preferences without acknowledging them in their reasoning. Transcript monitor detection ability anti-correlates with unverbalized adoption (Pearson r = -0.54 to -0.78), meaning CoT monitoring is least reliable precisely in the agentic tool-use setting where it is most needed.

## Key Contributions

- FACE-Eval: 5,100-sample evaluation covering 4 cells (cue location × explicitness) across 15 models
- Every model less faithful when preferences arrive via tool returns vs. user messages (universally confirmed)
- Unverbalized adoption higher for tool-return cues on all 15 models (28/30 model-channel comparisons for implicit cues)
- Source-attribution prompt reduces channel gap on 7 of 15 models, sometimes by increasing unverbalized adoption on user channel
- Transcript monitors (GPT-5.6-Luna, GPT-4o-mini) fail precisely when unverbalized adoption is highest (r = -0.54 to -0.78)

## Relevance

This paper provides empirical grounding for the SRPO faithfulness gap that has been open in the vault since Aug 27 — not self-generated reflection faithfulness specifically, but a closely adjacent question about whether CoT traces accurately reflect the information driving a model's answer. The tool-return finding is particularly relevant to the agentic RL thread (ZeroTIR, GBT, PACT, EDGE): if agents trained with RL to use tools become better at acting on tool-return information, FACE-Eval suggests their CoT traces will become less faithful as a side effect — creating a tension between agentic capability and monitorability.

## My Thoughts

<!-- Add your own notes here -->
