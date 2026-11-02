---
title: "When Fine-Grained Credit Assignment Helps and Hurts: Multimodal Agentic Reinforcement Learning through Video Editing"
authors: ["Lei Zhao", "Zongheng Cao", "Xinyu Hu"]
date: 2026-11-02
arxiv_id: "2610.35497v1"
url: "http://arxiv.org/abs/2610.35497v1"
score: 0.81
topics: [agentic RL, multimodal models, vision language models, RLAIF, reward model, GRPO]
status: unread
---

# When Fine-Grained Credit Assignment Helps and Hurts: Multimodal Agentic Reinforcement Learning through Video Editing

## Summary

A systematic study of when process rewards help vs. hurt in multimodal agentic RL, using video editing (4 task types spanning 30–60+ turn horizons) as a testbed. Decaying process rewards yield a 45.4% relative gain on long-horizon tasks (60+ turns) but only marginal gains on shorter-horizon tasks where outcome-only GRPO is competitive; fixed process-reward weight causes reward hacking (process reward rises while task completion falls), which decaying the weight to zero mitigates. On-policy self-distillation (OPSD) yields little improvement and is highly sensitive to privileged information choice.

## Key Contributions

- Task-horizon finding: fine-grained process rewards significantly help on 60+ turn tasks but not on 30–40 turn tasks where outcome GRPO is competitive
- Reward hacking diagnosis: fixed process-reward weight causes process metric and task completion to diverge; decaying to zero mitigates this
- OPSD evaluation: dense token-level supervision from self-distillation shows little gain and high sensitivity, suggesting signal dilution over long trajectories
- Four video editing task types as a controlled multimodal agentic RL testbed

## Relevance

This paper bridges the VLM RL reward-design thread (SophiaVL-R1, SVQA-R1, MRPO) and the long-horizon agentic RL thread by providing the first empirical answer to a key open question: does fine-grained credit assignment actually help in multimodal long-horizon settings? The horizon-dependent finding complements SCOPE's selective-step distillation (today) and CoFire's confidence erosion diagnosis (Oct 31).

## My Thoughts

<!-- Add your own notes here -->
