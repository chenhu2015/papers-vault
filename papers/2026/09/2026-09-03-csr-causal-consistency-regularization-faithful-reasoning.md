---
title: "Causal Consistency Regularization: Training Verifiably Sensitive Reasoning in Large Language Models"
authors: ["Sanjeda Akter", "Ibne Farabi Shihab", "Anuj Sharma"]
date: 2026-09-03
arxiv_id: "2509.01544v3"
url: "http://arxiv.org/abs/2509.01544v3"
score: 0.79
topics: [RLHF, reward model, LLM agent, agentic RL, reinforcement learning]
status: unread
---

# Causal Consistency Regularization: Training Verifiably Sensitive Reasoning in Large Language Models

## Summary

CSR proposes Counterfactual Sensitivity Regularization, which enforces causal consistency between intermediate reasoning steps and final answers by automatically generating counterfactual rationales via operator-level interventions (e.g., swapping '+' with '-') and penalizing the model when logically invalid traces still produce the original answer. CSR improves faithfulness by up to 70 percentage points over standard fine-tuning and process supervision across arithmetic, logical deduction, multi-hop QA, and code generation, while adding only ~9% training overhead via a warm-start curriculum and token-subset optimization. The method defines faithfulness using Counterfactual Outcome Sensitivity (COS) and transfers across model families with 94–97% success in structured domains.

## Key Contributions

- Counterfactual Sensitivity Regularization (CSR): automatically generates minimally perturbed counterfactual rationales via operator-level interventions and penalizes invariant model outputs
- Counterfactual Outcome Sensitivity (COS) metric: a new faithfulness measure based on how appropriately model outputs change under logical perturbations (complements accuracy)
- Establishes a new Pareto frontier on accuracy-vs-faithfulness across GSM8K, ProofWriter, HotpotQA, and MBPP
- Only ~9% training overhead via warm-start curriculum and token-subset optimization; complements inference-time self-consistency

## Relevance

Provides a training-level intervention for the bidirectional faithfulness gap identified by FACE-Eval (Sep 01) and REDAgentBench (Sep 02): FACE-Eval showed CoT blind to tool-return information (covert adoption), REDAgentBench showed execution violating verbalized constraints (overt non-compliance). CSR's counterfactual consistency is complementary — it forces intermediate steps to be causally necessary for the output, which would address both failure modes if applied to agentic tool-use training. This directly answers the Sep 02 open question: "can RL training address the bidirectional faithfulness failure at the training level?"

## My Thoughts

<!-- Add your own notes here -->
