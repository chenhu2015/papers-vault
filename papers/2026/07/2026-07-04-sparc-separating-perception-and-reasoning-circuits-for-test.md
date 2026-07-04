---
title: "SPARC: Separating Perception And Reasoning Circuits for Test-time Scaling of VLMs"
authors: ["Niccolo Avogaro", "Nayanika Debnath", "Li Mi", "Thomas Frick", "Junling Wang", "Zexue He", "Hang Hua", "Konrad Schindler", "Mattia Rigotti"]
date: 2026-07-04
arxiv_id: "2602.06566"
url: "https://arxiv.org/abs/2602.06566"
score: 0.78
topics: [multimodal models, vision-language models, VLM, agentic]
status: unread
---

# SPARC: Separating Perception And Reasoning Circuits for Test-time Scaling of VLMs

## Summary

SPARC decouples visual perception from reasoning in VLMs via a two-stage pipeline — global visual search first localizes question-relevant regions, then high-resolution reasoning conditions on those regions — enabling asymmetric compute allocation and independent optimization of each stage. The separation compresses context by running global search at lower resolution and allocating high-resolution processing only to selected regions, reducing visual token count. SPARC improves Qwen3VL-4B on V* VQA by 6.7 points and surpasses "thinking with images" by 4.6 points OOD with a 200× lower token budget.

## Key Contributions

- Explicit architectural decoupling of visual perception and reasoning as two independently scalable stages; inspired by sequential sensory-to-cognitive brain processing
- Asymmetric test-time compute allocation: perception or reasoning stage can be independently scaled or optimized based on which is the bottleneck
- Compressed context via low-resolution global visual search + high-resolution selective cropping of localized regions, reducing visual token count
- Supports selective RL optimization of the perceptual stage alone when perception is the bottleneck — avoids expensive end-to-end fine-tuning

## Relevance

SPARC is the VLM architectural counterpart to PASS (Jul 1): where PASS identified channel contamination between process and outcome signals in text RL, SPARC solves the analogous problem at the VLM level by structurally separating the perception channel from the reasoning channel so each can be independently supervised and scaled. The 200× token budget reduction is the most concrete compute efficiency result in the VLM test-time scaling thread; the OOD setting (distribution shift) connects to the RL generalization theme from "Why RL Generalizes Better Than SFT" (Jul 1).

## My Thoughts

<!-- Add your own notes here -->
