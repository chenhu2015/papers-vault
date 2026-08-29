---
title: "SAT: Sequential Agent Tuning for Coordinator Free Plug and Play Multi-LLM Training with Monotonic Improvement Guarantees"
authors: ["Yi Xie", "Yangyang Xu", "Yi Fan", "Bo Liu"]
date: 2026-04-17
arxiv_id: "2605.05216"
url: "https://arxiv.org/abs/2605.05216"
score: 0.80
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# SAT: Sequential Agent Tuning for Coordinator Free Plug and Play Multi-LLM Training with Monotonic Improvement Guarantees

## Summary

SAT trains teams of LLMs via block-coordinate updates — optimizing one agent at a time — with a sequence-aware on-policy advantage estimator and per-agent KL trust regions, requiring no central coordinator. The framework provides two theoretical guarantees: monotonic team improvement per update round, and plug-and-play invariance meaning any agent can be upgraded to a stronger model without retraining the rest while provably not degrading the performance bound. Empirically, a 3×4B team (12B total parameters) surpasses Qwen3-32B on AIME24/25 by 3.9%, and swapping two 4B agents for 8B models boosts the composite score by another 10.4% with no retraining.

## Key Contributions

- Block-coordinate multi-LLM training: one agent updated at a time, decoupled from others via per-agent KL trust regions that isolate occupancy drift
- Sequence-aware on-policy advantage estimator that conditions on the evolving team policy — avoids stale advantage estimates during sequential updates
- Monotonic improvement guarantee per update round (not just in expectation)
- Plug-and-play invariance: swapping agent k with a stronger model provably improves the team performance bound without requiring retraining of other agents

## Relevance

Opens a new angle in the vault: training multi-LLM systems as a coordinated team rather than training a single model. The OrchestraBench paper (Aug 17) studied failure modes of multi-agent orchestration; SAT is the first vault paper addressing training-time coordination for multi-LLM teams. The plug-and-play invariance guarantee is structurally analogous to SKILL0's curriculum-withdrawal invariance (Aug 26) but operates at the model-replacement level rather than the skill-internalization level.

## My Thoughts

<!-- Add your own notes here -->
