---
title: "Video-RTS: Rethinking Reinforcement Learning and Test-Time Scaling for Efficient and Enhanced Video Reasoning"
authors: ["Ziyang Wang", "Jaehong Yoon", "Shoubin Yu", "Md Mohaiminul Islam", "Gedas Bertasius", "Mohit Bansal"]
date: 2025-07-09
arxiv_id: "2507.06485"
url: "https://arxiv.org/abs/2507.06485"
score: 0.82
topics: [multimodal models, vision language models, VLM, RL training, agentic RL]
status: unread
---

# Video-RTS: Rethinking Reinforcement Learning and Test-Time Scaling for Efficient and Enhanced Video Reasoning

## Summary

Video-RTS skips the resource-intensive SFT stage and uses pure output-based RL training for video reasoning with no annotations, then pairs this with a sparse-to-dense video test-time scaling strategy that iteratively adds frames based on output consistency. Using only 3.6% of training samples, Video-RTS surpasses existing video reasoning models by 2.4% accuracy and achieves a 4.2% improvement on Video-Holmes. The pure RL training and adaptive video TTS offer complementary strengths, extending the RL+TTS synergy to video multimodal models.

## Key Contributions

- Pure RL training for video reasoning without SFT pretraining stage, using only output-based rewards and no annotations
- Sparse-to-dense video TTS: iteratively adds frames based on output consistency, providing adaptive frame budget allocation at inference time
- 3.6% training data → +2.4% accuracy over models trained on full data; +4.2% on Video-Holmes
- Demonstrates RL training and video-adaptive TTS have complementary strengths that combine additively

## Relevance

Video-RTS extends the RL+TTS synergy thread (RL^V, T1) specifically to the multimodal video domain, joining PRISM and SaGe (Jul 11) in the vault's VLM RL section. The sparse-to-dense frame TTS is the video-domain analog of ROSE's semantic-entropy branching (Jul 10): both adaptively allocate compute at inference time — ROSE by exploring diverse reasoning paths, Video-RTS by progressively densifying temporal context. The pure RL without SFT finding also directly extends the data efficiency thread established by PRISM's three-stage pipeline.

## My Thoughts

<!-- Add your own notes here -->
