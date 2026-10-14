---
title: "Same Reward, Different Skills: When Multimodal RL Learns to Look"
authors: ["Haocun Ye", "Xinlong Jiang", "Qile Chen", "Bingyu Wang", "Teng Zhang", "Shubai Chen", "Tingyu Wu", "Zhenkun Zheng", "Yiqiang Chen"]
date: 2026-10-14
arxiv_id: "2610.01908v1"
url: "http://arxiv.org/abs/2610.01908v1"
score: 0.82
topics: [agentic RL, RL training, multimodal models, vision language models, VLM, GRPO]
status: unread
---

# Same Reward, Different Skills: When Multimodal RL Learns to Look

## Summary

Demonstrates that standard RLVR improves vision-language benchmark scores even when images are absent during training, with blind-trained models recovering ~80% of real-image gains at 7B — revealing that benchmark gains and genuine visual grounding can diverge. Introduces the "visual resolvability" design principle: tasks must require visual evidence for correct answers and remain learnable, validated on counterfactual coordinate scenes where a 7B model raises discovery accuracy from 0.425 to 0.875 with standard GRPO. The key insight is that what RL is required to reward determines what skill it actually learns, with captions that answer training questions cutting visual grounding gains by two-thirds.

## Key Contributions

- Quantifies blind-trained vs. real-image-trained RLVR gap: blind models recover ~50% at 3B and ~80% at 7B of real-image gains, suggesting much of the benchmark improvement is non-visual
- "Visual resolvability" principle: target must be visually findable and not nameable in the question
- Counterfactual coordinate task design: no target name in question, correct answer requires locating target in image, tests generalize to unseen denser scenes and novel question types
- Control showing caption-answer leakage cuts grounding gain by ~2/3, directly implicating reward specification in skill learning

## Relevance

Directly addresses a core open question in the VLM RL credit thread: whether reward signals in GRPO/RLVR pipelines actually drive visual grounding or merely surface-level pattern matching. Connects to the RVCO/DyCPO open question on whether credit budgets improve late-stage optimization stability — this paper suggests the upstream task design may matter as much as the credit assignment method.

## My Thoughts

<!-- Add your own notes here -->
