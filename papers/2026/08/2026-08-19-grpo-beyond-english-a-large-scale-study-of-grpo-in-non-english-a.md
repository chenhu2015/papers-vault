---
title: "GRPO Beyond English: A Large-Scale Study of GRPO in Non-English and Multilingual Settings"
authors: ["Konstantin Dobler", "Federico Scozzafava", "Jonathan Janke", "Mohamed Ali"]
date: 2026-08-13
arxiv_id: "2608.13698v1"
url: "https://arxiv.org/abs/2608.13698"
score: 0.75
topics: [GRPO, RL training]
status: unread
---

# GRPO Beyond English: A Large-Scale Study of GRPO in Non-English and Multilingual Settings

## Summary

A large-scale study of GRPO across diverse base models, training languages, and reasoning language rewards finds that native-language RL training nearly matches English-only training, with strong crosslingual transfer where training in one language improves performance in many others. However, language-specific regressions can occur — some languages cause degradation in out-of-domain capabilities for others — revealing that broad multilingual RLVR gains require equally broad multilingual evaluation to detect these regressions.

## Key Contributions

- Large-scale empirical study of GRPO in non-English and multilingual settings across diverse base models
- Finding: native-language GRPO training leaves only a small gap to English-only reasoning performance
- Strong crosslingual transfer: single-language RL training broadly improves other-language performance
- Critical finding: some languages induce severe regressions in out-of-domain capabilities for other languages — model- and language-dependent
- Recommendation: multilingual RLVR requires broad multilingual evaluation to detect language-specific regressions

## Relevance

The vault's GRPO papers (SRGPO, Temporal GRPO, PASS@(k,T)) have all studied GRPO in English reasoning contexts. This is the first systematic study of how GRPO behaves across languages, revealing that the crosslingual transfer dynamics are non-trivial and asymmetric — directly relevant as GRPO becomes a standard RL training recipe in the interest profile.

## My Thoughts

<!-- Add your own notes here -->
