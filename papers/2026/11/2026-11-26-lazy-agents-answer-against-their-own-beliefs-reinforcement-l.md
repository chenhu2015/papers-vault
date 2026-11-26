---
title: "Lazy Agents Answer Against Their Own Beliefs: Reinforcement Learning with Verifiable Beliefs Teaches Them to Act on What They Believe"
authors: ["Richmond Sin Jing Xuan", "Peilin Feng", "Wenbin Wang", "Soujanya Poria"]
date: 2026-11-24
arxiv_id: "2611.32884"
url: "https://arxiv.org/abs/2611.32884"
score: 0.76
topics: [agentic RL, LLM agent, reinforcement learning, reward model]
status: unread
---

# Lazy Agents Answer Against Their Own Beliefs: Reinforcement Learning with Verifiable Beliefs Teaches Them to Act on What They Believe

## Summary

RLVB (RL with Verifiable Beliefs) addresses agent laziness — premature answer commitment before sufficient evidence — by rewarding continued exploration when the simulator's posterior still allows multiple answers and committing when evidence narrows. No judge, critic, or reward model is needed; the reward is computed directly from the simulator's posterior. Improves three VLMs by 17.1% average across 9 settings, outperforming PPO with LLM-judge process reward by 9.3% at 1.6× lower compute.

## Key Contributions

- Identifies agent laziness as a distinct failure mode: agents commit to answers even when their own stated belief names multiple candidates, because outcome reward treats lucky guesses and evidence-backed answers equally
- RLVB reward: positive for taking further steps when posterior admits multiple answers, positive for committing when evidence is sufficient — computable directly from simulator state with no external judge
- Introduces Pro Worlds benchmark: visual puzzles viewed through a small window, requiring evidence-gathering over multiple steps
- Outperforms PPO+LLM-judge process reward by 9.3% at 1.6× fewer GPU-hours; GRPO and PPO with outcome-only reward fall below baseline on average

## Relevance

Advances the agentic RL thread from a new angle: rather than fixing credit assignment (TACA, MSPO) or tool-call reward (DM-PRM), RLVB fixes the commitment timing problem using verifiable beliefs as a training signal. The connection to DM-PRM is notable — both use simulator-side computation instead of a trained reward model, but RLVB targets the commitment decision rather than step quality.

## My Thoughts

<!-- Add your own notes here -->
