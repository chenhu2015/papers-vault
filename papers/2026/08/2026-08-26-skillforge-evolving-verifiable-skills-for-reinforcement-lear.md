---
title: "SkillForge: Evolving Verifiable Skills for Reinforcement Learning Agents"
authors: ["Shidong Yang", "Ziyu Ma", "Tongwen Huang", "Xucong Wang", "Renda Li", "Yiming Hu", "Yong Wang", "Xiangxiang Chu"]
date: 2026-08-25
arxiv_id: "2608.24747v1"
url: "http://arxiv.org/abs/2608.24747v1"
score: 0.87
topics: [agentic RL, RL training, tool use]
status: unread
---

# SkillForge: Evolving Verifiable Skills for Reinforcement Learning Agents

## Summary

SkillForge extends SkillRL with continuous skill verification and refinement: the agent explicitly marks which skills it invoked, enabling RL to directly optimize both environment actions and skill invocation decisions. Evidence-based skill verification prunes ineffective skills while multi-pathway induction adds new ones, keeping the bank quality-controlled as it grows. Tested on ALFWorld, WebShop, and AppWorld, outperforming SkillRL and other skill-based baselines.

## Key Contributions

- Makes skill invocation explicit during agent interaction so RL can jointly optimize environment actions and skill selection decisions
- Evidence-based skill verification: prunes skills that no longer improve task performance under the current policy
- Multi-pathway skill induction: grows the skill bank through multiple induction routes rather than append-only trajectory extraction
- Outperforms SkillRL (its direct predecessor) on ALFWorld, WebShop, and AppWorld

## Relevance

Directly extends the skill-reuse thread established by SPyCE (Aug 23) and SkillGate (Aug 20): where SPyCE co-evolves a skill library with the policy in multimodal settings, SkillForge adds the missing quality-control loop — skills that become stale are verified and pruned, not just appended. This answers the append-only failure mode that SkillRL exhibited and that SPyCE addressed only implicitly through co-evolution.

## My Thoughts

<!-- Add your own notes here -->
