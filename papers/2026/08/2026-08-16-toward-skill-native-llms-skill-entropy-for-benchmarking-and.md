---
title: "Toward Skill-Native LLMs: Skill Entropy for Benchmarking and Training Long-Horizon Reasoning"
authors: ["Yinghui He", "Ling Yang", "Jiarui Liu", "Yongjin Yang", "Lechen Zhang", "Yingcheng Wu", "Zhenfei Yin", "Mengdi Wang", "Sanjeev Arora"]
date: 2026-08-05
arxiv_id: "2608.05139v1"
url: "https://arxiv.org/abs/2608.05139"
score: 0.79
topics: [agentic RL, LLM agent, reinforcement learning, GRPO]
status: unread
---

# Toward Skill-Native LLMs: Skill Entropy for Benchmarking and Training Long-Horizon Reasoning

## Summary

Skill Entropy formalizes the difficulty of switching from one skill to another within a multi-step reasoning chain, enabling Skill²-Bench: a benchmark of 558 cross-skill long-horizon tasks across 9 domains where each task requires sequential application of different skills. Skill-Entropy RL trains models to predict both the answer and the skill used at each step, combining step-level correctness with a skill-entropy reward that measures alignment between predicted and gold skill sequences. On Qwen3-4B-Instruct, Skill-Entropy RL improves Skill²-Bench score from 34.4% to 68.4%, and the skill-entropy reward transfers to off-the-shelf training data like OpenR1-Math.

## Key Contributions

- Skill Entropy: a principled measure of cross-skill switching difficulty (a pairwise information-theoretic measure over skill transition pairs)
- Skill²-Bench: 558 cross-skill tasks across 9 verifiable/open-ended domains at three difficulty levels defined by task-level skill-entropy score
- Skill-Entropy RL: step-level skill prediction + skill-entropy reward combined with step-correctness reward; applicable to any verifiable reasoning dataset
- 34.4% → 68.4% on Skill²-Bench for Qwen3-4B-Instruct; reusable reward signal on OpenR1-Math without Skill²-Bench data

## Relevance

Skill Entropy directly formalizes Gap #21 (complexity threshold for skill management). Gap #21 has been framed as: when does a skill set become too complex to manage, and how should RL training respond? Skill Entropy answers the "when" question with a principled pairwise measure (cross-skill transition difficulty), and Skill-Entropy RL answers the "how" question with a step-level reward aligned to the skill sequence. BCSD (Aug 14) was the closest prior approximation via skill utilization supervision; Skill Entropy replaces that indirect proxy with a formal definition. Gap #21 is now substantially closed — the boundary is defined by the skill-entropy score, and RL can optimize toward it.

## My Thoughts

<!-- Add your own notes here -->
