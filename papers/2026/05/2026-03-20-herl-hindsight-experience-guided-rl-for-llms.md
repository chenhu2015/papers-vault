---
title: "Experience is the Best Teacher: Motivating Effective Exploration in Reinforcement Learning for LLMs"
authors: ["Wenjian Zhang", "Kongcheng Zhang", "Jiaxin Qi", "Baisheng Lai", "Jianqiang Huang"]
date: 2026-03-20
arxiv_id: "2603.20046v1"
url: "http://arxiv.org/abs/2603.20046v1"
score: 0.79
topics: [RL training, agentic RL, reward model]
status: unread
---

# Experience is the Best Teacher: Motivating Effective Exploration in Reinforcement Learning for LLMs

## Summary

HeRL treats failed RL trajectories together with their unmet rubrics as hindsight experience, injecting this as in-context guidance to steer the policy beyond its current distribution. A bonus reward further incentivises responses with greater improvement potential under such guidance. Achieves superior gains over baselines and benefits additionally from experience-guided self-improvement at test time.

## Key Contributions

- Hindsight experience: failed trajectories + their unmet rubrics repurposed as in-context steering signals
- Bonus reward for responses that show improvement potential when given hindsight guidance
- Theoretically provides more accurate expected gradient estimation than standard trial-and-error RL
- Test-time self-improvement via experience-guided rollouts, beyond just training-time gains

## Relevance

Addresses the same exploration bottleneck as RAGEN-2 (reasoning collapse) but through a hindsight lens: instead of filtering bad samples, HeRL actively repurposes failed trajectories as curriculum. Rubric-based unmet goals as in-context guidance also connects to the reward model / RLAIF thread in the interest profile.

## My Thoughts

<!-- Add your own notes here -->
