---
title: "Multi-Branch Policy Optimization for Multimodal Large Language Models"
authors: ["Shuai Lyu", "Yuning Gong", "Ruiling Gao", "Xiaoran Shang", "Zhonghong Ou", "Ping Zong", "Yifan Zhu", "Yuan Sun", "Yang Qin", "Peng Hu"]
date: 2026-08-05
arxiv_id: "2608.07581"
url: "https://arxiv.org/abs/2608.07581"
score: 0.82
topics: [multimodal models, vision language models, VLM, agentic RL, RL training]
status: unread
---

# Multi-Branch Policy Optimization for Multimodal Large Language Models

## Summary

MBPO constructs reasoning trees at vision-language decision boundaries, enabling sibling branches to explore diverse visual hypotheses and assigning segment-level credit via branch-relative advantages rather than uniform token-level credit across the response. A temporal replay buffer reuses informative segments while controlling policy staleness, directly addressing progressive advantage degeneration in multimodal RL where uniform credit collapses relative advantages toward zero.

## Key Contributions

- Tree-based framework at vision-language decision boundaries: branch points are explicitly identified where multiple visual interpretations diverge, rather than branching arbitrarily
- Branch-relative advantages for segment-level credit: sibling branches provide a natural counterfactual baseline — the advantage of a segment is computed relative to same-branch alternatives, not the global group mean
- Temporal replay buffer: reuses informative past segments while controlling policy staleness via a staleness penalty, improving sample efficiency without the divergence risk of standard off-policy updates
- Empirical: outperforms representative baselines on multiple multimodal reasoning benchmarks with improved signal quality and optimization efficiency

## Relevance

MBPO extends the vault's multimodal credit assignment problem in a new dimension: where previous work (VAD, OPPO, CFPO) addresses whether visual evidence is faithfully attributed in the teacher correction or reward signal, MBPO addresses where in the reasoning process to branch — specifically at VL decision boundaries. The branch-relative advantage is structurally analogous to Parallel Shapley's path-level credit (branching for counterfactual isolation) but applied at the visual hypothesis level rather than the tool-call level. The temporal replay buffer also connects to IBPO's implicit multi-trajectory credit: both use past trajectory information to enrich credit signals, but MBPO does so via explicit tree structure while IBPO uses divergence between concurrent trajectories.

## My Thoughts

<!-- Add your own notes here -->
