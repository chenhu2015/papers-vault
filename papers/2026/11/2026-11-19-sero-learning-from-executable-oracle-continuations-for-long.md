---
title: "SERO: Learning from Executable Oracle Continuations for Long-Horizon Agentic Reinforcement Learning"
authors: ["Dingyi Rong", "Yue Shi", "Chaofan Ma", "Zongrui Wang", "Jiezhang Cao"]
date: 2026-10-14
arxiv_id: "2610.19397"
url: "https://arxiv.org/abs/2610.19397"
score: 0.88
topics: [agentic RL, RL training, LLM agent, RLAIF]
status: unread
---

# SERO: Learning from Executable Oracle Continuations for Long-Horizon Agentic Reinforcement Learning

## Summary

SERO extends on-policy distillation by augmenting agentic RL with executable oracle continuations: rather than supervising only the oracle action at a policy-reached state, it lets a training-only oracle continue interacting with the real environment, making downstream observations and oracle actions themselves available for learning. Policy-reachability weighting scales oracle supervision at each step by the frozen behavior policy's compatibility with the preceding oracle branch, allowing deeper oracle guidance to become effective as the policy improves. Evaluated on ALFWorld and WebShop with Qwen2.5-1.5B/7B, full-continuation supervision substantially outperforms single-action oracle supervision.

## Key Contributions

- State-rooted executable rollout: oracle continues from a state actually reached by the current policy in the real environment (not a simulated state), making downstream oracle observations and actions available for training
- Policy-reachability weighting: each oracle step is weighted by the frozen behavior policy's compatibility with the preceding oracle actions, so deep oracle supervision becomes effective only as the policy grows compatible
- Oracle loss is optimized separately from the base RL estimator; no oracle is used at inference time
- Directly extends the multi-turn OPD literature (SAGE-OPD, Skill-SD, EMPO) by supervising the full executable continuation rather than a single oracle action

## Relevance

This paper is a direct extension of the multi-turn OPD/OPSD cluster that has been the primary focus of recent digests (SAGE-OPD, Skill-SD, ActFirst-OPD, MVPO, EMPO). SERO fills a gap in the cluster by using the oracle-controlled *future trajectory* as supervision rather than just oracle actions at a single state — a qualitatively different form of privileged information that connects to the executable oracle angle probed after EMPO.

## My Thoughts

<!-- Add your own notes here -->
