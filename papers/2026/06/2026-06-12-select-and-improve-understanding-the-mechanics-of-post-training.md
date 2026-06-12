---
title: "Select and Improve: Understanding the Mechanics of Post-Training for Reasoning"
authors: ["Akshay Krishnamurthy", "Audrey Huang", "Nived Rajaraman"]
date: 2026-06-11
arxiv_id: "2606.13125v1"
url: "http://arxiv.org/abs/2606.13125v1"
score: 0.80
topics: [RL training, RLHF, reinforcement learning, reward model]
status: unread
---

# Select and Improve: Understanding the Mechanics of Post-Training for Reasoning

## Summary

This paper decomposes RL post-training into two mechanistically distinct processes: strategy selection (the model learns to choose among pre-existing solution strategies) and strategy improvement (the model develops genuinely better strategies). Controlled math reasoning experiments show that SFT data diversity activates strategy selection, while increasing RL task difficulty activates strategy improvement. The mechanistic separation provides practical design principles for continued scaling of reasoning capabilities.

## Key Contributions

- **Two-mechanism decomposition**: strategy selection (choosing from existing strategies) vs strategy improvement (developing new ones) are empirically separable and require different interventions
- **SFT data role clarified**: diverse SFT data is the key driver of strategy selection, not just a warm-start for RL
- **RL difficulty drives improvement**: harder RL tasks push the model to genuinely improve strategies rather than just select better among existing ones
- **Practical interventions**: the separation suggests curriculum design principles — first diversify SFT data, then increase RL difficulty — for continued scaling

## Relevance

Provides a mechanistic complement to RL Excursions (Jun 8, which found RL timing and data composition matter more than scale) and SUPERNOVA (Jun 7, which showed data curation matters for RLVR generalization). The selection/improvement distinction also clarifies what SIRI (Jun 8) and ARISE (today) are doing: skill internalization/library building likely activates strategy selection, while difficulty-scaled rollouts drive strategy improvement.

## My Thoughts

<!-- Add your own notes here -->
