---
title: "Drop the Act: Probe-Filtered RL for Faithful Chain-of-Thought Reasoning"
authors: ["Swapnil Parekh"]
date: 2026-05-12
arxiv_id: "2605.11467v1"
url: "http://arxiv.org/abs/2605.11467v1"
score: 0.80
topics: [RL training, GRPO, RLHF, reward model]
status: unread
---

# Drop the Act: Probe-Filtered RL for Faithful Chain-of-Thought Reasoning

## Summary

ProFIL trains a multi-head attention probe once on the frozen base model to detect post-commitment "reasoning theater" steps from internal activations; during GRPO, rollouts whose probe score exceeds a threshold have their advantage zeroed. Training on a frozen base (rather than the evolving RL model) provides robustness to RL's obfuscation failure mode. Across four reasoning domains and two architectures, ProFIL reduces theater by 11-100%, raises faithful-fraction by up to +24pp, and shortens chains 4-19% while preserving or improving task accuracy.

## Key Contributions

- Definition of "reasoning theater" (post-commitment deliberative steps) as a formal GRPO failure mode
- Frozen-base probe design for robustness to RL obfuscation (Goodhart-like failure for in-training probes)
- Advantage zeroing as a training-time trajectory filter; no post-hoc editing needed
- Verifier-derived labels, no human annotation; generalizes across reasoning domains and architectures

## Relevance

ProFIL extends the DRE thread (Jun 19, which edits post-answer continuation from successful trajectories post-hoc before the RL update) with an in-training activation-based detection mechanism — ProFIL is the "during training" counterpart to DRE's "before update" editing. The frozen-base design directly addresses the compound failure mode that the First-Principles paper (Jun 16) identified: RL obfuscates in-training signals, so the probe must be anchored to the pre-RL base to remain reliable. Together with STRIDE (Jun 20) and DRE (Jun 19), ProFIL completes a three-layer trajectory credit stack: detect theater at activation level (ProFIL), contrast discriminative patterns at n-gram level (STRIDE), edit successful-trajectory suffixes post-rollout (DRE).

## My Thoughts

<!-- Add your own notes here -->
