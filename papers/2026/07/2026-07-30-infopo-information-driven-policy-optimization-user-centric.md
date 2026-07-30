---
title: "InfoPO: Information-Driven Policy Optimization for User-Centric Agents"
authors: ["Fanqi Kong", "Jiayi Zhang", "Mingyi Deng", "Chenglin Wu", "Yuyu Luo", "Bang Liu"]
date: 2026-07-30
arxiv_id: "2603.00656v2"
url: "http://arxiv.org/abs/2603.00656v2"
score: 0.80
topics: [agentic RL, RL training, GRPO, tool use, LLM agent]
status: unread
---

# InfoPO: Information-Driven Policy Optimization for User-Centric Agents

## Summary

InfoPO frames multi-turn interaction as active uncertainty reduction and computes a distinct IG definition: it credits turns whose feedback measurably changes the agent's subsequent action distribution compared to a masked-feedback counterfactual, rather than measuring log-likelihood changes (IGPO/CIGPO) or semantic clustering (InfoReasoner). This counterfactual IG is combined with task outcomes via adaptive variance-gated fusion to identify information importance while maintaining task-oriented goal direction. Consistently outperforms prompting and multi-turn RL baselines on intent clarification, collaborative coding, and tool-augmented decision making, with robustness under user simulator shifts and generalization to environment-interactive tasks.

## Key Contributions

- Third distinct IG definition in the multi-turn RL family: IG = change in agent's action distribution when feedback is masked vs. observed (counterfactual information gain)
- Adaptive variance-gated fusion that combines IG signal with task outcomes, dynamically weighting importance by signal variance
- Broader coverage than retrieval/search: applied to intent clarification, collaborative coding, and tool-augmented decision making
- Robustness under user simulator distribution shift — generalizes to environment-interactive tasks

## Relevance

InfoPO completes the taxonomy of IG definitions in the multi-turn LLM RL literature: IGPO/CIGPO (IG = Δ log P_policy(y*)), InfoReasoner (IG = uncertainty reduction via semantic clustering), InfoPO (IG = Δ action distribution vs. masked counterfactual). The counterfactual definition is the most model-agnostic of the three — it requires neither a reference model nor belief-state estimation, only forward passes of the agent under two conditions. InfoPO's variance-gated fusion is also structurally parallel to TAO-RL (today, 0.83)'s entropy-guided bonus: both modulate the strength of the auxiliary signal based on how much informative variance it carries at a given turn.

## My Thoughts

<!-- Add your own notes here -->
