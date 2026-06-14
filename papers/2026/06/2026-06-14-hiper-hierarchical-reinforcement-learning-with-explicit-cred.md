---
title: "HiPER: Hierarchical Reinforcement Learning with Explicit Credit Assignment for Large Language Model Agents"
authors: ["Jiangweizhi Peng", "Yuanxin Liu", "Ruida Zhou", "Charles Fleming", "Zhaoran Wang", "Alfredo Garcia", "Mingyi Hong"]
date: 2026-06-14
arxiv_id: "2602.16165v2"
url: "http://arxiv.org/abs/2602.16165v2"
score: 0.82
topics: [agentic RL, RL training, LLM agent, reinforcement learning]
status: unread
---

# HiPER: Hierarchical Reinforcement Learning with Explicit Credit Assignment for Large Language Model Agents

## Summary

HiPER decomposes LLM agent policies into a high-level planner (proposes subgoals) and a low-level executor (carries them out), introducing hierarchical advantage estimation (HAE) that aggregates returns over each subgoal's execution window and coordinates updates across both levels. Theoretical analysis proves HAE is unbiased and achieves strictly lower variance than flat GAE when hierarchical structure is present. With Qwen2.5-7B-Instruct, HiPER reaches 97.4% on ALFWorld (+6.6%) and 83.3% on WebShop (+8.3%), with especially large gains on long-horizon tasks requiring multiple dependent subtasks.

## Key Contributions

- Hierarchical Plan-Execute RL framework (HiPER): high-level planner proposes subgoals, low-level executor implements them over multiple action steps
- Hierarchical Advantage Estimation (HAE): returns aggregated over subgoal execution windows, with provably lower variance than flat GAE under hierarchical structure — unbiasedness theorem provided
- State-of-art: 97.4% ALFWorld (+6.6%), 83.3% WebShop (+8.3%) with 7B model, particularly dominant on long-horizon multi-subtask configurations
- HAE coordinates credit updates across both levels simultaneously, avoiding the credit propagation lag that afflicts flat policies on long horizons

## Relevance

HiPER directly extends the hierarchical RL thread opened by ARISE (Jun 12), which built a Manager skill library and Worker reasoning without a variance-reduction guarantee. HiPER provides the theoretical underpinning: HAE's lower-variance proof explains why hierarchical decomposition helps not just intuitively but quantifiably, and the 7B results on ALFWorld now represent the state of the art on that benchmark.

## My Thoughts

<!-- Add your own notes here -->
