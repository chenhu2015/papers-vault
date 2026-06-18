---
title: "Preference Instability in Reward Models: Detection and Mitigation via Sparse Autoencoders"
authors: ["Shunchang Liu", "Xin Chen", "Belen Martin Urcelay", "Francesco Croce"]
date: 2026-06-18
arxiv_id: "2605.16339"
url: "https://arxiv.org/abs/2605.16339"
score: 0.83
topics: [reward model, RLHF, agentic RL]
status: unread
---

# Preference Instability in Reward Models: Detection and Mitigation via Sparse Autoencoders

## Summary

Reward models exhibit preference instability — contradictory preference rankings under meaning-preserving perturbations (paraphrasing, pattern injection, backdoor triggers) — due to over-reliance on brittle "unstable features" isolable in a sparse SAE latent space where benign and perturbed inputs activate separable patterns. Two SAE-based mitigation strategies are proposed: Feature Steering (suppresses anomalously activated features at inference) and Residual Correction (learns adaptive adjustments over SAE features), both of which substantially reduce incorrect preference assignments on harmlessness and hallucination benchmarks without retraining the reward model.

## Key Contributions

- Characterizes RM preference instability under three semantic-preserving perturbation types and attributes it to "unstable features" over-activated by brittle surface patterns
- SAE Feature Steering: identifies and suppresses anomalously activated features at inference time, requires no retraining
- SAE Residual Correction: learns adaptive adjustments over SAE features to restore correct preferences
- Both methods preserve benign performance and general utility, validated on harmlessness and hallucination benchmarks

## Relevance

Directly addresses the reward model robustness thread opened by HARVE (Jun 8, reward-head vector editing) and PRIME (Jun 17, proxy reward internalization): where HARVE patches the RM's representation of reward hacking and PRIME tracks the policy's hacking capability, this paper patches the RM's surface-feature brittleness — a third intervention point in the reward model quality stack, targeting distributional robustness rather than hacking specifically.

## My Thoughts

<!-- Add your own notes here -->
