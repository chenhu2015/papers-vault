---
title: "Distributional Process Reward Models: Calibrated Prediction of Future Rewards via Conditional Optimal Transport"
authors: ["Rachel Ma", "Dylan Hadfield-Menell", "Kristjan Greenewald"]
date: 2026-06-14
arxiv_id: "2605.06785v2"
url: "http://arxiv.org/abs/2605.06785v2"
score: 0.78
topics: [reward model, RLHF, RL training, GRPO]
status: unread
---

# Distributional Process Reward Models: Calibrated Prediction of Future Rewards via Conditional Optimal Transport

## Summary

Distributional PRMs calibrate process reward model uncertainty via conditional optimal transport (CondOT), learning a monotone conditional quantile function over PRM-estimated success probabilities conditioned on PRM hidden states — yielding structurally valid calibration without ad hoc binning. Integrated into the instance-adaptive scaling (IAS) framework for Best-of-N selection, calibrated PRMs improve both calibration error and downstream task accuracy on MATH-500 and AIME. The approach identifies that conventional PRMs are systematically overconfident on hard OOD problems (AIME) — precisely the regime where calibration matters most for test-time scaling.

## Key Contributions

- First application of conditional optimal transport to PRM calibration: CondOT map produces structurally valid monotone quantile estimates over PRM success probabilities, conditioned on PRM hidden states
- Identifies that standard PRMs are most poorly calibrated on hard OOD instances (AIME), creating a reliability gap exactly where test-time scaling is most needed
- Integration with Instance-Adaptive Scaling (IAS) for Best-of-N: calibrated confidence bounds enable principled instance-level compute allocation
- Improves calibration substantially over uncalibrated PRMs and baseline quantile regression, with downstream Best-of-N gains on MATH-500 and AIME

## Relevance

Distributional PRMs directly extends the PRM calibration thread from PRISM (Jun 13), which showed that step-level class imbalance causes PRMs to overcredit wrong steps. PRISM attacked bias in the training objective; Distributional PRMs attacks bias in the score distribution post-training — the two approaches are complementary layers: fix training-time bias (PRISM), then calibrate inference-time uncertainty (this paper).

## My Thoughts

<!-- Add your own notes here -->
