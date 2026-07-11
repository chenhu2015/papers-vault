---
title: "Beyond SFT-to-RL: Pre-alignment via Black-Box On-Policy Distillation for Multimodal RL"
authors: ["Sudong Wang", "Weiquan Huang", "Xiaomin Yu", "Zuhao Yang", "Hehai Lin", "Keming Wu", "Chaojun Xiao", "Chen Chen", "Wenxuan Wang", "Beier Zhu", "Yunjian Zhang", "Chengwei Qin"]
date: 2026-07-11
arxiv_id: "2604.28123"
url: "https://arxiv.org/abs/2604.28123"
score: 0.82
topics: [multimodal models, VLM, RLVR, GRPO, vision-language]
status: unread
---

# Beyond SFT-to-RL: Pre-alignment via Black-Box On-Policy Distillation for Multimodal RL

## Summary

PRISM addresses distributional drift between SFT initialization and RLVR in multimodal LLMs by inserting an explicit distribution-alignment stage using black-box on-policy distillation, framed as an adversarial game between the policy and a Mixture-of-Experts discriminator with dedicated perception and reasoning experts. The disentangled corrective signals steer the policy toward the supervision distribution before RLVR begins, without requiring access to teacher logits. Achieves +4.4 and +6.0 points over the SFT-to-RLVR baseline on 4B and 8B Qwen3-VL across GRPO, DAPO, and GSPO.

## Key Contributions

- Identifies distributional drift as a multimodal-specific compounding failure: perception errors and reasoning failures follow distinct drift patterns that amplify each other during subsequent RL
- Distribution-alignment stage via black-box OPD: adversarial game between policy and MoE discriminator provides disentangled perception and reasoning corrective signals without teacher logit access
- 113K high-quality demonstrations curated from Gemini 3 Flash for the alignment stage, featuring dense visual grounding and step-by-step reasoning on the hardest unsolved problems
- Algorithm-agnostic: improvements hold consistently across GRPO, DAPO, and GSPO RL objectives

## Relevance

PRISM is the first multimodal-specific paper in the vault to directly address the pre-RL initialization problem. The text-only vault has covered SFT-to-RL pipeline issues (TEMPO's phase gate, RL-PLUS's hybrid policy) but none addressed the unique drift pattern of multimodal models where perception and reasoning errors interact. PRISM's MoE discriminator with separate perception/reasoning experts is the architectural realization of the disentangled multimodal failure modes identified implicitly in earlier vault papers (Bad Seeing or Bad Thinking, SRPO). This rebalances the vault toward the interest profile's multimodal thread after a text-heavy month.

## My Thoughts

<!-- Add your own notes here -->
