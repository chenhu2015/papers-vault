---
title: "Connect the Dots: Training LLMs for Long-Lifecycle Agents with Cross-Domain Generalization Via Reinforcement Learning"
authors: ["Yanxi Chen", "Weijie Shi", "Boyi Hu", "Zeyue Zhang", "Zhiwei Wang", "Yuexiang Xie", "Yaliang Li", "Bolin Ding", "Jingren Zhou"]
date: 2026-06-18
arxiv_id: "2606.20002"
url: "https://arxiv.org/abs/2606.20002"
score: 0.77
topics: [agentic RL, GRPO, LLM agent, RL training]
status: unread
---

# Connect the Dots: Training LLMs for Long-Lifecycle Agents with Cross-Domain Generalization Via Reinforcement Learning

## Summary

Presents the Connect the Dots (CoD) framework for training LLMs as long-lifecycle agents that continuously explore, learn, and self-update context across task sequences using GRPO-style RL with fine-grained credit assignment over long interleaved rollout sequences. Unlike standard task-by-task RL, CoD trains the meta-capability of integrating experience from earlier tasks to perform better on later tasks. Demonstrates cross-domain generalization with Qwen3-8B and Qwen3.6-27B, showing the elicited meta-capability transfers out-of-distribution and from CoD to Ralph-loop settings.

## Key Contributions

- CoD framework: end-to-end RL training with long rollouts interleaving solve-task and update-context episodes
- GRPO-style RL with fine-grained credit assignment for long-horizon sequences
- Tasks and environments targeting the meta-capability of continuous environment learning (rather than domain-specific capabilities)
- Out-of-distribution cross-domain generalization and transfer from CoD to Ralph-loop settings

## Relevance

Extends the agentic RL thread into the "long-lifecycle" regime — agents that don't just solve individual tasks but continuously improve over a sequence of deployments. Complements the multi-turn exploration paper (Oct 20) and StructRL (Oct 18) by addressing how to train for continuous self-improvement rather than just reducing invalid actions or structuring rewards. The fine-grained credit assignment within GRPO over long interleaved rollouts is a novel structural contribution to the step-credit cluster.

## My Thoughts

<!-- Add your own notes here -->
