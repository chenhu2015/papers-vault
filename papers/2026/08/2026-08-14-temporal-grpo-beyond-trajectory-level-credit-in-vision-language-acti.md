---
title: "Temporal GRPO: Beyond Trajectory-Level Credit in Vision-Language-Action Reinforcement Learning"
authors: ["Yao Zhou", "Hang Gao", "Fengge Wu"]
date: 2026-08-13
arxiv_id: "2608.13026v1"
url: "http://arxiv.org/abs/2608.13026v1"
score: 0.82
topics: [agentic RL, RL training, GRPO, multimodal models, vision language models]
status: unread
---

# Temporal GRPO: Beyond Trajectory-Level Credit in Vision-Language-Action Reinforcement Learning

## Summary

Temporal GRPO identifies trajectory-level credit aliasing in GRPO-based VLA post-training — a single rollout advantage penalizes correct early-stage actions when the full trajectory fails later. It fixes this by detecting task stages, aligning each rollout with stage-specific action intervals, and computing comparative advantages only across rollouts that have reached the same stage. On RoboTwin 2.0 and LIBERO-Long, stage-aligned advantages improve task success and concentrate improvement at the first diverging stage.

## Key Contributions

- Defines and names **trajectory-level credit aliasing**: the problem where GRPO applies one rollout-level advantage to all actions, including correct early-stage actions in a failing trajectory
- **Stage detection**: constructs detectable task stages from the task structure, aligning rollout prefixes with corresponding stage intervals
- **Stage-specific comparison**: advantages are computed only across rollouts that have entered the same stage, eliminating cross-stage aliasing
- Evaluated on RoboTwin 2.0 and LIBERO-Long; gains are concentrated at the first stage where rollout outcomes diverge, validating the credit aliasing hypothesis

## Relevance

This extends the vault's credit assignment taxonomy to VLA action-level robotics policies — introducing a new segment-level mechanism (stage-aligned credit) that is structurally analogous to SHAPE's solvability-stage segments and MBPO's branch-relative intervals, but applied to robotics VLA action sequences. The stage-only comparison directly addresses the same aliasing problem that trajectory-level credit methods (TACO, DAPR) face, but at a finer granularity defined by the task's observable stage structure rather than tool calls or VL decision points.

## My Thoughts

<!-- Add your own notes here -->
