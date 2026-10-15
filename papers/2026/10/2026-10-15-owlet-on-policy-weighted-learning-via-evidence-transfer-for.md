---
title: "OWLET: On-Policy Weighted Learning via Evidence Transfer for Video Large Language Model Post-Training"
authors: ["Qitan Lv", "Ke Fan", "Hong Wang", "Wen Wu", "Yilin Wang", "Bowen Zhou", "Feng Wu", "Chao Zhang"]
date: 2026-10-15
arxiv_id: "2610.13272v1"
url: "https://arxiv.org/abs/2610.13272"
score: 0.90
topics: [agentic RL, VLM, vision-language, multimodal, RLHF, reward model]
status: unread
---

# OWLET: On-Policy Weighted Learning via Evidence Transfer for Video Large Language Model Post-Training

## Summary

OWLET introduces evidence-aware credit redistribution for Video-LLM RL post-training: it constructs a privileged teacher view combining global temporal context with question-conditioned local windows, then redistributes response-level advantages to tokens according to their relative evidence support (likelihood difference between views). A spatiotemporal state alignment objective aligns hidden states on verifier-accepted responses, providing structural supervision that RLVR alone misses.

## Key Contributions

- Evidence-aware credit redistribution: token-level advantage weighting by comparing likelihoods under global vs. local-evidence teacher views
- Spatiotemporal state alignment: hidden-state-level supervision on verifier-accepted responses to guide internal representation
- No larger teacher model required — privileged view is constructed from the same model with different frame sampling
- Addresses the known failure mode of RLVR for video: same response-level advantage ignores that tokens differ in their visual grounding degree

## Relevance

Directly extends the VLM RL credit assignment thread with a video-specific evidence-transfer mechanism. The privileged-view construction (global + local question-conditioned frames) is a concrete architectural answer to the "visual resolvability" concern raised by "Same Reward, Different Skills" (Oct 14): OWLET operationalises resolvability as a token-likelihood differential rather than a binary flag, and uses it to reweight advantages in-training rather than as a post-hoc diagnostic.

## My Thoughts

<!-- Add your own notes here -->
