---
title: "RLVMR: Reinforcement Learning with Verifiable Meta-Reasoning Rewards for Robust Long-Horizon Agents"
authors: ["Zijing Zhang", "Ziyang Chen", "Mingxiao Li", "Zhaopeng Tu", "Xiaolong Li"]
date: 2025-07-30
arxiv_id: "2507.22844"
url: "https://arxiv.org/abs/2507.22844"
score: 0.80
topics: [agentic RL, LLM agent, RLAIF, reward model]
status: unread
---

# RLVMR: Reinforcement Learning with Verifiable Meta-Reasoning Rewards for Robust Long-Horizon Agents

## Summary

RLVMR integrates dense process-level supervision into end-to-end RL by rewarding verifiable meta-reasoning behaviors: the agent explicitly tags its cognitive steps (planning, exploration, reflection) and receives programmatic rule-based rewards for actions that contribute to effective problem-solving. These process-centric rewards combine with the final outcome signal and are optimized via a critic-free policy gradient, addressing the 'inefficient exploration' failure mode where outcome-only RL reinforces flawed reasoning paths. Achieves 83.6% on the most-difficult unseen ALFWorld split with a 7B model (new SoTA), with reduced redundant actions and enhanced error recovery.

## Key Contributions

- **Meta-reasoning step tagging**: agent explicitly tags each cognitive step as planning, exploration, or reflection — making the reasoning structure legible to the reward system
- **Verifiable process reward**: programmatic rule-based rewards assigned for meta-reasoning tags that contribute to problem-solving, without needing a learned reward model
- **Critic-free policy gradient**: process rewards + outcome signal optimized without a value function, reducing infrastructure complexity
- New SoTA on ALFWorld (83.6% hardest unseen split, 7B) and ScienceWorld; analysis shows gains come from reduced redundant actions and improved error recovery rather than just exploration volume

## Relevance

Provides a domain-knowledge-based process supervision approach complementary to the statistics-based credit assignment family (IG-based: IGPO/InfoReasoner/InfoPO/CIGPO/A²TGPO; entropy-based: STAPO/ERPO/STARE/ICT): instead of deriving process signals from outcome reward statistics or token entropy, RLVMR specifies verifiable cognitive behaviors as the process reward, opening the question of whether meta-reasoning tags could be combined with IG-based signals for compound process supervision.

## My Thoughts

<!-- Add your own notes here -->
