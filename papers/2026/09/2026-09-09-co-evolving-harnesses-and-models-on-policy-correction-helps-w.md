---
title: "Co-Evolving Harnesses and Models: On-Policy Correction Helps Weaker Models Catch Up Where Imitation Fails"
authors: ["Zhou Yu", "Bin Bi", "Shiva Kumar Pentyala", "Shubham Mehrotra", "Sougata Chaudhuri", "Shilpa Bhagavath", "Zeyuan Chen", "Ran Xu", "Phil Mui", "James Zhu", "Sitaram Asur"]
date: 2026-09-09
arxiv_id: "2609.09134v1"
url: "http://arxiv.org/abs/2609.09134v1"
score: 0.75
topics: [agentic RL, LLM agent, RL training, tool use]
status: unread
---

# Co-Evolving Harnesses and Models: On-Policy Correction Helps Weaker Models Catch Up Where Imitation Fails

## Summary

This paper shows that imitation of a stronger expert on an evolved harness backfires for weaker models across 7 enterprise agent tasks: the weaker model adopts the expert's planning strategy without the competence to execute it, disrupting model-harness fit. The solution is an on-policy expert-correction pipeline (automated by a meta-level MLE agent) that localizes the failing turn in the weaker model's own rollout and rewrites only that turn, preserving the model's native planning style. The compatibility-preserving recipe combines harness evolution and model adaptation without performance regression.

## Key Contributions

- Identifies a source of contention between harness evolution and imitation fine-tuning: imitation disrupts model-harness fit when the weaker model adopts the expert's planning style without the competence to execute it
- On-policy expert-correction pipeline: a meta-level MLE agent localizes the failing turn in the weaker model's own rollout and asks the expert to rewrite only that turn
- Preserves the model's native planning style while incorporating expert knowledge at failure points
- Tested across 7 enterprise agent tasks on Qwen3-Coder and Gemma 4; imitation degrades performance 4-30 points, on-policy correction recovers it

## Relevance

Connects to the agentic RL harness thread (EvoHarness-RL, Aug 2026) and the multi-turn credit assignment thread: the on-policy correction approach is structurally a turn-level credit signal — the meta-MLE agent assigns negative credit to the failing turn and solicits targeted expert correction at that turn only, similar to per-turn advantage redistribution in TRIAL/RTPO but using expert rewriting rather than RL reward signals.

## My Thoughts

<!-- Add your own notes here -->
