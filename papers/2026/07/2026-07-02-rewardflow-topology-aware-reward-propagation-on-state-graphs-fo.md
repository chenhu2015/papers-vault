---
title: "RewardFlow: Topology-Aware Reward Propagation on State Graphs for Agentic RL with Large Language Models"
authors: ["Xiao Feng", "Bo Han", "Zhanke Zhou", "Jiaqi Fan", "Jiangchao Yao", "Ka Ho Li", "Dahai Yu", "Michael Kwok-Po Ng"]
date: 2026-07-02
arxiv_id: "2603.18859v2"
url: "https://arxiv.org/abs/2603.18859"
score: 0.82
topics: [agentic RL, credit assignment, reward model, GRPO, LLM agent, tool use]
status: unread
---

# RewardFlow: Topology-Aware Reward Propagation on State Graphs for Agentic RL with Large Language Models

## Summary

RewardFlow constructs state graphs from the intrinsic topological structure of agentic trajectories and performs topology-aware propagation to estimate each state's contribution to final success, yielding annotation-free dense process rewards without a learned PRM or manual labeling. The method achieves +6.2% average success rate on text-based agentic benchmarks, +29.7% on visual reasoning over the strongest baseline across three model scales, and +10% accuracy on the DeepResearch benchmark.

## Key Contributions

- State graph construction capturing intrinsic topological structure of trajectory rollouts
- Topology-aware reward propagation estimating each state's contribution to terminal success
- Annotation-free dense process rewards eliminating PRM training, annotation bottlenecks, and reward hacking risk
- +6.2% text agentic, +29.7% visual reasoning, +10% DeepResearch across three model scales

## Relevance

RewardFlow is GraphGPO's (Jun 30) closest structural cousin: both build state-level representations from cross-trajectory graph structure, both estimate per-state value from that topology. The difference is that GraphGPO estimates goal-distance advantage by tracking state reachability across a unified rollout graph, while RewardFlow propagates final success backward through trajectory topology. Together they form a complementary pair: GraphGPO's distance-to-goal estimation is prospective (how far from success?), RewardFlow's propagation is retrospective (how much did this state contribute?). The +29.7% gain on visual reasoning also provides a concrete benchmark for the VLM agentic RL thread.

## My Thoughts

<!-- Add your own notes here -->
