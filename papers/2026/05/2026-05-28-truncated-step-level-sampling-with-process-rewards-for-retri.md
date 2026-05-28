---
title: "Truncated Step-Level Sampling with Process Rewards for Retrieval-Augmented Reasoning"
authors: ["Chris Samarinas", "Haw-Shiuan Chang", "Hamed Zamani"]
date: 2026-02-26
arxiv_id: "2602.23440v3"
url: "https://arxiv.org/abs/2602.23440"
score: 0.82
topics: [agentic RL, tool use, GRPO, reward model, LLM agent]
status: unread
---

# Truncated Step-Level Sampling with Process Rewards for Retrieval-Augmented Reasoning

## Summary

SLATE (Step-Level Advantage estimation for Truncated Exploration) addresses credit assignment in retrieval-augmented RL via two ideas: truncated step-level sampling generates k continuations from a shared prefix, proven to reduce advantage-estimate variance by up to a factor of T over full-trajectory sampling, providing the first formal variance guarantee for step-level RL in retrieval reasoning. Dense decomposed process rewards separately evaluate reasoning quality, query quality, and answer correctness via an LLM judge. SLATE improves 7.0% over Search-R1 on 7B and 30.7% on 3B across 7 QA benchmarks.

## Key Contributions

- Truncated step-level sampling: k completions from shared prefix isolates variance to one decision point at a time
- First formal proof that step-level sampling reduces advantage variance by factor up to T vs. full-trajectory sampling
- Dense decomposed process rewards on ternary scale: reasoning quality, query quality, answer correctness
- 30.7% relative improvement over Search-R1 on 3B model, confirming gains compound at smaller scale

## Relevance

SLATE's formal variance-reduction theorem complements the empirical credit-assignment work seen this week (IG-Search, PiCA, TIPS, EvalAct) and brings the theoretical rigor from the May 27 token-credit papers (Covariance-Aware GRPO, MaR) to the retrieval-augmented RL domain.

## My Thoughts

<!-- Add your own notes here -->
