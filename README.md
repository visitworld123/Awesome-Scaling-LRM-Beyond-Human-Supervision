# Awesome-Scaling-LRM-Beyond-Verifiable-Truths

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths?style=social)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths)
[![GitHub](https://img.shields.io/badge/-github-teal?logo=github)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths)
[![arXiv](https://img.shields.io/badge/Survey-Coming_Soon-b31b1b.svg)](#-citation)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths/pulls)

> **Companion repository** for the survey:
> **Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence**

A curated list of papers, code, and benchmarks on **scaling Large Reasoning Models (LRMs)** when verifiable supervision is scarce or unavailable — covering intrinsic signals, consensus, self-driven learning, LLM/RM verifiers, and reference-consistency rewards.

---

## 📢 News

- **2026-08** Repository reorganized to match the survey taxonomy (verifiable feedback vs. unverifiable reward) and evaluation suites.
- Contributions welcome — open a PR to add new papers under the correct category.

---

## 📖 Introduction

Recent advances in large reasoning models (LRMs) have achieved remarkable success via **reinforcement learning with verifiable rewards (RLVR)** on tasks where outputs can be deterministically checked (e.g., mathematics, code). Scaling LRMs through interaction experience for **general** tasks remains hard, mainly due to:

1. **Scarcity of verifiable data** even in verifiable domains;
2. **Lack of ground-truth verification** in open-ended / unverifiable tasks.

This survey organizes the literature around two core challenges:

| Challenge | Goal | Method families |
|-----------|------|-----------------|
| **Scaling Verifiable Feedback** | Amplify limited verifiable data | Intrinsic certainty · Consensus · Self-driven learning |
| **Scaling Unverifiable Reward** | Train without explicit verification | LLM / reward-model verifiers · Reasoning consistency signals |

This repository tracks papers, code, datasets, and benchmarks aligned with that taxonomy and is updated continuously.

---

## 🗂️ Taxonomy

```text
Scaling Large Reasoning Models
├── Reasoning Models Scaling on Verifiable Tasks
│   Challenge: Scaling Verifiable Feedback / Answer
│   ├── Exploring Intrinsic Certainty
│   ├── Power of Seeking Consensus
│   └── Self-Driven Learning Paradigm
├── Reasoning Models Scaling on Unverifiable Tasks
│   Challenge: Scaling Unverifiable Reward
│   ├── Extra Verifier-based Incentive Signal
│   │   ├── LLM as a Verifier
│   │   └── Reward Model as a Verifier
│   └── Reasoning Consistency-based Incentive Signal
└── Evaluation
    ├── Evaluation on Verifiable Tasks
    └── Evaluation on Unverifiable Tasks
```

---

## 📑 Table of Contents

- [💡 Scaling on Verifiable Tasks](#-large-reasoning-model-scaling-beyond-limited-verifiable-annotation)
  - [Exploring Intrinsic Certainty](#exploring-intrinsic-certainty)
  - [Power of Seeking Consensus](#power-of-seeking-consensus)
  - [Self-Driven Learning Paradigm](#self-driven-learning-paradigm)
- [🛠️ Scaling on Unverifiable Tasks](#️-large-reasoning-model-scaling-beyond-explicit-verifiable-signal)
  - [LLM as a Verifier](#llm-as-a-verifier)
  - [Reward Model as a Verifier](#reward-model-as-a-verifier)
  - [Reasoning Consistency-based Incentive Signal](#reasoning-consistency-based-incentive-signal)
- [📚 Evaluation, Datasets and Benchmarks](#-evaluation-datasets-and-benchmark)
  - [Verifiable Tasks](#evaluation-on-verifiable-tasks)
  - [Unverifiable Tasks](#evaluation-on-unverifiable-tasks)
  - [Judge / Reward Model Benchmarks](#benchmarking-verifiers--reward-models)
- [🤝 Contributing](#-contributing)
- [📜 Citation](#-citation)

---

## 💡 Large Reasoning Model Scaling Beyond Limited Verifiable Annotation

> **Challenge:** *Scaling Verifiable Feedback* — verifiable domains still suffer from limited high-quality labeled data.

### Exploring Intrinsic Certainty

Use model-internal confidence / entropy / self-certainty as the learning signal when ground-truth answers are unavailable at reward time.

- The Unreasonable Effectiveness of Entropy Minimization in LLM Reasoning (EM-RL)
  <a href="https://arxiv.org/pdf/2505.15134?"><img src="https://img.shields.io/badge/arxiv-2505.15134-silver" alt="Paper"></a>
  <a href="https://github.com/shivamag125/EM_PT"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/shivamag125/EM_PT"><img src="https://img.shields.io/github/stars/shivamag125/EM_PT" alt="stars"></a>

- Right Question is Already Half the Answer: Fully Unsupervised LLM Reasoning Incentivization (EMPO)
  <a href="https://arxiv.org/pdf/2504.05812?"><img src="https://img.shields.io/badge/arxiv-2504.05812-silver" alt="Paper"></a>
  <a href="https://github.com/QingyangZhang/EMPO"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/QingyangZhang/EMPO"><img src="https://img.shields.io/github/stars/QingyangZhang/EMPO" alt="stars"></a>
  <a href="https://huggingface.co/collections/qingyangzhang/empo-67f9f7ad7817ebff4b664010"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Maximizing Confidence Alone Improves Reasoning (RENT)
  <a href="https://arxiv.org/pdf/2505.22660?"><img src="https://img.shields.io/badge/arxiv-2505.22660-silver" alt="Paper"></a>
  <a href="https://github.com/satrams/rent-rl"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/satrams/rent-rl"><img src="https://img.shields.io/github/stars/satrams/rent-rl" alt="stars"></a>

- Confidence Is All You Need: Few-Shot RL Fine-Tuning of Language Models (RLSC)
  <a href="https://arxiv.org/pdf/2506.06395?"><img src="https://img.shields.io/badge/arxiv-2506.06395-silver" alt="Paper"></a>

- Learning to Reason without External Rewards (Intuitor)
  <a href="https://arxiv.org/pdf/2505.19590?"><img src="https://img.shields.io/badge/arxiv-2505.19590-silver" alt="Paper"></a>
  <a href="https://github.com/sunblaze-ucb/Intuitor"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sunblaze-ucb/Intuitor"><img src="https://img.shields.io/github/stars/sunblaze-ucb/Intuitor" alt="stars"></a>
  <a href="https://huggingface.co/collections/sunblaze-ucb/intuitor-684f895c78ed2d3ef3a678b3"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- No Free Lunch: Rethinking Internal Feedback for LLM Reasoning
  <a href="https://arxiv.org/pdf/2506.17219?"><img src="https://img.shields.io/badge/arxiv-2506.17219-silver" alt="Paper"></a>

- Shop-R1: Rewarding LLMs to Simulate Human Behavior in Online Shopping via Reinforcement Learning
  <a href="https://arxiv.org/pdf/2507.17842?"><img src="https://img.shields.io/badge/arxiv-2507.17842-silver" alt="Paper"></a>

### Power of Seeking Consensus

Derive pseudo-rewards from agreement across multiple samples, trajectories, or semantically related queries (majority vote, consistency, teacher–student consensus).

- Co-Rewarding: Stable Self-supervised RL for Eliciting Reasoning in Large Language Models
  <a href="https://arxiv.org/pdf/2508.00410?"><img src="https://img.shields.io/badge/arxiv-2508.00410-silver" alt="Paper"></a>

- TTRL: Test-Time Reinforcement Learning
  <a href="https://arxiv.org/pdf/2504.16084?"><img src="https://img.shields.io/badge/arxiv-2504.16084-silver" alt="Paper"></a>

- Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO (MM-UPT)
  <a href="https://arxiv.org/pdf/2505.22453?"><img src="https://img.shields.io/badge/arxiv-2505.22453-silver" alt="Paper"></a>

- Consistent Paths Lead to Truth: Self-Rewarding Reinforcement Learning for LLM Reasoning (CoVo)
  <a href="https://arxiv.org/pdf/2506.08745?"><img src="https://img.shields.io/badge/arxiv-2506.08745-silver" alt="Paper"></a>

- ETTRL: Balancing Exploration and Exploitation in LLM Test-Time Reinforcement Learning Via Entropy Mechanism
  <a href="https://arxiv.org/pdf/2508.11356?"><img src="https://img.shields.io/badge/arxiv-2508.11356-silver" alt="Paper"></a>

- Can Large Reasoning Models Self-Train?
  <a href="https://arxiv.org/pdf/2505.21444?"><img src="https://img.shields.io/badge/arxiv-2505.21444-silver" alt="Paper"></a>

- ZeroGUI: Automating Online GUI Learning at Zero Human Cost
  <a href="https://arxiv.org/pdf/2505.23762?"><img src="https://img.shields.io/badge/arxiv-2505.23762-silver" alt="Paper"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/github/stars/OpenGVLab/ZeroGUI" alt="stars"></a>
  <a href="https://huggingface.co/collections/OpenGVLab/zerogui-68388cb7dbf608133c4b5fb2"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

### Self-Driven Learning Paradigm

Models generate their own tasks, curricula, or training data (self-play, self-instruct, absolute-zero style loops) to reduce dependence on human-annotated verifiable examples.

- SeRL: Self-Play Reinforcement Learning for Large Language Models with Limited Data
  <a href="https://arxiv.org/pdf/2505.20347?"><img src="https://img.shields.io/badge/arxiv-2505.20347-silver" alt="Paper"></a>

- ZeroGUI: Automating Online GUI Learning at Zero Human Cost
  <a href="https://arxiv.org/pdf/2505.23762?"><img src="https://img.shields.io/badge/arxiv-2505.23762-silver" alt="Paper"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/github/stars/OpenGVLab/ZeroGUI" alt="stars"></a>

- CoT-Self-Instruct: Building High-Quality Synthetic Prompts for Reasoning and Non-Reasoning Tasks
  <a href="https://arxiv.org/pdf/2507.23751?"><img src="https://img.shields.io/badge/arxiv-2507.23751-silver" alt="Paper"></a>

- Beyond the Trade-off: Self-Supervised Reinforcement Learning for Reasoning Models' Instruction Following
  <a href="https://arxiv.org/pdf/2508.02150?"><img src="https://img.shields.io/badge/arxiv-2508.02150-silver" alt="Paper"></a>

- Self-Questioning Language Models (SQLM)
  <a href="https://arxiv.org/pdf/2508.03682?"><img src="https://img.shields.io/badge/arxiv-2508.03682-silver" alt="Paper"></a>

- Absolute Zero: Reinforced Self-Play Reasoning with Zero Data (AZR)
  <a href="https://arxiv.org/pdf/2505.03335?"><img src="https://img.shields.io/badge/arxiv-2505.03335-silver" alt="Paper"></a>

- R-Zero: Self-Evolving Reasoning LLM from Zero Data
  <a href="https://arxiv.org/pdf/2508.05004?"><img src="https://img.shields.io/badge/arxiv-2508.05004-silver" alt="Paper"></a>

- Co-Evolving LLM Coder and Unit Tester via Reinforcement Learning (CURE)
  <a href="https://arxiv.org/pdf/2506.03136?"><img src="https://img.shields.io/badge/arxiv-2506.03136-silver" alt="Paper"></a>

- Language Self-Play For Data-Free Training (LSP)
  <a href="https://arxiv.org/pdf/2412.16720?"><img src="https://img.shields.io/badge/arxiv-2412.16720-silver" alt="Paper"></a>

---

## 🛠️ Large Reasoning Model Scaling Beyond Explicit Verifiable Signal

> **Challenge:** *Scaling Unverifiable Reward* — open-ended tasks lack deterministic checkers.

### Extra Verifier Provide Incentive Signal

#### LLM as a Verifier

Use an LLM (or VLM) as judge / rubric / checklist scorer to provide training rewards.

- Crossing the Reward Bridge: Expanding RL with Verifiable Rewards Across Diverse Domains
  <a href="https://arxiv.org/pdf/2503.23829?"><img src="https://img.shields.io/badge/arxiv-2503.23829-silver" alt="Paper"></a>
  <a href="https://huggingface.co/collections/virtuoussy/rlvr-67ea349b086e3511f86d1c1f"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Continuous Self-Improvement of Large Language Models by Test-time Training with Verifier-Driven Sample Selection (VDS-TTT)
  <a href="https://arxiv.org/pdf/2505.19475?"><img src="https://img.shields.io/badge/arxiv-2505.19475-silver" alt="Paper"></a>

- SSR-Zero: Simple Self-Rewarding Reinforcement Learning for Machine Translation
  <a href="https://arxiv.org/pdf/2505.16637?"><img src="https://img.shields.io/badge/arxiv-2505.16637-silver" alt="Paper"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/github/stars/Kelaxon/SSR-Zero" alt="stars"></a>
  <a href="https://huggingface.co/collections/wjyccs/ssr-zero-6830189a8d2fd6fc7ce6fba6"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- ZeroGUI: Automating Online GUI Learning at Zero Human Cost
  <a href="https://arxiv.org/pdf/2505.23762?"><img src="https://img.shields.io/badge/arxiv-2505.23762-silver" alt="Paper"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenGVLab/ZeroGUI"><img src="https://img.shields.io/github/stars/OpenGVLab/ZeroGUI" alt="stars"></a>

- Omni-Thinker: Scaling Cross-Domain Generalization in LLMs via Multi-Task RL with Hybrid Rewards
  <a href="https://arxiv.org/pdf/2507.14783?"><img src="https://img.shields.io/badge/arxiv-2507.14783-silver" alt="Paper"></a>

- Learning to Reason for Factuality
  <a href="https://arxiv.org/pdf/2508.05618?"><img src="https://img.shields.io/badge/arxiv-2508.05618-silver" alt="Paper"></a>

- Checklists Are Better Than Reward Models for Aligning Language Models (RLCF)
  <a href="https://arxiv.org/pdf/2507.18624?"><img src="https://img.shields.io/badge/arxiv-2507.18624-silver" alt="Paper"></a>

- Rubrics as Rewards: Reinforcement Learning Beyond Verifiable Domains (RaR)
  <a href="https://arxiv.org/pdf/2507.17746?"><img src="https://img.shields.io/badge/arxiv-2507.17746-silver" alt="Paper"></a>

- Reinforcement Learning with Rubric Anchors (Rubicon)
  <a href="https://arxiv.org/pdf/2508.12790?"><img src="https://img.shields.io/badge/arxiv-2508.12790-silver" alt="Paper"></a>

- Breaking the Exploration Bottleneck: Rubric-Scaffolded Reinforcement Learning for General LLM Reasoning (RuscaRL)
  <a href="https://arxiv.org/pdf/2508.16949?"><img src="https://img.shields.io/badge/arxiv-2508.16949-silver" alt="Paper"></a>

- Kimi K2: Open Agentic Intelligence
  <a href="https://arxiv.org/pdf/2507.20534?"><img src="https://img.shields.io/badge/arxiv-2507.20534-silver" alt="Paper"></a>

- Baichuan-M2: Scaling Medical Capability with Large Verifier System
  <a href="https://arxiv.org/pdf/2509.02208?"><img src="https://img.shields.io/badge/arxiv-2509.02208-silver" alt="Paper"></a>

#### Reward Model as a Verifier

Train or apply specialized (generative / discriminative / process) reward models as the incentive signal.

- Seed1.5-Thinking: Advancing Superb Reasoning Models with Reinforcement Learning
  <a href="https://arxiv.org/pdf/2504.13914?"><img src="https://img.shields.io/badge/arxiv-2504.13914-silver" alt="Paper"></a>

- General-Reasoner: Advancing LLM Reasoning Across All Domains
  <a href="https://arxiv.org/pdf/2505.14652?"><img src="https://img.shields.io/badge/arxiv-2505.14652-silver" alt="Paper"></a>
  <a href="https://github.com/TIGER-AI-Lab/General-Reasoner"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/TIGER-AI-Lab/General-Reasoner"><img src="https://img.shields.io/github/stars/TIGER-AI-Lab/General-Reasoner" alt="stars"></a>
  <a href="https://huggingface.co/collections/TIGER-Lab/general-reasoner-67fe9386e43e046489eac013"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Crossing the Reward Bridge: Expanding RL with Verifiable Rewards Across Diverse Domains
  <a href="https://arxiv.org/pdf/2503.23829?"><img src="https://img.shields.io/badge/arxiv-2503.23829-silver" alt="Paper"></a>
  <a href="https://huggingface.co/collections/virtuoussy/rlvr-67ea349b086e3511f86d1c1f"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- StructVRM: Aligning Multimodal Reasoning with Structured and Verifiable Reward Models
  <a href="https://arxiv.org/pdf/2508.05383?"><img src="https://img.shields.io/badge/arxiv-2508.05383-silver" alt="Paper"></a>

- Inference-Time Scaling for Generalist Reward Modeling (SPCT)
  <a href="https://arxiv.org/pdf/2504.02495?"><img src="https://img.shields.io/badge/arxiv-2504.02495-silver" alt="Paper"></a>

- Writing-Zero: Bridge the Gap Between Non-verifiable Problems and Verifiable Rewards
  <a href="https://arxiv.org/pdf/2506.00103?"><img src="https://img.shields.io/badge/arxiv-2506.00103-silver" alt="Paper"></a>

- Pre-Trained Policy Discriminators are General Reward Models (POLAR)
  <a href="https://arxiv.org/pdf/2507.05197?"><img src="https://img.shields.io/badge/arxiv-2507.05197-silver" alt="Paper"></a>
  <a href="https://github.com/InternLM/POLAR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/InternLM/POLAR"><img src="https://img.shields.io/github/stars/InternLM/POLAR" alt="stars"></a>
  <a href="https://huggingface.co/collections/internlm/polar-68693f829d2e83ac5e6e124a"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Beyond the Trade-off: Self-Supervised Reinforcement Learning for Reasoning Models' Instruction Following
  <a href="https://arxiv.org/pdf/2508.02150?"><img src="https://img.shields.io/badge/arxiv-2508.02150-silver" alt="Paper"></a>

- EvolvR: Self-Evolving Pairwise Reasoning for Story Evaluation to Enhance Generation
  <a href="https://arxiv.org/pdf/2508.06046?"><img src="https://img.shields.io/badge/arxiv-2508.06046-silver" alt="Paper"></a>

- SEAgent: Self-Evolving Computer Use Agent with Autonomous Learning from Experience
  <a href="https://arxiv.org/pdf/2508.04700?"><img src="https://img.shields.io/badge/arxiv-2508.04700-silver" alt="Paper"></a>

- Posterior-GRPO: Rewarding Reasoning Processes in Code Generation
  <a href="https://arxiv.org/pdf/2508.05170?"><img src="https://img.shields.io/badge/arxiv-2508.05170-silver" alt="Paper"></a>

- ReasonFlux-PRM: Trajectory-Aware PRMs for Long Chain-of-Thought Reasoning in LLMs
  <a href="https://arxiv.org/pdf/2506.18896?"><img src="https://img.shields.io/badge/arxiv-2506.18896-silver" alt="Paper"></a>
  <a href="https://github.com/Gen-Verse/ReasonFlux"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Gen-Verse/ReasonFlux"><img src="https://img.shields.io/github/stars/Gen-Verse/ReasonFlux" alt="stars"></a>
  <a href="https://huggingface.co/collections/Gen-Verse/reasonflux-coder-6833109ed9300c62deb32c6b"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

### Reasoning Consistency-based Incentive Signal

Use reference answers (or latent rationales) as *implicit* incentives — likelihood, perplexity, ELBO / variational objectives — without an external verifier at reward time.

- Reinforcing General Reasoning without Verifiers (VeriFree)
  <a href="https://arxiv.org/pdf/2505.21493?"><img src="https://img.shields.io/badge/arxiv-2505.21493-silver" alt="Paper"></a>
  <a href="https://github.com/sail-sg/VeriFree"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/sail-sg/VeriFree"><img src="https://img.shields.io/github/stars/sail-sg/VeriFree" alt="stars"></a>
  <a href="https://huggingface.co/collections/zhouxiangxin/verifree-685a1e9509d0db2ed9731c62"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Beyond Verifiable Rewards: Scaling Reinforcement Learning for Language Models to Unverifiable Data (JEPO)
  <a href="https://arxiv.org/pdf/2503.19618?"><img src="https://img.shields.io/badge/arxiv-2503.19618-silver" alt="Paper"></a>

- Language Models Are Hidden Reasoners: Unlocking Latent Reasoning Capabilities via Self-Rewarding (LaTRO)
  <a href="https://arxiv.org/pdf/2411.04282?"><img src="https://img.shields.io/badge/arxiv-2411.04282-silver" alt="Paper"></a>
  <a href="https://github.com/SalesforceAIResearch/LaTRO"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/SalesforceAIResearch/LaTRO"><img src="https://img.shields.io/github/stars/SalesforceAIResearch/LaTRO" alt="stars"></a>

- Direct Reasoning Optimization: LLMs Can Reward and Refine Their Own Reasoning for Open-Ended Tasks (DRO)
  <a href="https://arxiv.org/pdf/2506.13351?"><img src="https://img.shields.io/badge/arxiv-2506.13351-silver" alt="Paper"></a>

- RLPR: Extrapolating RLVR to General Domains without Verifiers
  <a href="https://arxiv.org/pdf/2506.18254?"><img src="https://img.shields.io/badge/arxiv-2506.18254-silver" alt="Paper"></a>
  <a href="https://github.com/OpenBMB/RLPR"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/OpenBMB/RLPR"><img src="https://img.shields.io/github/stars/OpenBMB/RLPR" alt="stars"></a>

- NOVER: Incentive Training for Language Models via Verifier-Free Reinforcement Learning
  <a href="https://arxiv.org/pdf/2505.16022?"><img src="https://img.shields.io/badge/arxiv-2505.16022-silver" alt="Paper"></a>
  <a href="https://github.com/thinkwee/NOVER"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/thinkwee/NOVER"><img src="https://img.shields.io/github/stars/thinkwee/NOVER" alt="stars"></a>
  <a href="https://huggingface.co/collections/thinkwee/novereason-68937ca75331dfaddaf24016"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Learning to Reason for Long-Form Story Generation (VR-CLI)
  <a href="https://arxiv.org/pdf/2503.22828?"><img src="https://img.shields.io/badge/arxiv-2503.22828-silver" alt="Paper"></a>
  <a href="https://github.com/Alex-Gurung/ReasoningNCP"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Alex-Gurung/ReasoningNCP"><img src="https://img.shields.io/github/stars/Alex-Gurung/ReasoningNCP" alt="stars"></a>

- SSR-Zero: Simple Self-Rewarding Reinforcement Learning for Machine Translation
  <a href="https://arxiv.org/pdf/2505.16637?"><img src="https://img.shields.io/badge/arxiv-2505.16637-silver" alt="Paper"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Kelaxon/SSR-Zero"><img src="https://img.shields.io/github/stars/Kelaxon/SSR-Zero" alt="stars"></a>

---

## 📚 Evaluation, Datasets and Benchmark

### Evaluation on Verifiable Tasks

#### Mathematical Reasoning

- GSM8K <a href="https://arxiv.org/pdf/2110.14168?"><img src="https://img.shields.io/badge/arxiv-2110.14168-silver" alt="Paper"></a>
- MATH / MATH500 <a href="https://arxiv.org/pdf/2305.20050?"><img src="https://img.shields.io/badge/arxiv-2305.20050-silver" alt="Paper"></a>
- LiveMathBench <a href="https://arxiv.org/pdf/2412.13147?"><img src="https://img.shields.io/badge/arxiv-2412.13147-silver" alt="Paper"></a>
- NuminaMath / AMC <a href="https://arxiv.org/pdf/2410.01271?"><img src="https://img.shields.io/badge/arxiv-2410.01271-silver" alt="Paper"></a>
- AIME 2024 / AIME 2025
- RandomCalculation <a href="https://arxiv.org/pdf/2507.10532?"><img src="https://img.shields.io/badge/arxiv-2507.10532-silver" alt="Paper"></a>

#### Code Generation

- MBPP <a href="https://arxiv.org/pdf/2108.07732?"><img src="https://img.shields.io/badge/arxiv-2108.07732-silver" alt="Paper"></a>
- LiveCodeBench <a href="https://arxiv.org/pdf/2403.07974?"><img src="https://img.shields.io/badge/arxiv-2403.07974-silver" alt="Paper"></a>
- CRUXEval <a href="https://arxiv.org/pdf/2401.03065?"><img src="https://img.shields.io/badge/arxiv-2401.03065-silver" alt="Paper"></a>
- HumanEval <a href="https://arxiv.org/pdf/2107.03374?"><img src="https://img.shields.io/badge/arxiv-2107.03374-silver" alt="Paper"></a>
- CodeContests <a href="https://arxiv.org/pdf/2203.07814?"><img src="https://img.shields.io/badge/arxiv-2203.07814-silver" alt="Paper"></a>
- MHPP <a href="https://arxiv.org/pdf/2405.11430?"><img src="https://img.shields.io/badge/arxiv-2405.11430-silver" alt="Paper"></a>
- CodeElo <a href="https://arxiv.org/pdf/2501.01257?"><img src="https://img.shields.io/badge/arxiv-2501.01257-silver" alt="Paper"></a>

#### Logical Puzzles or Games

- ZebraLogic <a href="https://arxiv.org/pdf/2502.01100?"><img src="https://img.shields.io/badge/arxiv-2502.01100-silver" alt="Paper"></a>
- AutoLogi <a href="https://arxiv.org/pdf/2502.16906?"><img src="https://img.shields.io/badge/arxiv-2502.16906-silver" alt="Paper"></a>
- Sudoku-Bench <a href="https://arxiv.org/pdf/2505.16135?"><img src="https://img.shields.io/badge/arxiv-2505.16135-silver" alt="Paper"></a>

#### Multi-choice Evaluation

- AQuA <a href="https://arxiv.org/pdf/1705.04146?"><img src="https://img.shields.io/badge/arxiv-1705.04146-silver" alt="Paper"></a>
- CodeMMLU
- LogiQA <a href="https://arxiv.org/pdf/2007.08124?"><img src="https://img.shields.io/badge/arxiv-2007.08124-silver" alt="Paper"></a>

### Evaluation on Unverifiable Tasks

#### Multi-task QA

- GPQA <a href="https://arxiv.org/pdf/2311.12022?"><img src="https://img.shields.io/badge/arxiv-2311.12022-silver" alt="Paper"></a>
- Humanity's Last Exam (HLE) <a href="https://arxiv.org/pdf/2501.14249?"><img src="https://img.shields.io/badge/arxiv-2501.14249-silver" alt="Paper"></a>
- MMLU <a href="https://arxiv.org/pdf/2009.03300?"><img src="https://img.shields.io/badge/arxiv-2009.03300-silver" alt="Paper"></a>
- MMLU-Pro <a href="https://arxiv.org/pdf/2406.01574?"><img src="https://img.shields.io/badge/arxiv-2406.01574-silver" alt="Paper"></a>

#### Specific Domain QA

**Commonsense**

- CommonsenseQA <a href="https://arxiv.org/pdf/1811.00937?"><img src="https://img.shields.io/badge/arxiv-1811.00937-silver" alt="Paper"></a>
- CHARM / CHARM-style Chinese commonsense suites

**Medical**

- MedQA <a href="https://arxiv.org/pdf/2009.13081?"><img src="https://img.shields.io/badge/arxiv-2009.13081-silver" alt="Paper"></a>
- MedBullets / JAMA clinical QA
- MedXpertQA <a href="https://arxiv.org/pdf/2501.18362?"><img src="https://img.shields.io/badge/arxiv-2501.18362-silver" alt="Paper"></a>

**Finance**

- FinanceQA <a href="https://arxiv.org/pdf/2501.18062?"><img src="https://img.shields.io/badge/arxiv-2501.18062-silver" alt="Paper"></a>
- FinTextQA
- FinBen / FinanceBench

**Law**

- LawBench
- LexEval
- LegalBench
- LEXam <a href="https://arxiv.org/pdf/2505.12864?"><img src="https://img.shields.io/badge/arxiv-2505.12864-silver" alt="Paper"></a>

#### Open-ended Generation

- LitBench
- CS4
- SS-GEN
- AlpacaEval
- IFEval <a href="https://arxiv.org/pdf/2311.07911?"><img src="https://img.shields.io/badge/arxiv-2311.07911-silver" alt="Paper"></a>
- MT-Bench <a href="https://arxiv.org/pdf/2306.05685?"><img src="https://img.shields.io/badge/arxiv-2306.05685-silver" alt="Paper"></a>

#### Social Intelligence

- EQ-Bench
- ToMBench
- EgoSocialArena
- SocialEval

### Benchmarking Verifiers & Reward Models

#### Benchmarking on LLM as a Verifier

- MLLM-as-a-Judge: Assessing Multimodal LLM-as-a-Judge with Vision-Language Benchmark
  <a href="https://arxiv.org/pdf/2402.04788?"><img src="https://img.shields.io/badge/arxiv-2402.04788-silver" alt="Paper"></a>
  <a href="https://github.com/Dongping-Chen/MLLM-Judge"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Dongping-Chen/MLLM-Judge"><img src="https://img.shields.io/github/stars/Dongping-Chen/MLLM-Judge" alt="stars"></a>
  <a href="https://huggingface.co/datasets/ONE-Lab/MLLM-as-a-Judge"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Judging the Judges: A Systematic Study of Position Bias in LLM-as-a-Judge
  <a href="https://arxiv.org/pdf/2406.07791?"><img src="https://img.shields.io/badge/arxiv-2406.07791-silver" alt="Paper"></a>

- JudgeBench: A Benchmark for Evaluating LLM-based Judges
  <a href="https://arxiv.org/pdf/2410.12784?"><img src="https://img.shields.io/badge/arxiv-2410.12784-silver" alt="Paper"></a>
  <a href="https://github.com/ScalerLab/JudgeBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/ScalerLab/JudgeBench"><img src="https://img.shields.io/github/stars/ScalerLab/JudgeBench" alt="stars"></a>
  <a href="https://huggingface.co/datasets/ScalerLab/JudgeBench"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Evaluating Judges as Evaluators: The JETTS Benchmark of LLM-as-Judges as Test-Time Scaling Evaluators
  <a href="https://arxiv.org/pdf/2504.15253?"><img src="https://img.shields.io/badge/arxiv-2504.15253-silver" alt="Paper"></a>
  <a href="https://github.com/SalesforceAIResearch/jetts-benchmark"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/SalesforceAIResearch/jetts-benchmark"><img src="https://img.shields.io/github/stars/SalesforceAIResearch/jetts-benchmark" alt="stars"></a>

- CodeJudgeBench: Benchmarking LLM-as-a-Judge for Coding Tasks
  <a href="https://arxiv.org/pdf/2507.10535?"><img src="https://img.shields.io/badge/arxiv-2507.10535-silver" alt="Paper"></a>
  <a href="https://github.com/hongcha0/CodeJudgeBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/hongcha0/CodeJudgeBench"><img src="https://img.shields.io/github/stars/hongcha0/CodeJudgeBench" alt="stars"></a>
  <a href="https://huggingface.co/datasets/mattymchen/codejudgebench"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

#### Benchmarking on Reward Model as a Verifier

- RewardBench: Evaluating Reward Models for Language Modeling
  <a href="https://arxiv.org/pdf/2403.13787?"><img src="https://img.shields.io/badge/arxiv-2403.13787-silver" alt="Paper"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/github/stars/allenai/reward-bench" alt="stars"></a>
  <a href="https://huggingface.co/datasets/allenai/reward-bench"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- RM-Bench: Benchmarking Reward Models of Language Models with Subtlety and Style
  <a href="https://arxiv.org/pdf/2410.16184?"><img src="https://img.shields.io/badge/arxiv-2410.16184-silver" alt="Paper"></a>
  <a href="https://github.com/THU-KEG/RM-Bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/THU-KEG/RM-Bench"><img src="https://img.shields.io/github/stars/THU-KEG/RM-Bench" alt="stars"></a>
  <a href="https://huggingface.co/datasets/THU-KEG/RM-Bench"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- ViLBench: A Suite for Vision-Language Process Reward Modeling
  <a href="https://arxiv.org/pdf/2503.20271?"><img src="https://img.shields.io/badge/arxiv-2503.20271-silver" alt="Paper"></a>
  <a href="https://huggingface.co/datasets/UCSC-VLAA/ViLBench"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- Socratic-PRMBench: Benchmarking Process Reward Models with Systematic Reasoning Patterns
  <a href="https://arxiv.org/pdf/2505.23474?"><img src="https://img.shields.io/badge/arxiv-2505.23474-silver" alt="Paper"></a>
  <a href="https://github.com/Xiang-Li-oss/Socratic-PRMBench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/Xiang-Li-oss/Socratic-PRMBench"><img src="https://img.shields.io/github/stars/Xiang-Li-oss/Socratic-PRMBench" alt="stars"></a>

- RewardBench 2: Advancing Reward Model Evaluation
  <a href="https://arxiv.org/pdf/2506.01937?"><img src="https://img.shields.io/badge/arxiv-2506.01937-silver" alt="Paper"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/allenai/reward-bench"><img src="https://img.shields.io/github/stars/allenai/reward-bench" alt="stars"></a>
  <a href="https://huggingface.co/datasets/allenai/reward-bench-2"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

- RewardAnything: Generalizable Principle-Following Reward Models
  <a href="https://arxiv.org/pdf/2506.03637?"><img src="https://img.shields.io/badge/arxiv-2506.03637-silver" alt="Paper"></a>
  <a href="https://github.com/WisdomShell/RewardAnything"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/WisdomShell/RewardAnything"><img src="https://img.shields.io/github/stars/WisdomShell/RewardAnything" alt="stars"></a>
  <a href="https://huggingface.co/WisdomShell/RewardAnything-8B-v1"><img src="https://img.shields.io/badge/huggingface-yellow"></a>

---

## 🤝 Contributing

Pull requests are welcome. Please:

1. Place the paper under the **correct taxonomy node** (Intrinsic / Consensus / Self-Driven / LLM Verifier / RM Verifier / Consistency / Evaluation).
2. Prefer the badge format used above (`arxiv` / `github` / `huggingface`).
3. Briefly note why the work belongs in that category in the PR description.

---

## 📜 Citation

If you find this repository or our survey helpful, please consider citing:

```bibtex
@article{yang2026scaling,
  title   = {Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence},
  author  = {Yang, Zhiqin and Fu, Jingwen and Liu, Yuhan and Liu, Hengyu and Zhang, Yonggang and Cao, Kainan and Zhang, Zizhuo and Li, Chenxin and Yuan, Ruibin and Pan, Jiahao and Sun, Jiankai and Lin, Yunlong and Zhang, Zhenyuan and Xiong, Jing and Li, Yibo and Lin, Sida and Xue, Wei and Han, Bo and Guo, Yike},
  year    = {2026},
  note    = {Survey; companion repository: https://github.com/visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths}
}
```

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths&type=Date)](https://star-history.com/#visitworld123/Awesome-Scaling-LRM-Beyond-Verifiable-Truths&Date)
