---
title: "Evidence-RL: Towards Evidence-intensive Visual Reasoning"
authors: ["Haojie Huang", "Xinlei Yu", "Chengming Xu"]
date: 2026-09-06
arxiv_id: "2608.08021"
url: "https://arxiv.org/abs/2608.08021"
score: 0.80
topics: [VLM, vision-language, multimodal models, GRPO, reinforcement learning, RL training]
status: unread
---

# Evidence-RL: Towards Evidence-intensive Visual Reasoning

## Summary

Evidence-RL proposes Counterfactual Evidence Disentanglement (CED), a training-time grounding audit that neutralizes object-centric evidence regions in VLM responses and compares the support drop against matched non-evidence regions, rewarding GRPO-trained models for answers that causally depend on the evidence path rather than shortcuts. Using only weak object-level proposals with no question-specific annotation and no inference-time overhead, CED outperforms prior RL-based post-training methods across nine benchmarks and four backbones. CED operationally merges the VIG thread (grounding-density reward) with the CSR thread (counterfactual causal necessity) into a single VLM RL training objective.

## Key Contributions

- Counterfactual Evidence Disentanglement (CED): evidence region neutralization with support-drop comparison against non-evidence regions as GRPO reward signal
- No question-specific evidence annotation required — uses weak object-level proposals only
- Zero inference-time overhead — operates at training time on sampled rollouts
- Validated across nine public benchmarks and four VLM backbones

## Relevance

CED is the VLM-grounding instantiation of CSR (Sep 03): both use counterfactual perturbation at training time to penalize models when outputs don't causally depend on the intended intermediate signal. The key difference is the target: CSR perturbs logical reasoning steps to enforce causal step-necessity; CED perturbs spatial evidence regions to enforce visual grounding. This convergence suggests a unified training principle — "counterfactual causal necessity" — that may apply across all faithfulness failure modes in the five-mode stack, and CED's implementation (object-centric regions + GRPO reward) provides a clean multimodal template for extending this principle to visual reasoning chains.

## My Thoughts

<!-- Add your own notes here -->
