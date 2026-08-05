---
title: "Progressive Agent Skill Generation via Reinforcement Learning"
authors: ["Junhao Shen", "Zhanqiu Zhang", "Yiwen Guo", "Hong Cheng"]
date: 2026-08-05
arxiv_id: "2608.01678"
url: "https://arxiv.org/abs/2608.01678"
score: 0.80
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# Progressive Agent Skill Generation via Reinforcement Learning

## Summary

Skill-α formulates agent skill generation as a sequential editing process and trains a skill generator using RL with a rollback reward: each edit is evaluated by comparing downstream task execution under the original vs. edited skill on an anchored query, giving a supervision signal tied directly to task performance rather than heuristics. This avoids the pipeline-specific design limitations of prior skill generation methods and handles heterogeneous evidence sources uniformly. Under a GPT-4o worker, Skill-α improves average success rates over the strongest baseline by 3.3 points on CL-Bench and 6.7 points on tau2-bench.

## Key Contributions

- Rollback reward: evaluates each skill edit by comparing downstream execution under original vs. edited skill on an anchored query — ties skill quality directly to task performance
- Sequential editing decomposition: breaks skill construction into individually evaluable steps, enabling RL credit at the edit level
- Handles both document-to-skill and experience-to-skill generation settings with a unified learning objective
- 3.3pt improvement on CL-Bench and 6.7pt on tau2-bench over strongest pipeline-based baseline

## Relevance

Skill-α extends the vault's skill lifecycle synthesis (SkillRise → Bayesian-Agent → ReSkill → UCOB → SPyCE) with a RL-native skill *generation* mechanism. Prior papers addressed skill retrieval (Bayesian-Agent, ReSkill), skill evolution (SkillRise, SPyCE), and skill-credit integration (UCOB), but none trained the skill generator itself with RL. Skill-α's rollback reward is structurally analogous to UCOB's return-to-go comparison at anchor states — both compare execution outcomes under two skill conditions at a reference query — but Skill-α applies this comparison to improve the *skill generator policy* rather than the *task-execution policy*.

## My Thoughts

<!-- Add your own notes here -->
