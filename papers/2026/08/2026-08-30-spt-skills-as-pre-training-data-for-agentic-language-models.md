---
title: "SPT: Skills as Pre-Training Data for Agentic Language Models"
authors: ["Yufei Sun", "Yudong Li", "Yiming Cheng"]
date: 2026-08-30
arxiv_id: "2608.26563"
url: "https://arxiv.org/abs/2608.26563"
score: 0.79
topics: [agentic RL, LLM agent, tool use, RL training, reinforcement learning]
status: unread
---

# SPT: Skills as Pre-Training Data for Agentic Language Models

## Summary

Introduces Skill Pre-Training (SPT), a mid-training method that applies causal language modeling to SkillCorpus—a collection of public multi-file skill packages—using Reference Insert, a reference-aware assembly strategy that places supporting files near their mentions in the primary instruction file. Experiments across model scales and post-training recipes show SPT consistently improves agentic performance over mid-training on trajectory data or general data while largely preserving general capability; skill data combined with general annealing corpora yields additional gains.

## Key Contributions

- SkillCorpus: curated collection of public multi-file skill packages as pre-training data for agentic LMs
- Reference Insert: reference-aware file assembly that preserves inter-file relationships critical for skill comprehension
- Mid-training on skills (before RL post-training) improves agentic performance more than trajectory or general data mid-training
- Skill data and general annealing corpora are complementary — mixing yields additional gains over either alone

## Relevance

SPT occupies a previously empty position in the skill-evolution design space: all prior vault skill papers (SkillForge, Skill-R1, Skill1, SKILL0) use explicit skill libraries during RL training time. SPT instead absorbs skill knowledge into base model parameters during mid-training before any RL begins. This creates a new axis for the skill-vs-experience internalization taxonomy: (1) inference-time skill retrieval (SKILL0), (2) RL-time skill library evolution (SkillForge/Skill-R1/Skill1), (3) pre-training skill absorption (SPT) — whether these are complementary or substitutes is an open empirical question.

## My Thoughts

<!-- Add your own notes here -->
