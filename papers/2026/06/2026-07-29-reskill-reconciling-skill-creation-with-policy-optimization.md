---
title: "ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL"
authors: ["Zelin He", "Haotian Lin", "Boran Han", "Wei Zhu", "Haoyang Fang", "Bernie Wang", "Xuan Zhu", "Runze Li", "Matthew Reimherr"]
date: 2026-06-01
arxiv_id: "2606.01619"
url: "https://arxiv.org/abs/2606.01619"
score: 0.75
topics: [agentic RL, RL training, LLM agent, tool use, GRPO]
status: unread
---

# ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL

## Summary

ReSkill reconciles modular skill evolution with policy learning in agentic RL by embedding skill creation within the GRPO training loop via three mechanisms: an assertion-driven skill creator diagnosing failures and proposing trigger-based conditional skill revisions; within-group rollout sampling exploiting GRPO's group structure for controlled skill-version comparison; and Thompson Sampling with adaptive discounting for skill-version exploration under an evolving policy. ReSkill consistently outperforms existing memory and skill-based RL methods with the largest gains on unseen tasks, and exhibits automatic skill lifecycle management (create, test, refine, prune as policy improves).

## Key Contributions

- **Assertion-driven skill creator**: diagnoses past failures and proposes conditional, trigger-based skill revisions rather than monolithic skill updates
- **Within-group rollout**: uses GRPO's group structure to compare skill versions in controlled settings — same group, different skill versions — providing direct comparative signal without separate ablation runs
- **Thompson Sampling + adaptive discounting**: balances skill version exploration/exploitation as the policy evolves; discounting ensures older skill comparisons are down-weighted as the policy distribution shifts
- **Automatic lifecycle**: skills are created, tested, refined, and pruned continuously; largest improvements on unseen tasks suggest skills capture generalizable rather than task-specific behaviors

## Relevance

Novel exploitation of GRPO's group structure for a purpose orthogonal to credit assignment: rather than using within-group variance to estimate token-level or turn-level advantage (as in CIGPO, EmoAgent-R1/P-GRPO, STAPO), ReSkill uses within-group rollout to compare discrete skill versions under matched policy conditions. Connects to SEED (Jul 25, hindsight skill distillation) — SEED converts completed trajectories into auxiliary loss signals; ReSkill creates explicitly represented and versioned skills that are tested and pruned online. Also connects to PATS (Jul 25, adaptive scaffolding) — both adapt what is presented to the model at training time, but at different levels (PATS: prompt-level evidence cards; ReSkill: code-level skill functions).

## My Thoughts

<!-- Add your own notes here -->
