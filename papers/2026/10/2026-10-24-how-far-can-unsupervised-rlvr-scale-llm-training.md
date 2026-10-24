---
title: "How Far Can Unsupervised RLVR Scale LLM Training?"
authors: ["Bingxiang He", "Yuxin Zuo", "Zeyuan Liu", "Shangziqi Zhao", "Zixuan Fu", "Junlin Yang", "Cheng Qian", "Kaiyan Zhang", "Yuchen Fan", "Ganqu Cui", "Xiusi Chen", "Youbang Sun", "Xingtai Lv", "Xuekai Zhu", "Li Sheng", "Ran Li", "Huan-ang Gao", "Yuchen Zhang", "Bowen Zhou", "Zhiyuan Liu", "Ning Ding"]
date: 2026-03-09
arxiv_id: "2603.08660v1"
url: "http://arxiv.org/abs/2603.08660v1"
score: 0.81
topics: [RLHF, RLAIF, reward model, reinforcement learning, RL training]
status: unread
---

# How Far Can Unsupervised RLVR Scale LLM Training?

## Summary

Comprehensive analysis of unsupervised RLVR classifying intrinsic vs. external reward methods and showing all intrinsic approaches converge toward sharpening the model's initial distribution—succeeding when confidence aligns with correctness but collapsing catastrophically otherwise. Systematic experiments confirm intrinsic rewards follow a rise-then-fall pattern with collapse timing determined by model prior, not engineering choices; proposes Model Collapse Step as a practical RL trainability indicator. Shows external rewards grounded in computational asymmetries may escape the confidence-correctness ceiling.

## Key Contributions

- Unified theoretical framework showing all intrinsic RLVR methods reduce to sharpening the base model's initial distribution — success requires confidence-correctness alignment as a prerequisite
- Empirical confirmation of universal rise-then-fall pattern across intrinsic methods; collapse timing is determined by model prior (Model Collapse Step), not reward engineering choices
- Model Collapse Step as a practical pre-training indicator for RL trainability: measure it before committing to RL post-training
- Evidence that external rewards (grounded in computational asymmetry, not model confidence) may escape the sharpening ceiling — motivating a path beyond intrinsic URLVR

## Relevance

Provides the theoretical ceiling analysis for the RL training dynamics/scaling thread: while IsoCompute and the empirical scaling paper focus on resource allocation within RLVR, this paper characterizes the fundamental limit of intrinsic reward methods and proposes a diagnostic (Model Collapse Step) for knowing when RL post-training will succeed vs. fail.

## My Thoughts

<!-- Add your own notes here -->
