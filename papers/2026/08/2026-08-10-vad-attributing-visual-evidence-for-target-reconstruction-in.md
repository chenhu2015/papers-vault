---
title: "VAD: Attributing Visual Evidence for Target Reconstruction in Multimodal On-Policy Distillation"
authors: ["Kangning Zhang", "Yixing Li", "Shuai Shao", "Qingyao Li", "Zhengxi Lu", "Zhiyuan Yao", "Jianghao Lin", "Wenxiang Jiao", "Yuan Lu", "Weiwen Liu", "Weinan Zhang", "Yong Yu"]
date: 2026-08-10
arxiv_id: "2607.28590"
url: "https://arxiv.org/abs/2607.28590"
score: 0.82
topics: [multimodal, vision-language, VLM, RLHF]
status: unread
---

# VAD: Attributing Visual Evidence for Target Reconstruction in Multimodal On-Policy Distillation

## Summary

VAD isolates visually-grounded teacher corrections in multimodal OPD by comparing teacher log-probabilities with visual evidence present vs. removed at each student prefix; the resulting change in centered log-probabilities defines a signed visual evidence proxy direction. Teacher corrections are projected onto this proxy to obtain an intervention-aligned component (primary supervision target) and a proxy-unexplained residual, with the privileged teacher demoted to a weak regularizer. Outperforms direct OPD and visual-advantage weighting across six fine-grained visual benchmarks at 4B and 9B scales.

## Key Contributions

- Counterfactual visual evidence attribution: evaluates teacher log-probabilities with and without visual evidence at each student prefix, yielding a signed visual evidence direction proxy
- Projection-based correction decomposition into intervention-aligned component (visually supported) and proxy-unexplained residual
- Student-anchored target reconstruction from the intervention-aligned component; teacher demoted to weak regularizer
- Token-level analysis showing proxy-aligned component enriched in task-relevant visual corrections, with strongest shifts when evidence refutes a mistaken answer

## Relevance

VAD bridges two active threads in the vault: CSCR's counterfactual robustness framework (applied to RL advantage calibration) and the multimodal OPD shortcut problem (ViGOS, IAPO). While CSCR tests whether the advantage direction changes under outcome condition flipping, VAD tests whether the teacher direction changes under visual evidence removal — both are counterfactual robustness frameworks, but CSCR operates at RL advantage calibration level and VAD at OPD supervision target level. VAD also directly addresses the multimodal OPD shortcut identified by ViGOS: by attributing corrections to visual evidence, it prevents linguistic priors and teacher-specific effects from contaminating the supervision signal.

## My Thoughts

<!-- Add your own notes here -->
