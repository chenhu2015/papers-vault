---
title: "Bradley-Terry Training Can Distort Outcome Probabilities of Initially Accurate Language World Models"
authors: ["Xinze Shi", "Litian Zhang", "Zhenjie Su", "Zelong Yu", "Yuting Zhang", "Qihua Feng", "Zifeng Kang", "Chaozhuo Li", "Zhengxuan Hu"]
date: 2026-11-19
arxiv_id: "2611.25594"
url: "https://arxiv.org/abs/2611.25594"
score: 0.76
topics: [RLHF, reward model, reinforcement learning, RL training]
status: unread
---

# Bradley-Terry Training Can Distort Outcome Probabilities of Initially Accurate Language World Models

## Summary

This paper shows that the Bradley-Terry comparative feedback objective—the core of most RLHF pipelines—can systematically distort accurate outcome probability distributions, shifting 33–43 percentage points onto physically impossible outcomes even when starting from an accurate model. The distortion is in the objective itself (its optimum predicts the final model's behavior before training), and a likelihood that correctly accounts for the judge's rule avoids the shift entirely.

## Key Contributions

- Demonstrates BT objective distorts outcome probabilities even starting from an accurate model: 33–43 pp shift to impossible outcomes on a simulated robot push task
- The distortion is in the objective, not the data: the BT optimum, computed analytically before training, predicts exactly where the trained model ends up
- A judge-aware likelihood (that knows the comparison rule) learns from the same comparisons without the distortion
- Quantifies utility cost: false-reject threshold inflation costs ~3 pp utility per decision; without impossible events the cost averages below 1 pp

## Relevance

Directly extends the Forecasting RLHF thread opened on Nov 20, which characterized how RM edits propagate to policy behavior. This paper identifies a more fundamental failure mode: the BT training objective itself can reverse an accurate model's calibration, providing a theoretical diagnosis that complements Forecasting RLHF's empirical covariance-based predictor.

## My Thoughts

<!-- Add your own notes here -->
