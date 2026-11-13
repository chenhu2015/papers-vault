---
title: "Internalizing Curriculum Judgment for LLM Reinforcement Fine-Tuning"
authors: ["Han Zheng", "Yining Ma", "Karthick Gunasekaran", "Bharathan Balaji", "Zheng Du", "Shiv Vitaladevuni", "Cathy Wu"]
date: 2026-05-11
arxiv_id: "2605.11235v2"
url: "https://arxiv.org/abs/2605.11235"
score: 0.80
topics: [agentic RL, reinforcement learning, RLHF, agentic, LLM agent]
status: unread
---

# Internalizing Curriculum Judgment for LLM Reinforcement Fine-Tuning

## Summary

METIS (METacognitive Internalized Self-judgment) replaces external curriculum heuristics by treating within-prompt reward variance as a proxy for prompt informativeness, predicting it in-context from recent training outcomes. The policy jointly optimises standard RFT rewards and a self-judgment reward, closing the loop so it learns what to train on next. Achieves up to 2.1× training speedup with improved or matched performance across math, code, and agentic function-calling benchmarks.

## Key Contributions

- Within-prompt reward variance as a cheap, well-calibrated proxy for prompt informativeness
- In-context prediction of this metric from recent training outcomes (no auxiliary model)
- Joint optimisation of RFT reward + self-judgment reward for metacognitive curriculum control
- Eliminates external curriculum heuristics and auxiliary selectors; closed-loop and model-native

## Relevance

Connects the adaptive scaffolding cluster to the GRPO training dynamics thread: METIS is the curriculum-internalisation counterpart to papers like BRAT (training stability) and AutoScaffold (external teacher). It addresses the same root problem — which prompts to train on when — but via metacognitive self-awareness rather than teacher signals. The 2.1× speedup claim is the strongest data-efficiency result in this thread.

## My Thoughts

<!-- Add your own notes here -->
