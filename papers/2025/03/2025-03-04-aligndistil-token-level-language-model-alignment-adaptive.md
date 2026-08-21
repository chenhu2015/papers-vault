---
title: "AlignDistil: Token-Level Language Model Alignment as Adaptive Policy Distillation"
authors: ["Songming Zhang", "Xue Zhang", "Tong Zhang", "Bojie Hu", "Yufeng Chen", "Jinan Xu"]
date: 2025-03-04
arxiv_id: "2503.02832"
url: "https://arxiv.org/abs/2503.02832"
score: 0.82
topics: [RLHF, reward model, RLAIF, RL training]
status: unread
---

# AlignDistil: Token-Level Language Model Alignment as Adaptive Policy Distillation

## Summary

AlignDistil proves a formal equivalence between RLHF with DPO-integrated reward and token-level distillation from a teacher that linearly combines DPO and reference model logits, providing a theoretical bridge between RLHF and token-level distillation. A contrastive DPO reward (trained with both normal and reverse DPO models) closes the accuracy gap with pure reward models, and token-adaptive logit extrapolation constructs an appropriate teacher distribution per token to avoid under/over-optimization. Demonstrates superior alignment performance and faster convergence over existing methods.

## Key Contributions

- RLHF ↔ token-level distillation theoretical equivalence: DPO-integrated reward in RLHF objective equals distillation from a teacher combining DPO and reference logits
- Contrastive DPO reward using normal + reverse DPO models to close the accuracy gap with pure reward models
- Token-adaptive logit extrapolation: per-token teacher distribution construction to avoid under/over-optimization
- Superior to existing alignment methods with faster convergence due to token-level distributional reward

## Relevance

AlignDistil provides the theoretical foundation linking RLHF and token-level distillation that the vault's OPD thread has been investigating empirically. The Aug 19 paper "Towards Understanding On-Policy Distillation" showed that OPD gains can be illusory (sampling efficiency, not capability). Today's GC-OPD shows that in long-context settings, teacher-verifier disagreement is the failure mode. AlignDistil explains *why* the two approaches are equivalent under the right conditions — and specifically when they diverge (when the DPO model's reward is inaccurate). The contrastive DPO reward mechanism is a strong candidate for closing the teacher-verifier gap identified by GC-OPD.

## My Thoughts

<!-- Add your own notes here -->
