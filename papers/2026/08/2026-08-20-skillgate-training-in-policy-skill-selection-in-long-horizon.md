---
title: "SkillGate: Training In-Policy Skill Selection in Long-Horizon Agents"
authors: ["Qingyao Li", "Wenxiang Jiao", "Shuai Shao", "Kangning Zhang", "Yuan Lu", "Yi Guo", "Weiwen Liu", "Weinan Zhang", "Yong Yu"]
date: 2026-08-19
arxiv_id: "2608.18852"
url: "https://arxiv.org/abs/2608.18852"
score: 0.87
topics: [agentic RL, tool use, LLM agent, RL training]
status: unread
---

# SkillGate: Training In-Policy Skill Selection in Long-Horizon Agents

## Summary

Identifies "selector credit starvation": in long-horizon agentic RL, broadcast sequence-level advantage assigns vanishing and often wrong-signed credit to the sparse skill-selection tokens, preventing effective tool/skill selection learning. SkillGate resolves this with disjoint credit channels — outcome reward reaches only execution tokens, while a separate action-local advantage trains the selector with positive signal only when the correct skill is chosen. On five agentic benchmarks with 16-candidate slates, a 9B policy improves from 40.8% to 53.2% trial success.

## Key Contributions

- Formal identification and empirical audit of selector credit starvation: wrong-signed credit, vanishing magnitude, and monotonic worsening with trajectory length
- Disjoint credit channel architecture: outcome advantage (execution tokens) + action-local advantage (selector tokens only) — each trained on its correct signal without cross-contamination
- 12.4pp absolute improvement on a 9B model across five benchmarks; two-thirds reduction in exposure to misleading skill candidates
- Explains why standard outcome-rewarded RL structurally cannot teach skill/tool selection in long-horizon settings

## Relevance

Selector credit starvation is a foundational problem for any agentic RL system that uses a skill or tool library — it explains why vanilla GRPO or PPO training fails to teach the agent which tool to invoke. This connects directly to the vault's agentic RL and tool use threads (OrchestraBench, Agent Lightning, LEGO-RL) and provides a principled fix that any multi-tool agentic RL pipeline needs.

## My Thoughts

<!-- Add your own notes here -->
