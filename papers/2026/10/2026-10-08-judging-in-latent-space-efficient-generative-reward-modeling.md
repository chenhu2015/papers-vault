---
title: "Judging in Latent Space: Efficient Generative Reward Modeling via Semantics-Preserving Compression"
authors: ["Mingqing Yuan", "Xiaobo Liang", "Junwei Yang", "Ziwei Chen"]
date: 2026-10-08
arxiv_id: "2610.09788v1"
url: "http://arxiv.org/abs/2610.09788v1"
score: 0.76
topics: [reward model, RLHF, multimodal models]
status: unread
---

# Judging in Latent Space: Efficient Generative Reward Modeling via Semantics-Preserving Compression

## Summary

LatentGRM replaces token-by-token verbalization in generative reward models with compact continuous latent trajectories derived from rubric-guided semantic chunking and compression. A separate interpreter reconstructs evaluation text from the latent trajectory offline, confirming that criterion-dependent preference information is retained under compression. LatentGRM-8B achieves competitive preference accuracy versus explicit SFT judges while compressing evaluation trajectories by 8.9–9.2× and reducing total judge inference time by 6.1–7.0× at vote@5.

## Key Contributions

- Rubric-guided semantic chunking and compression into continuous latent trajectories for reward modeling
- Offline interpreter that reconstructs evaluation text to verify information retention under compression
- 8.9–9.2× trajectory compression and 6.1–7.0× inference speedup at vote@5 versus token-by-token GRM
- Controlled rubric interventions showing criterion-dependent preference information survives latent encoding

## Relevance

Relevant to reward model efficiency — an orthogonal axis to the credit assignment thread. If generative reward models (relevant to EnGRICH and the process reward cluster) are too slow for online RL training, LatentGRM's compression is a practical enabler. Connects the reward-model-efficiency concern to the latent reasoning trend.

## My Thoughts

<!-- Add your own notes here -->
