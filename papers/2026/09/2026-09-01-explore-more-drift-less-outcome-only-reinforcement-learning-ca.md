---
title: "Explore More, Drift Less: Outcome-Only Reinforcement Learning Can Suffice for Long-Horizon Interactive Agents"
authors: ["Liming Pu", "Xiaoxia Li", "Yifu Liu"]
date: 2026-09-01
arxiv_id: "2609.01245v1"
url: "http://arxiv.org/abs/2609.01245v1"
score: 0.87
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Explore More, Drift Less: Outcome-Only Reinforcement Learning Can Suffice for Long-Horizon Interactive Agents

## Summary

CANOPY (Coverage-ANchored On-PolicY RL) argues that the apparent ceiling of outcome-only RL on small models is caused by signal starvation (GRPO produces zero gradient when rollout groups fail to mix successes and failures, silencing the hardest tasks) and policy drift (many updates on a small task pool collapse the sampling distribution once saturation makes informative groups rare). CANOPY addresses both directly: scale same-task exploration until natural signal reappears, keep every update on-policy and KL-anchored, and expand the interaction budget at test time. A Qwen3-14B policy trained with CANOPY topped the AppWorld public leaderboard (Feb 2026) with 86.9 Test-Normal TGC and 67.6 Test-Challenge; the same design principles lift Qwen3.5-9B on SWE-bench Verified by 16.6 points.

## Key Contributions

- Signal starvation diagnosis: group-relative RL produces zero gradient for tasks where all rollouts succeed or all fail — under-scaled exploration silences exactly the hardest, most instructive tasks
- Coverage-anchored exploration: scale same-task rollouts until the natural success/failure mix reappears — no auxiliary reward or process signal needed
- Policy drift prevention: on-policy updates + KL anchor + confinement to the agent's own action tokens — prevents distribution collapse as the policy improves
- Test-time interaction budget expansion as a first-class design dimension alongside training-time coverage

## Relevance

CANOPY is the strongest empirical counterevidence yet to the "dense credit is necessary for long-horizon RL" conclusion that has been building across recent digests (T1, TASPO, CRISP, PLVR). If outcome-only RL with coverage-anchoring can top AppWorld without dense intermediate rewards, the key variable may be exploration coverage rather than reward density. This does not invalidate the dense-credit thread — CANOPY's enlarged test-time budget may be doing the work that dense rewards do at training time — but it shifts the question from "how to assign credit" to "when does credit become necessary vs. when does better exploration suffice."

## My Thoughts

<!-- Add your own notes here -->
