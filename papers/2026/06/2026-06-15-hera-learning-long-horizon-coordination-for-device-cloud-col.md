---
title: "Hera: Learning Long-Horizon Coordination for Device-Cloud Collaborative LLM Agents"
authors: ["Yuxin Zhang", "Mengxue Hu", "Zheng Lin", "Xiaoyi Fan", "Fan Xie", "Zihan Fang", "Jing Yang", "Wenjun Zhu", "Zhiwen Chen", "Chengfei Lv", "Zhe Chen"]
date: 2026-05-23
arxiv_id: "2605.24598v1"
url: "https://arxiv.org/abs/2605.24598"
score: 0.71
topics: [agentic RL, RL training, LLM agent, reinforcement learning]
status: unread
---

# Hera: Learning Long-Horizon Coordination for Device-Cloud Collaborative LLM Agents

## Summary

Hera trains a step-level device-cloud routing policy via imitation learning cold-start followed by cost-aware RL that jointly optimizes task success and cloud API usage efficiency, grouping identical states across trajectories for dense supervision. On ALFWorld, WebShop, and AppWorld, Hera achieves 92.5% of cloud-only success while routing only 46.3% of steps to the cloud model. The cost-aware RL formulation shows agentic RL can be applied to inference-time resource management, not just training-time capability improvement.

## Key Contributions

- Step-level device-cloud routing (vs. task-level) for LLM agent coordination at multi-turn granularity
- Two-stage training: imitation learning cold-start using state-action agreement labels, followed by cost-aware RL
- Cost-aware RL that jointly optimizes task success rate and cloud call reduction with shared objective
- Strong performance-cost Pareto frontier across ALFWorld, WebShop, and AppWorld benchmarks

## Relevance

Applies RL to the deployment efficiency problem for agentic LLMs — a complementary angle to the training-side RL focus of recent digests. The step-level routing connects to ARISE's (Jun 12) Manager/Worker decomposition: Hera's routing policy plays a similar manager role, deciding when to escalate to stronger computation rather than when to invoke a skill.

## My Thoughts

<!-- Add your own notes here -->
