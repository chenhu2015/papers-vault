---
title: "When In-Distribution Gains Fail: Evaluating Weak-to-Strong Reward Models under Preference Shift"
authors: ["Khoi Le", "Tri Cao", "Phong Nguyen", "Cong-Duy Nguyen", "Anh Tuan Luu", "Miao Chunyan", "See-Kiong Ng", "Thong Nguyen"]
date: 2026-05-25
arxiv_id: "2605.25629"
url: "http://arxiv.org/abs/2605.25629v2"
score: 0.82
topics: [RLHF, reward model, RL training]
status: unread
---

# When In-Distribution Gains Fail: Evaluating Weak-to-Strong Reward Models under Preference Shift

## Summary

W2S preference learning is shown to fail under zero-shot distribution shift, revealing a representational failure mode where weak-supervised fine-tuning pulls strong models toward source-domain features rather than broadly transferable preference representations. Representation Anchoring (Anchor) constrains excessive drift from the pretrained strong model's representation space during fine-tuning, consistently improving out-of-distribution reward model transfer across preference domains, datasets, and model families.

## Key Contributions

- Zero-shot distribution shift evaluation protocol and transfer-aware metrics for W2S preference learning
- Representational failure mode identified: weak supervision pulls strong model toward source-domain features
- Representation Anchoring (Anchor): simple regularizer preventing excessive drift from pretrained representation space
- Consistent OOD transfer improvement while maintaining competitive in-distribution performance

## Relevance

Directly addresses the reward model OOD/overoptimization thread — a 3-day carry-forward — specifically from the weak-to-strong generalization angle; the failure mode identified here is practically important for scalable oversight.

## My Thoughts

<!-- Add your own notes here -->
