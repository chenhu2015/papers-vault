---
title: "SkillRise: Agentic Reinforcement Learning for Cross-Task Skill Evolution"
authors: ["Zhiyuan Yao", "Yuxin Chen", "Zhengxi Lu", "Zishan Xu", "Yueqing Sun", "Yifu Guo", "Yuquan Lu", "Zhengzhou Cai", "Kangning Zhang", "Zhuowen Han", "Zi-Han Wang", "Ziang Ye", "Qi Gu", "Xunliang Cai", "Weiwen Liu", "Yongliang Shen"]
date: 2026-07-31
arxiv_id: "2607.26784"
url: "https://arxiv.org/abs/2607.26784"
score: 0.82
topics: [agentic RL, LLM agent, tool use, GRPO]
status: unread
---

# SkillRise: Agentic Reinforcement Learning for Cross-Task Skill Evolution

## Summary

SkillRise is a unified RL framework for cross-task skill evolution that organizes related tasks into progressively challenging sequences and trains a single policy to alternate between task solving and curating an evolving skill document passed directly to the next task. Decoupled credit assignment supervises task-solving with current-task outcome and skill curation with discounted downstream outcomes — a credit signal that flows across task boundaries. Achieves strongest Pass@1 on ALFWorld, WebShop, and ScienceWorld (2.3-8.5pp gains over the strongest baseline), with test-time scaling: performance improves with longer sequences of related tasks even when each task is attempted only once.

## Key Contributions

- Cross-task skill evolution via a single policy that alternates between task-solving and skill-curation roles
- Decoupled credit assignment: task-solving supervised by current-task outcome, skill-curation supervised by discounted downstream outcomes across tasks
- Progressive task sequencing: related instances organized into progressively challenging sequences for curriculum learning
- Test-time scaling: longer task sequences improve performance, demonstrating transferable skill reuse rather than repeated-sample benefits

## Relevance

SkillRise sits at the intersection of the agentic RL thread (ReSkill, Bayesian-Agent) and the credit assignment thread. Its decoupled credit assignment — where skill curation is rewarded by *downstream* task outcomes — is a fundamentally different credit signal from within-episode credit (all prior vault papers). This cross-episode credit flow is structurally closer to the branch-level credit gap (Gap #8 remaining: branch↔fork) than to token/turn-level credit, since the skill document is a persistent state that persists *between* episodes, making each curation decision a branch point for a downstream MDP. SkillRise provides the first implementation of cross-episode credit assignment for skill learning in agentic RL.

## My Thoughts

<!-- Add your own notes here -->
