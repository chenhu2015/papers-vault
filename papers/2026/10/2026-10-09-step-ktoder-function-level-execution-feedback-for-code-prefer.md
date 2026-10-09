---
title: "Function-Level Execution Feedback for Code Preference Optimization"
authors: ["Idris Nechnech", "Sehwan Kim", "Jimin Seo", "Yeongoon Kim", "Minhae Oh", "Sangwoo Hong", "Jungwoo Lee"]
date: 2026-08-23
arxiv_id: "2608.23632"
url: "https://arxiv.org/abs/2608.23632"
score: 0.75
topics: [agentic RL, RL training, reward model, RLAIF]
status: unread
---

# Function-Level Execution Feedback for Code Preference Optimization

## Summary

STEP-KTODER defines process supervision steps for code as module-level functions in decomposed multi-function programs and assigns binary correctness labels via automatically generated unit tests, avoiding the systematic over-prediction errors of LLM-as-judge labeling. It combines function-level KTO (step-level supervision) with outcome-level KTO on the full program, demonstrating improvements over outcome-only KTO and DPO across HumanEval(+), MBPP(+), BigCodeBench, and LiveCodeBench. Execution-based labels are shown to be critical — LLM judge annotations systematically corrupt positive step labels and degrade downstream preference optimization.

## Key Contributions

- Code-specific step definition: module-level functions as the natural unit of process supervision in decomposed multi-function programs
- Automatic unit test generation for binary step-level correctness labels (execution-verified, no LLM judge)
- Step-wise KTO: combines function-level process supervision with program-level outcome supervision in a unified KTO objective
- Key empirical finding: LLM-as-judge systematically over-predicts function failures, corrupting positive labels and degrading KTO training — execution labels are not just better but necessary

## Relevance

Extends the step-credit thread to code agents via KTO rather than RL (complementing DepGPO's graph-derived execution credit and BoostAPR's learned-credit approach). The function-level step definition is a principled answer to the open question from the BoostAPR thread: how to define credit granularity for code agents without execution-verified training data — here, auto-generated unit tests provide that verification cheaply. The execution > LLM-judge finding reinforces the reliability dimension from the VLM credit thread (SAVOR).

## My Thoughts

<!-- Add your own notes here -->
