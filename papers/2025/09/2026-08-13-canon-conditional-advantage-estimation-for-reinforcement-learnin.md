---
title: "Conditional Advantage Estimation for Reinforcement Learning in Large Reasoning Models"
authors: ["Guanxu Chen", "Yafu Li", "Yuxian Jiang", "Chen Qian", "Qihan Ren", "Jingyi Yang", "Yu Cheng", "Dongrui Liu", "Jing Shao"]
date: 2026-08-13
arxiv_id: "2509.23962"
url: "https://arxiv.org/abs/2509.23962"
score: 0.72
topics: [GRPO, RL training, RLHF, reward model, PPO]
status: unread
---

# Conditional Advantage Estimation for Reinforcement Learning in Large Reasoning Models

## Summary

CANON regroups RLVR sampled responses into high/low subsets based on a target metric (entropy, length), measures which metric trend contributes to better performance through inter-group comparison, and identifies the better response within the same group — amplifying the target metric's impact without presuming a directional prior. This avoids the failure mode of hand-crafted higher-is-better/lower-is-better preferences that require careful hyperparameter tuning and can bias training adversely. Applied to entropy, CANON consistently outperforms prior methods on math reasoning and high-complexity logic tasks; applied to length, it yields a more favorable performance-cost Pareto frontier.

## Key Contributions

- Direction-agnostic metric amplification: inter-group comparison determines which direction of the target metric benefits performance, without hand-crafting a directional prior
- Two-level grouping: inter-group measures metric trend contribution; intra-group identifies the better response within the same metric level
- Applied to entropy: consistently outperforms prior entropy-shaped advantage methods across three LLMs
- Applied to length: improves token efficiency with better performance-cost Pareto frontier

## Relevance

CANON's direction-agnostic inter-group comparison is a new approach to advantage shaping that sits between GRPO's group-relative baseline (over reward) and DASH's sequential divergence history (over step-level divergence). Where GRPO normalizes advantage by group reward statistics and DASH gates by divergence sequence fit, CANON conditions advantage on whether a target metric (entropy, length) is correlated with reward improvement in that group — deriving the direction empirically rather than assuming it. This connects to the vault's entropy-credit thread (SoftmaxGRPO from Aug 11 used temperature-scaled softmax for entropy control; CANON uses inter-group comparison for entropy direction inference) and to the vault's GRPO normalization thread more broadly.

## My Thoughts

<!-- Add your own notes here -->
