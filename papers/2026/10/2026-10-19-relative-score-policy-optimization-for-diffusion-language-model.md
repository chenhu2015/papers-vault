---
title: "Relative Score Policy Optimization for Diffusion Language Models"
authors: ["RSPO authors"]
date: 2026-10-19
arxiv_id: "2605.10218v1"
url: "http://arxiv.org/abs/2605.10218v1"
score: 0.82
topics: [GRPO, RL training, reward model, RLHF]
status: unread
---

# Relative Score Policy Optimization for Diffusion Language Models

## Summary

RSPO sidesteps the high-variance ELBO problem in dLLM policy optimization by reinterpreting the reward advantage as a calibration target for the noisy relative log-ratio between current and reference policies — updating based on the gap between the estimated and reward-implied log-ratio rather than the raw advantage. This avoids the amplification of inaccurate score estimates under high verifier rewards, yielding especially strong gains on planning tasks and competitive math-reasoning performance.

## Key Contributions

- Identifies that high verifier rewards amplify ELBO approximation error, destabilizing dLLM RL
- Proposes reward advantage as a target for the relative log-ratio (not just an update direction)
- RSPO updates based on gap between current log-ratio estimate and reward-implied target
- Strong planning task performance; competitive math reasoning vs ELBO-based baselines

## Relevance

Fifth paper in the diffusion LM RL thread (PACT + GDPO + CJ-GRPO + DiSPO + RSPO). RSPO addresses the objective instability problem from a different angle than DiSPO (credit) or CJ-GRPO (consistency): it targets the ELBO variance at high reward magnitudes, complementing GDPO's ELBO-based approach with a calibration-based alternative.

## My Thoughts

<!-- Add your own notes here -->
