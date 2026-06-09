---
title: "Video Understanding Reward Modeling: A Robust Benchmark and Performant Reward Models"
authors: ["Yuancheng Wei", "Linli Yao", "Lei Li", "Haojie Zhang", "Hao Zhou", "Fandong Meng", "Xu Sun"]
date: 2026-06-09
arxiv_id: "2605.07872"
url: "https://arxiv.org/abs/2605.07872"
score: 0.77
topics: [reward model, RLHF, multimodal models, VLM, vision-language]
status: unread
---

# Video Understanding Reward Modeling: A Robust Benchmark and Performant Reward Models

## Summary

Video Understanding Reward Bench (VURB) provides 2,100 preference pairs with long chain-of-thought traces for evaluating multimodal reward models across general, long, and reasoning-oriented video tasks. An automated pipeline constructs VUP-35K video preference data for training VideoDRM (discriminative) and VideoGRM (generative) reward models, both achieving SOTA on VURB with significant best-of-N test-time scaling gains. Results confirm that preference data quality rather than quantity drives reward model capability in the video domain.

## Key Contributions

- VURB: first robust benchmark for video reward models with long-CoT preference pairs
- VUP-35K: large-scale automated video preference dataset construction pipeline
- VideoDRM (discriminative) and VideoGRM (generative) reward models achieving SOTA
- Best-of-N test-time scaling demonstrated to work effectively for video reward models

## Relevance

Fills a gap in the reward model thread: previous weeks covered RM-NLHF, RefCritic, SAVE, HARVE, and RREDCoT — all for text/math. This extends reward modeling to video understanding (long, reasoning-heavy video tasks), relevant to the multimodal VLM interest area. The automated preference data pipeline parallels the SUPERNOVA data curation thread and provides a scalable approach for multimodal RLHF without costly human annotation.

## My Thoughts

<!-- Add your own notes here -->
