---
title: "Efficient RLVR Training via Weighted Mutual Information Data Selection"
authors: ["Xinyu Zhou", "Boyu Zhu", "Haotian Zhang", "Huiming Wang", "Zhijiang Guo"]
date: 2026-03-02
arxiv_id: "2603.01907v1"
url: "https://arxiv.org/abs/2603.01907"
score: 0.78
topics: [RLHF, GRPO, RL training, reward model]
status: unread
---

# Efficient RLVR Training via Weighted Mutual Information Data Selection

## Summary

InSight grounds RLVR data selection in a weighted mutual information objective with Bayesian latent success rates, decomposing expected uncertainty reduction into difficulty- and evidence-dependent components that expose the limitation of difficulty-only heuristics. Rather than using noisy sampled outcomes, InSight constructs a stable acquisition score from the mean belief of success rates, naturally extending to multi-rollout RLVR settings. InSight achieves +1.41 average gain on Planning & Mathematics benchmarks, +1.01 on general reasoning, and up to 2.2x training acceleration over difficulty-based baselines.

## Key Contributions

- Bayesian MI decomposition: expected uncertainty reduction factored into difficulty-dependent and evidence-dependent components — reveals that difficulty-only selection ignores epistemic uncertainty from limited evidence
- Mean belief acquisition score: uses posterior mean of Bayesian latent success rates rather than noisy sampled outcomes, yielding a stable score that extends naturally to multi-rollout settings
- 2.2x training acceleration: achieves strong benchmark gains with significantly fewer training steps vs. difficulty-only baselines (e.g., FADE)
- Theoretical grounding: provides formal justification for why difficulty equates informativeness only under uniform evidence, not in general

## Relevance

Connects to the RL rollout efficiency / allocation thread and the GRPO curriculum thread (FADE, Primacy Bias). InSight's Bayesian framing is more principled than FADE's bilinear timescale separation, addressing the same problem from an information-theoretic angle. TAC (also Nov 8) addresses the multi-domain variant of this problem using gradient transferability; InSight addresses the single-domain data selection problem. Together they provide coverage of the data-efficiency axis of RLVR training.

## My Thoughts

<!-- Add your own notes here -->
