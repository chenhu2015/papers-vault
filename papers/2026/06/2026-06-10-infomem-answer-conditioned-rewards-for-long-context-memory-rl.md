---
title: "InfoMem: Training Long-Context Memory Agents with Answer-Conditioned Information Gain"
authors: ["Tiancheng Han", "Yong Li", "Wuzhou Yu", "Qiaosheng Zhang", "Wenqi Shao"]
date: 2026-06-02
arxiv_id: "2606.03329v1"
url: "http://arxiv.org/abs/2606.03329v1"
score: 0.80
topics: [agentic RL, RL training, GRPO, LLM agent, reward model]
status: unread
---

# InfoMem: Training Long-Context Memory Agents with Answer-Conditioned Information Gain

## Summary

InfoMem proposes rewarding chunk-wise memory agents by measuring how much the agent's accumulated final memory increases the model's per-token log-likelihood of the ground-truth answer, directly evaluating memory utility rather than proxying it through lexical overlap with intermediate steps. The reward is restricted to successful trajectories and normalised before composition for stable GRPO training. InfoMem outperforms comparable RL-based memory agent baselines under the same training budget on long-document QA tasks.

## Key Contributions

- Answer-conditioned information-gain reward: measures whether final memory supports the correct answer via log-likelihood increase
- Restricts the reward signal to successful trajectories to avoid rewarding unhelpful memory on failures
- Normalisation before reward composition for stable GRPO optimisation
- Analysis demonstrating that effective memory rewards should be answer-conditioned (not query-conditioned) and applied selectively to successes

## Relevance

Complements MemoPilot (today) from the reward-design perspective: MemoPilot designs the training objective for the memory-update policy module; InfoMem designs the reward signal for chunk-wise reading agents. Both are in the memory-augmented agentic RL cluster, a new thread opened by today's retrieval/memory search. Also connects to RREDCoT (Jun 8, segment-level reward redistribution for CoT) as another instance of intermediate-step credit assignment without expensive Monte Carlo estimation.

## My Thoughts

<!-- Add your own notes here -->
