---
title: "The Hidden Bias of Process Reward Models: PRISM for Rewarding the Right Reasoning"
authors: ["Aakriti Agrawal", "Souradip Chakraborty", "Armin Saghafian", "Nihal Sharma", "Rizal Fathony", "Nam H Nguyen", "C. Bayan Bruss", "Amrit Singh Bedi", "Furong Huang"]
date: 2026-06-13
arxiv_id: "2606.09078"
url: "https://arxiv.org/abs/2606.09078"
score: 0.83
topics: [reward model, RLHF, agentic RL]
status: unread
---

# The Hidden Bias of Process Reward Models: PRISM for Rewarding the Right Reasoning

## Summary

PRMs trained on step-level reasoning data suffer from severe class imbalance causing standard cross-entropy to amplify a hidden bias, overcrediting plausible but wrong intermediate steps at high false-positive rates. PRISM shows that false positives are asymmetrically more harmful than false negatives in reasoning guidance, and proposes a bias-aware training objective that recalibrates step-level rewards to reduce false positives on math reasoning benchmarks.

## Key Contributions

- Diagnoses step-level data imbalance as a structural PRM training flaw: correct steps vastly outnumber incorrect steps, causing CE to amplify overcrediting of wrong steps
- Establishes FP asymmetry theorem: false positives (wrong steps scored high) degrade tree-search reasoning more severely than false negatives
- PRISM: bias-corrected training objective that recalibrates step-level reward estimates toward reduced FP rate
- Empirical improvements in PRM-guided math reasoning search quality

## Relevance

Directly extends the process reward and credit assignment thread: RREDCoT (Jun 8) addressed step-level *segmentation*, 3SPO (Jun 11) addressed step-level *advantage estimation*, and PRISM now addresses the *training data bias* that corrupts step-level labels before they ever reach the model — a complementary layer in the credit quality stack.

## My Thoughts

<!-- Add your own notes here -->
