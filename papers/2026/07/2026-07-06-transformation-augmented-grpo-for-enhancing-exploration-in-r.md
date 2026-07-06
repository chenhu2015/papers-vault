---
title: "Transformation-Augmented GRPO for Enhancing Exploration in Reasoning of Large Language Models"
authors: ["Khiem Le", "Phuc Nguyen", "Youssef Mroueh", "Chi-Heng Lin", "Shangqian Gao", "Ting Hua", "Nitesh V. Chawla"]
date: 2026-01-30
arxiv_id: "2601.22478v5"
url: "http://arxiv.org/abs/2601.22478v5"
score: 0.75
topics: [GRPO, RL training, reinforcement learning, reward model]
status: unread
---

# Transformation-Augmented GRPO for Enhancing Exploration in Reasoning of Large Language Models

## Summary

TA-GRPO addresses GRPO's two core failure modes — gradient vanishing (all-identical-reward groups yield zero gradients) and diversity collapse (convergence to a single reasoning pattern) — by automatically generating multiple semantically equivalent rephrasings of each training question and pooling responses across the original and rephrasings into a joint group with mixed rewards and diverse paths. Advantages are jointly computed over this expanded response set with importance ratios aligned to the original question, yielding +4.97pp and +4.34pp pass@32 on Qwen3-1.7B and Qwen3-4B on AMC/OlympiadBench/AIME while matching baselines trained on 2.5× more data.

## Key Contributions

- Formal diagnosis of gradient vanishing (uniform-reward groups) and diversity collapse (single-pattern convergence) as GRPO's two co-occurring failure modes
- Question rephrasing via LLM to generate problem-equivalent variants that shift perceived difficulty, ensuring mixed-reward groups without changing the training curriculum
- Joint advantage computation over the expanded rephrasing pool with importance ratios anchored to the original question — preserving the on-policy learning signal while exploiting rephrasing-induced diversity
- +4.97pp pass@32 gains on competition-level math (AMC, OlympiadBench, AIME24/25) and OOD generalization (Minerva, GPQA-Diamond)

## Relevance

TA-GRPO addresses the same failure mode cluster that AREW/SeL (Jul 5) diagnosed as information self-locking, but from the training signal angle rather than the reward reweighting angle: where AREW's directional critiques reweight the reward signal post-hoc, TA-GRPO restructures the group formation pre-hoc to guarantee mixed-reward gradients. The two approaches are complementary and could in principle be combined — rephrasing to prevent diversity collapse, directional critiques to recover from SeL when collapse occurs despite rephrasing.

## My Thoughts

<!-- Add your own notes here -->
