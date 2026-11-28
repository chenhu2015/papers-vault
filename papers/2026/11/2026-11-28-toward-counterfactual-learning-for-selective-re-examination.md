---
title: "Toward Counterfactual Learning for Selective Re-Examination in Agentic Visual Search"
authors: ["Ao Chen", "Shengchao Chen", "Yan Luximon"]
date: 2026-10-31
arxiv_id: "2611.00848"
url: "https://arxiv.org/abs/2611.00848"
score: 0.82
topics: [agentic RL, VLM, vision-language, GRPO, LLM agent, multimodal]
status: unread
---

# Toward Counterfactual Learning for Selective Re-Examination in Agentic Visual Search

## Summary

CARE (Counterfactual Advantage for Re-Examination) addresses when a VLM agent should commit to an answer vs. request another look in high-resolution visual search. The authors first release ReSee, a 3,227-trajectory benchmark with explicit commit-or-re-examine decisions and counterfactual adjudication. CARE then uses paired continuations from the same search state under commit vs. re-examine verdicts; their cost-aware return difference provides a counterfactual credit signal assigned only to verdict tokens, giving decision-level credit assignment that GRPO lacks. CARE improves accuracy and decision selectivity over GRPO on six OOD benchmarks with fewer visual requests.

## Key Contributions

- ReSee benchmark: 3,227 visual-search trajectories with 8,827 explicit commit-or-re-examine decisions and counterfactual adjudication labels
- CARE: decision-level RL using paired commit/re-examine continuations from identical search states; cost-aware return difference as counterfactual credit
- Credit assigned only to verdict tokens (localized), not diffused across the whole trajectory
- Outperforms GRPO on six unseen OOD benchmarks with higher accuracy and fewer visual queries

## Relevance

Extends the agentic credit assignment thread (TACA, MSPO, ViCARD, TWICE) with a decision-level counterfactual credit method for VLM search agents. The search-continuation vs. commit framing is a natural extension of TWICE's twin-rollout counterfactual idea applied to VLM action choices, connecting the variance reduction thread (Search 2 today) directly to the agentic VLM space.

## My Thoughts

<!-- Add your own notes here -->
