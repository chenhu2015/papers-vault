---
title: "Process Rewards with Learned Reliability"
authors: ["Jinyuan Li", "Langlin Huang", "Chengsong Huang", "Shaoyang Xu", "Donghong Cai", "Yuyi Yang", "Wenxuan Zhang", "Jiaxin Huang"]
date: 2026-07-21
arxiv_id: "2605.15529"
url: "https://arxiv.org/abs/2605.15529"
score: 0.83
topics: [reinforcement learning, RL training, reward model, RLHF]
status: unread
---

# Process Rewards with Learned Reliability

## Summary

BetaPRM identifies that current PRMs output a single scalar reward per step without indicating when that prediction should be trusted, forcing downstream methods to treat imperfect step-level signals as uniformly reliable decision inputs. The distributional PRM predicts both a step-level success probability and a calibrated reliability estimate via a Beta distribution parameterized from Monte Carlo step-success supervision, enabling downstream methods to weight process rewards by trustworthiness rather than magnitude alone. The reliability output directly addresses the gap FaithRL identified: using a PRM as a faithfulness judge requires knowing when the PRM's step-level signal is trustworthy — BetaPRM makes this explicit through distributional prediction.

## Key Contributions

- Identification of the uniform-reliability assumption in current PRMs as a structural limitation: downstream methods cannot distinguish confident correct step signals from uncertain/noisy ones
- BetaPRM: distributional PRM predicting a Beta distribution over step-level success probability, yielding both a point estimate and a reliability (concentration) parameter
- Monte Carlo step-success supervision to train the Beta distribution's parameters end-to-end
- Reliability-weighted downstream usage: step-level rewards weighted by their calibrated trustworthiness, enabling robust PRM integration in RL training loops

## Relevance

BetaPRM closes the queued gap from FaithRL (Jul 20): FaithRL uses a PRM as a faithfulness judge in step-level RL, but standard PRMs output undifferentiated scalars — BetaPRM provides the reliability signal needed to trust those step-level judgments. This extends the vault's PRM thread (GroundedPRM, KV-PRM, SCI-PRM, LLMs-as-a-Jury, Paradox of Outcome Optimization) with a calibration dimension: not just "what is the process quality?" but "how confident should we be in this process quality estimate?" The Paradox paper established that PRMs are topologically necessary for causal generalization; BetaPRM establishes that uncalibrated PRMs introduce a second failure mode when used as training signals.

## My Thoughts

<!-- Add your own notes here -->
