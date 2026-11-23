---
title: "TPMM-DPO: Trajectory-aware Preference-guided Model Merging for Iterative Direct Preference Optimization"
authors: ["Lingling Fu", "Yongfu Xu"]
date: 2026-05-22
arxiv_id: "2605.23398"
url: "https://arxiv.org/abs/2605.23398"
score: 0.70
topics: [RLHF, RL training]
status: unread
---

# TPMM-DPO: Trajectory-aware Preference-guided Model Merging for Iterative Direct Preference Optimization

## Summary

TPMM-DPO addresses iterative DPO's late-stage over-optimization by treating the sequence of policy models from successive iterations as an optimization trajectory and merging them with learned fusion weights rather than using the most recent model as reference. This smooths the reference model, mitigating noise accumulation from noisy preference data and iterative reference drift, yielding consistent generation quality improvements and higher reward scores on in-domain and out-of-domain evaluations.

## Key Contributions

- Identification of late-stage over-optimization and performance fluctuation in standard iterative DPO due to noisy preference data accumulating in the reference model
- Trajectory-aware merging: treats the sequence of policy models as an optimization path and adaptively weights them to build a smoother reference model
- Learnable fusion weights outperform simple averaging at mitigating late-stage degradation from noisy preferences
- Consistent improvements in win rates and reward scores on in-domain and out-of-domain benchmarks

## Relevance

Adjacent to the RLHF training dynamics thread: where Gate-DPO addresses probability collapse within a single training run and BT-Distortion addresses the objective-level calibration failure, TPMM-DPO addresses the multi-iteration drift problem in iterative RLHF pipelines. Practical angle useful when the user considers iterative DPO for post-training.

## My Thoughts

<!-- Add your own notes here -->
