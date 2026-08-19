---
title: "Towards Understanding On-Policy Distillation through the Lens of Test-Time Scaling"
authors: ["Xinmu Ge", "Zizhuo Zhang", "Yu Huang", "Jianing Zhu"]
date: 2026-08-12
arxiv_id: "2608.11829v1"
url: "https://arxiv.org/abs/2608.11829"
score: 0.72
topics: [RL training, RLAIF]
status: unread
---

# Towards Understanding On-Policy Distillation through the Lens of Test-Time Scaling

## Summary

Analyzing on-policy distillation (OPD) through test-time scaling metrics (pass@K vs avg@K) reveals that OPD-trained models improve sampling efficiency (avg@K) but not the capability boundary (pass@K), which shifts back to the pre-OPD base model as K increases. A problem-level solvability analysis shows OPD causes more problems to become unsolvable than solvable, characterizing OPD as "illusory distillation" whose apparent gains arise from improved sampling efficiency rather than genuinely new reasoning capabilities acquired from the teacher.

## Key Contributions

- pass@K vs avg@K decomposition of OPD gains: OPD improves avg@K (sampling efficiency) not pass@K (capability boundary)
- As K increases, pass@K advantage shifts back to the pre-OPD base model — capability ceiling unchanged or reduced
- Progressive training dynamics: OPD shifts toward strong small-K performance at the expense of large-K boundary
- Problem-level solvability analysis: OPD makes more previously solvable problems unsolvable than previously unsolvable problems solvable
- "Illusory distillation" characterization: OPD gains are sampling efficiency gains, not genuine capability transfer

## Relevance

The Explicit Language Memory paper (Aug 18) showed VQA-paradigm training preserves VLM backbone quality during RL fine-tuning, raising the question of what distillation-style training actually transfers to the student. This paper provides the diagnostic framework for that question: if OPD gains are "illusory" (sampling efficiency only), then any VLA hierarchy using distillation-style training for the high-level VLM component needs to be evaluated via pass@K dynamics, not just avg@K-style aggregate metrics.

## My Thoughts

<!-- Add your own notes here -->
