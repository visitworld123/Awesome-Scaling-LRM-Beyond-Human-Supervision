# Contributing

Thanks for helping keep this list up to date with the survey
**Scaling Large Reasoning Models beyond Human Supervision: A Path toward Superintelligence**.

## Add a paper

1. Open a PR that edits `README.md` only (unless you are also fixing links/typos elsewhere).
2. Insert the entry under the **correct taxonomy section**:
   - Intrinsic Certainty
   - Seeking Consensus
   - Self-Driven Learning
   - LLM as a Verifier
   - Reward Model as a Verifier
   - Reasoning Consistency-based Incentive
   - Evaluation / Benchmarks
3. Prefer this badge format:

```markdown
- Paper Title (ShortName)
  <a href="https://arxiv.org/pdf/XXXX.XXXXX?"><img src="https://img.shields.io/badge/arxiv-XXXX.XXXXX-silver" alt="Paper"></a>
  <a href="https://github.com/org/repo"><img src="https://img.shields.io/badge/-github-teal?logo=github" alt="github"></a>
  <a href="https://github.com/org/repo"><img src="https://img.shields.io/github/stars/org/repo" alt="stars"></a>
  <a href="https://huggingface.co/..."><img src="https://img.shields.io/badge/huggingface-yellow"></a>
```

4. In the PR description, one sentence on **why** the paper belongs in that category.

## Scope

In-scope: methods that scale LRMs when verifiable labels / checkers are limited or absent.

Out-of-scope: generic LLM surveys without a clear link to verifiable / unverifiable reward scaling.
