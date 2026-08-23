---
title: "Copy Less, Ground More: Overcoming Repetitive Copying in Long-Context Reasoning via Evidence-Aware Reinforcement Learning"
authors: ["Lizhe Fang", "Weizhou Shen", "Tianyi Tang", "Yisen Wang"]
date: 2026-07-21
arxiv_id: "2607.19345v2"
url: "http://arxiv.org/abs/2607.19345v2"
score: 0.80
topics: [RL training, RLAIF, agentic RL]
status: unread
---

# Copy Less, Ground More: Overcoming Repetitive Copying in Long-Context Reasoning via Evidence-Aware Reinforcement Learning

## Summary

GEAR identifies repetitive copying of input text as a pervasive, context-length-scaling failure mode in long-context LLM reasoning, traced to insufficient grounding: models that fail to focus on key evidence are far more likely to answer incorrectly. It proposes a reward shaping method augmenting accuracy with a grounding reward (overlap with annotated key evidence) and a distractor penalty (overlap with irrelevant context), plus an automated pipeline to construct evidence-annotated training data from arbitrary documents. GEAR achieves consistent improvements up to +4.6 points over standard accuracy-only RL, with larger gains at longer contexts and reduced reasoning trace length.

## Key Contributions

- Documents repetitive copying as a scaling failure mode: prevalence and severity increase monotonically with context length across frontier long-context LLMs
- Root-cause analysis: separating key evidence from distractor context shows grounding failure is the mechanism — models that copy distractors are more likely to be wrong
- GEAR reward: r_total = r_accuracy + λ_g * r_grounding - λ_d * r_distractor; grounding and distractor terms measured by text overlap with automatically annotated evidence/distractor spans
- Automated evidence-annotation pipeline generalises to arbitrary natural-language documents (no domain-specific annotation required); +4.6 pts average, +reduction in reasoning trace length across multiple model scales

## Relevance

GEAR's evidence-grounding reward is structurally analogous to SSPO's Evidence Anchors design pattern (Aug 22): both use selected evidence segments from the input/environment to shape step-level training signals. GEAR applies this to the reward-shaping level in standard RL (not teacher-student distillation), making it complementary — SSPO uses evidence anchors to distinguish teacher from student steps during OPD, while GEAR uses evidence grounding as a direct RL reward signal for long-context reasoning tasks.

## My Thoughts

<!-- Add your own notes here -->
