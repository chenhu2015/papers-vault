---
title: "Process Reward Modeling with Reliability- and Conservatism-Aware Bayesian Belief"
authors: ["Zhongjian Qiao", "Zhixiang Zhou", "Jiafei Lyu", "Peisong Wang", "Qiaosheng Zhang", "Siyang Gao", "Shuang Qiu"]
date: 2026-10-16
arxiv_id: "2610.23223v1"
url: "https://arxiv.org/abs/2610.23223"
score: 0.75
topics: [reward model, multimodal models, RLVR, vision-language, VLM]
status: unread
---

# Process Reward Modeling with Reliability- and Conservatism-Aware Bayesian Belief

## Summary

BayesianPRM treats the process reward as a random variable and maintains a Bayesian belief over a discretized reward ensemble via two complementary updates: reliability-aware updating (how well each ensemble member explains supervision data, via an amortized ELBO network) and conservatism-aware calibration (reweighting toward lower rewards to suppress policy-mismatch-induced overestimation). The resulting calibrated reward consistently improves test-time scaling on multimodal reasoning benchmarks.

## Key Contributions

- Bayesian belief over PRM ensemble: process reward treated as random variable; belief maintained over discretized reward hypothesis space
- Reliability-aware belief updating: amortized ELBO network measures each ensemble member's fit to supervision data
- Conservatism-aware calibration: belief reweighted toward lower rewards to suppress systematic overestimation from train/test policy mismatch
- Multimodal reasoning gains: consistently better test-time scaling on multimodal benchmarks vs. standard PRMs

## Relevance

Directly relevant to both the reward model thread and the VLM/multimodal thread. The reliability + conservatism two-axis calibration framework is a principled extension of the PRM calibration work in the step-credit cluster (TACE's distributional normalization, OVC's outcome-conditioned calibration), adding a Bayesian uncertainty angle. The policy mismatch / overestimation problem diagnosed here also connects to the GRPO training dynamics thread (VeXact, DLC on training-inference mismatch).

## My Thoughts

<!-- Add your own notes here -->
