---
title: "Socratic-MCTS: Test-Time Visual Reasoning by Asking the Right Questions"
authors: ["David Acuna", "Ximing Lu", "Jaehun Jung", "Hyunwoo Kim", "Amlan Kar", "Sanja Fidler", "Yejin Choi"]
date: 2025-06-10
arxiv_id: "2506.08927v1"
url: "https://arxiv.org/abs/2506.08927v1"
score: 0.73
topics: [vision language models, VLM, multimodal models, agentic RL]
status: unread
---

# Socratic-MCTS: Test-Time Visual Reasoning by Asking the Right Questions

## Summary

Socratic-MCTS shows that MCTS-inspired search over subquestion-subanswer pairs can elicit long-form reasoning from non-reasoning VLMs without any training or supervision, framing VLM inference as search over latent decisions in an output stream. Subquestions act as branching choices in an MCTS tree, helping models connect fragmented knowledge into extended reasoning traces. The approach yields 2% overall gains on MMMU-PRO (9% in Liberal Arts), positioning search as a training-free alternative to RL for unlocking VLM reasoning.

## Key Contributions

- Training-free MCTS-inspired search that injects subquestion-subanswer pairs into non-reasoning VLMs' output streams
- Reasoning framed as latent decision search, enabling long-form chain-of-thought without distillation or RL
- 2% overall MMMU-PRO improvement, with 9% gain in Liberal Arts — shows broad applicability beyond STEM
- Useful baseline/comparison point: shows how much of RL-trained reasoning gains MCTS search alone can recover

## Relevance

Provides a complementary angle to the RL-trained reasoning thread by asking how much MCTS search alone (no training) can achieve for VLMs — relevant context for evaluating the marginal value of RL training on top of search. Connects to VAGEN's world-model search and PRISM-MCTS from today's digest.

## My Thoughts

<!-- Add your own notes here -->
