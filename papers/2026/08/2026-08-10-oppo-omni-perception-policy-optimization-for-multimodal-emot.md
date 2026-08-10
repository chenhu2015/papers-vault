---
title: "Omni-Perception Policy Optimization for Multimodal Emotion Reasoning"
authors: ["Zhiyuan Han", "Beier Zhu", "Wenwen Tong", "Pengyang Shao", "Peipei Song", "Xinyi Wang", "Jiangnan Chen", "Lewei Lu", "Xun Yang"]
date: 2026-08-10
arxiv_id: "2606.25325"
url: "https://arxiv.org/abs/2606.25325"
score: 0.72
topics: [multimodal, vision-language, VLM, RLHF]
status: unread
---

# Omni-Perception Policy Optimization for Multimodal Emotion Reasoning

## Summary

OPPO introduces a reinforcement learning framework for multimodal emotion reasoning that optimizes both utilization and faithfulness of omni-modal perception. An Omni-Perception Reward decomposes ground-truth reasoning into visual, acoustic, and emotion cue components, rewarding trajectories that semantically recover all cue types; an Omni-Perception Loss applies KL penalties on modality-specific evidence tokens when those inputs are masked, directly suppressing cross-modal hallucination. Achieves state-of-the-art on MER-UniBench and MME-Emotion while substantially improving utilization and faithfulness scores on the new MEP-Bench diagnostic benchmark.

## Key Contributions

- Omni-Perception Reward: decomposes ground-truth reasoning into fine-grained visual, acoustic, and emotion cues; rewards trajectories that semantically recover all cue types
- Omni-Perception Loss: compares policy under full vs. unimodally masked inputs; applies KL penalty only to modality-specific evidence tokens to suppress cross-modal hallucination
- MEP-Bench: diagnostic benchmark quantifying both utilization (are multimodal cues used?) and faithfulness (are they accurately represented without hallucination?)
- Multi-modal extension of the visual faithfulness RL training signal approach (cf. IAPO, ViGOS)

## Relevance

OPPO extends the vault's Gap #7 (visual faithfulness as VLM RL training signal) from visual-only to omni-modal settings. IAPO (Aug 3) introduced faithfulness as a reward signal for VLM RL; ViGOS (Jun 17) decoupled perception and reasoning in OPD to prevent shortcut; OPPO extends both ideas to audio+visual emotion reasoning by combining reward-level cue recovery with loss-level masked-input KL on evidence tokens. The masked-input KL approach (penalize modality-specific tokens when that modality is removed) is structurally analogous to VAD's counterfactual evidence attribution but operates as a training loss rather than a supervision target reconstruction.

## My Thoughts

<!-- Add your own notes here -->
