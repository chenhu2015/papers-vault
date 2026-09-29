---
title: "ASCT: Attentive Search over Counterfactual Trees for Credit Assignment in Agentic Reinforcement Learning"
authors: ["Yang Li", "Jinhan Yang", "hai liu", "Di Wan", "Xiyu Chen", "Zongsi Xu", "Tuo Zhou", "Sheng Zhong", "Sergey Volkov", "Ye Luo", "Hao Sun"]
date: 2026-09-29
arxiv_id: "2609.35215v1"
url: "https://arxiv.org/abs/2609.35215"
score: 0.92
topics: [agentic RL, RL training, LLM agent, agentic, reward model]
status: unread
---

# ASCT: Attentive Search over Counterfactual Trees for Credit Assignment in Agentic Reinforcement Learning

## Summary

ASCT addresses the terminal-only credit problem in agentic RL by constructing a counterfactual action tree at training time: from each actor-visited state, an auxiliary tree evaluates alternative legal actions from the same recoverable prefix, producing an action-value table that replaces the PPO advantage. The actor deploys alone at inference while the tree is used only during training, avoiding counterfactual compute at test time. On HotpotQA RAG, ASCT-AgentUCT reaches 0.6187 utility versus 0.5939 for VinePPO, using 50.3% fewer auxiliary tokens.

## Key Contributions

- Auxiliary counterfactual tree at training time: from actor-visited states, enumerate alternative actions and roll them forward to estimate local action-value contrasts
- Three tree instantiations: Uniform search, UCT (upper confidence bound), and AgentUCT (cost-aware variant that weights search budget by action cost)
- Action-value table derived from the tree replaces the standard PPO advantage, supplying step-level credit without human process labels
- Actor deploys alone at inference — zero counterfactual overhead at test time; search is training-only

## Relevance

Directly addresses the confound raised by "Credit Without Ground Truth": rather than relying on logprob ratios or LLM-judge scores (both flagged as fluency-confounded), ASCT computes credit via actual rollout contrasts from the same recoverable state, grounding advantage in executed outcomes. This is the strongest response to the step-credit audit challenge yet seen. Complements CRR (same digest) which uses forkable environments for similar purposes in SWE contexts.

## My Thoughts

<!-- Add your own notes here -->
