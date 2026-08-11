---
title: "CFPO: Counterfactual Policy Optimization for Multimodal Reasoning"
authors: ["Zhangyuan Yu", "Wanran Sun", "Guangjing Yang", "Xiaohu Wu", "Qicheng Lao"]
date: 2026-06-22
arxiv_id: "2606.23206"
url: "https://arxiv.org/abs/2606.23206"
score: 0.81
topics: [multimodal models, vision language models, VLM, RL training, GRPO]
status: unread
---

# CFPO: Counterfactual Policy Optimization for Multimodal Reasoning

## Summary

CFPO regularizes multimodal RL by maximizing the prediction discrepancy between full visual input and a counterfactual state where critical visual cues are suppressed, enforcing causal consistency between perception and reasoning. The cross-modal counterfactual enhancement integrates as a plug-in with GRPO/DAPO without additional reward models, achieving 3.17–6.25% gains over standard RL baselines and 1.32–2.13% over PAPO on multiple benchmarks.

## Key Contributions

- Cross-modal counterfactual enhancement: a regularization term that maximizes the KL divergence between predictions under full visual input and those under visual-cue-suppressed input, preventing language priors from compensating for ignored visual evidence
- Root-cause framing: addresses both hallucination from language priors (visual bypass at start) and hallucination drift during long CoT (visual shortcut acquisition mid-reasoning)
- Plug-in integration with GRPO/DAPO: no additional reward models, no extra annotation, compatible with standard policy gradient frameworks
- Competitive results: 3.17–6.25% over standard RL, 1.32–2.13% over PAPO (the state-of-the-art perception-aware method at time of writing)

## Relevance

CFPO bridges the CSCR counterfactual credit thread with the multimodal visual grounding thread in a direct and practical way. Where CSCR asks "does the teacher direction change under counterfactual outcome conditioning?" (a data-level diagnostic), CFPO asks "does the policy prediction change under counterfactual visual-cue suppression?" (a training-time regularization). The counterfactual suppression mechanism is structurally parallel to VAD's visual evidence attribution (VAD removes visual evidence from teacher corrections; CFPO removes visual cues from policy inputs) but operates as a training-time adversarial signal rather than a supervision-decomposition tool. The connection to OPPO's masked-input KL is also direct: OPPO masks modality-specific tokens to enforce cross-modal faithfulness; CFPO suppresses critical visual cues to enforce causal grounding.

## My Thoughts

<!-- Add your own notes here -->
