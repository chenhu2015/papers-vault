---
title: "Bayesian-Agent: Posterior-Guided Skill Evolution for LLM Agent Harnesses"
authors: ["Xiaojun Wu", "Cehao Yang", "Honghao Liu", "Xueyuan Lin", "Wenjie Zhang", "Zhichao Shi", "Xuhui Jiang", "Chengjin Xu", "Jia Li", "Jian Guo"]
date: 2026-07-30
arxiv_id: "2606.08348v1"
url: "http://arxiv.org/abs/2606.08348v1"
score: 0.82
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# Bayesian-Agent: Posterior-Guided Skill Evolution for LLM Agent Harnesses

## Summary

Bayesian-Agent treats reusable skills and SOPs as hypotheses about whether a frozen model will succeed under particular harness conditions, maintaining a feature-conditioned categorical Bayesian posterior over each skill and mapping posterior state into inspectable lifecycle actions: patch, split, compress, retire, and explore. Unlike ReSkill (Jul 29)'s Thompson Sampling for version selection within a skill, Bayesian-Agent's posterior directly governs the entire skill lifecycle including retirement and exploration, enabling principled management of skill reliability under distribution shift without updating model weights. Improves SOP-Bench from 80% to 95%, Lifelong AgentBench from 90% to 100%, and RealFin-Bench from 45% to 65% with deepseek-v4-flash.

## Key Contributions

- Feature-conditioned categorical Bayesian posterior over each skill, tracking reliability as verified trajectory evidence accumulates
- Posterior state maps to five inspectable actions: patch (fix failing skills), split (separate skill for different contexts), compress (reduce complexity), retire (remove unreliable skills), explore (test unvalidated skills)
- Cross-harness framework: evaluated on native backend and GenericAgent, mini-swe-agent, and Claude Code backends
- Demonstrates skill evolution as posterior-guided optimization, not heuristic reflection

## Relevance

Bayesian-Agent is the Bayesian complement to ReSkill (Jul 29, Thompson Sampling + adaptive discounting for skill version selection). ReSkill addresses the question "which version of an existing skill to use"; Bayesian-Agent addresses the prior question "what to do with a skill whose reliability is changing" — providing lifecycle management (retire/split/explore) that ReSkill's bandit formulation does not cover. Together they characterize two layers of the agentic skill management problem: selection (Thompson Sampling, ReSkill) and lifecycle (Bayesian posterior, Bayesian-Agent), a connection not drawn by either paper.

## My Thoughts

<!-- Add your own notes here -->
