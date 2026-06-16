---
title: "Retrospective Progress-Aware Self-Refinement for LLM Agent Training"
authors: ["Xinbei Ma", "Congmin Zheng", "Jiyang Qiu", "Jiale Hong", "Yao Yao", "Xiangmou Qu", "Jiaxin Yin", "Xingyu Lou", "Jun Wang", "Weiwen Liu", "Weinan Zhang", "Zhuosheng Zhang", "Hai Zhao"]
date: 2026-06-16
arxiv_id: "2606.14302v1"
url: "http://arxiv.org/abs/2606.14302v1"
score: 0.75
topics: [reinforcement learning, agentic RL, LLM agent, RL training]
status: unread
---

# Retrospective Progress-Aware Self-Refinement for LLM Agent Training

## Summary

RePro trains LLM agents to self-generate progress signals via a forward-then-reflect rollout paradigm: the agent first executes actions online, then retrospectively reassesses step-wise progress given the completed trajectory and known outcome, teaching metacognitive awareness that outcome-reward training alone cannot produce. A Retrospection Warmup initializes reflection format from minimal external demonstrations, followed by RePro-PO with a composite reward that produces self-generated progress supervision without continuous external labeling. Evaluated on WebShop, ALFWorld, and Sokoban, RePro yields up to 12% absolute success rate gains for Qwen models.

## Key Contributions

- Forward-then-reflect rollout paradigm: online action execution followed by retrospective self-assessment of step-wise progress
- Retrospection Warmup bootstraps reflection capability from minimal demonstrations without full SFT
- RePro-PO composite reward combines task success with quality of self-generated progress signals
- Pilot study finding: online progress prompting hurts performance while retrospective demonstrations help — motivating the asymmetric training design

## Relevance

RePro addresses the same gap as 3SPO (Jun 11) and StepOPSD (today): the mismatch between sparse trajectory-level rewards and local step decisions that determine success. Where 3SPO uses historical success rates to generate static state scores and StepOPSD uses hindsight distillation, RePro teaches the agent to generate its own progress commentary — a metacognitive approach that sits closer to the ARISE/SENTINEL self-reflection paradigm than to external credit assignment. The finding that retrospective (but not online) progress prompting helps is a useful empirical constraint for designing future agent RL training curricula.

## My Thoughts

<!-- Add your own notes here -->
