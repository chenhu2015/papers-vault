---
title: "PRO-CUA: Process-Reward Optimization for Computer Use Agents"
authors: ["Yifei He", "Rui Yang", "Hao Bai", "Tong Zhang", "Han Zhao"]
date: 2026-05-31
arxiv_id: "2605.29119"
url: "https://arxiv.org/abs/2605.29119"
score: 0.85
topics: [agentic RL, tool use, LLM agent, reward model, PPO]
status: unread
---

# PRO-CUA: Process-Reward Optimization for Computer Use Agents

## Summary

PRO-CUA decouples on-policy GUI environment rollouts from policy optimization: the agent generates diverse candidate actions per state, receives step-level feedback from a PRM, and is optimized with group-relative advantages — avoiding golden answers or offline expert trajectories. This iterative PRM-guided design provides dense credit assignment for long-horizon GUI interaction and reduces distribution shift by training on the agent's own execution states.

## Key Contributions

- Decouples on-policy GUI rollout from policy optimization, enabling iterative PRM-guided training without golden answers or expert demos
- Group-relative advantage computation from PRM step-level feedback avoids sparse trajectory-level rewards for long-horizon GUI tasks
- Reduces distribution shift by training on the agent's own live execution states rather than offline demonstrations
- Validated on live web benchmarks, demonstrating reliable step-level PRM guidance for computer use agents

## Relevance

A key instance of the agentic RL + tool use thread applied to computer use; pairs well with DeepTool's deliberation approach. The group-relative advantage from PRM is essentially GRPO applied at the step level for GUI agents — extending the GRPO methodology the user tracks into computer use domains.

## My Thoughts

<!-- Add your own notes here -->
