---
title: "Why Does RL Generalize Better Than SFT? A Data-Centric Perspective on VLM Post-Training"
authors: ["Aojun Lu", "Tao Feng", "Hangjie Yuan", "Wei Li", "Yanan Sun"]
date: 2026-02-11
arxiv_id: "2602.10815v1"
url: "http://arxiv.org/abs/2602.10815v1"
score: 0.80
topics: [multimodal models, vision-language models, VLM, RLHF, RL training]
status: unread
---

# Why Does RL Generalize Better Than SFT? A Data-Centric Perspective on VLM Post-Training

## Summary

RL's superior OOD generalization over SFT on VLMs is explained by an implicit data filtering effect: RL inherently prioritizes medium-difficulty samples because hard samples yield near-zero group advantage signals and easy samples yield near-zero loss gradients, while SFT treats all training samples uniformly. DC-SFT (Difficulty-Curated SFT) that explicitly filters the training set to medium-difficulty samples matches or exceeds RL's OOD generalization with greater stability and efficiency, suggesting that data difficulty selection — not the RL algorithm per se — is the operative mechanism behind the generalization advantage.

## Key Contributions

- Systematic evaluation of SFT OOD generalization across training datasets of varying difficulty levels, confirming hard samples significantly degrade OOD performance on VLMs
- Data-centric explanation of the RL–SFT generalization gap: RL acts as an implicit curriculum filter selecting medium-difficulty samples
- DC-SFT: difficulty-based training set filtering that replicates and surpasses RL OOD generalization without the instability or compute overhead of RL
- Practical implication: data curation achieves robust VLM generalization more efficiently than RL post-training, which challenges the narrative that RL algorithms have inherent generalization advantages

## Relevance

This paper extends the ReasonMaxxer/Curriculum-RL (Jun 20/Jun 21) thread to the multimodal domain, providing a data-centric account of why RL post-training generalizes better on VLMs. It is the most direct VLM-specific result in this digest series (the interest profile explicitly includes multimodal models and VLMs), and its DC-SFT result also has implications for the RL-guided distillation thread queued from Jun 30 — if difficulty filtering is the active ingredient, then RL-distilled data pipelines may be replaceable with cheaper offline curation.

## My Thoughts

<!-- Add your own notes here -->
