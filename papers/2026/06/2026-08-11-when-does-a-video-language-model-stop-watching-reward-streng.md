---
title: "When Does a Video-Language Model Stop Watching? Reward Strength Controls the Formation and Reversal of Visual Shortcuts in Multimodal RLVR"
authors: ["Zekun Xu"]
date: 2026-06-20
arxiv_id: "2606.22043"
url: "https://arxiv.org/abs/2606.22043"
score: 0.77
topics: [multimodal models, vision language models, VLM, RL training]
status: unread
---

# When Does a Video-Language Model Stop Watching? Reward Strength Controls the Formation and Reversal of Visual Shortcuts in Multimodal RLVR

## Summary

Using grounding penalty strength as a control variable in multimodal RLVR, this paper characterizes visual shortcut formation as having a sharp onset over a narrow training window, a monotone dose-response (increasing penalty strength progressively suppresses shortcuts), and a critical intervention window where pre-onset penalty is far more effective than post-consolidation repair. The hysteresis-like asymmetry between acquiring and removing visual shortcuts reframes shortcut collapse as a controllable, time-dependent process rather than a binary defect.

## Key Contributions

- Sharp onset: visual shortcut reliance emerges abruptly over a narrow training window, robust across random seeds — not a gradual drift
- Monotone dose-response: at an intermediate penalty strength, the model first forms then reverses shortcuts, exposing the hysteresis asymmetry
- Critical intervention window: applying grounding penalty before onset arrests formation with high efficiency; the same penalty after consolidation is much less effective
- Practical implication: shortcut prevention requires early monitoring of training dynamics, not just evaluation of final performance

## Relevance

This paper provides the empirical mechanistic complement to ViGOS, VAD, OPPO, and CFPO. Where those papers propose methods to prevent or counteract visual shortcuts, this paper characterizes *when* those interventions must be applied and *why* late intervention fails. The hysteresis finding is particularly relevant to CFPO's design: CFPO applies counterfactual suppression throughout training, which is consistent with the pre-onset prevention strategy validated here. The sharp onset phenomenon also reframes the multimodal shortcut problem for the vault's gap analysis: Gap #7 (visual faithfulness as VLM RL training signal) is not just about the right signal but about the right timing of that signal.

## My Thoughts

<!-- Add your own notes here -->
