# Variance-Averse n-Step Offline Reinforcement Learning

**Anonymous Authors**

---

<p align="center">
  <a href="#">📄 Paper</a> |
  <a href="#">💻 Code</a> |
  <a href="#">🌐 Project Page</a>
</p>

---

## 🔔 News
- **[2026-XX-XX]** Anonymous project page released for peer review.
- **[2026-XX-XX]** Paper submitted to a top-tier machine learning conference.

---

## 📌 Abstract
Offline reinforcement learning (RL) in sparse, long-horizon environments is
challenging due to compounding value estimation errors and dataset-induced
uncertainty.
While multi-step returns reduce long-horizon bias, they often amplify return
variance and destabilize learning under heterogeneous behavior data.
We propose a **variance-averse offline RL framework** that combines $n$-step
learning with **categorical distributional value estimation** and
**variance-aware policy optimization**.
By explicitly downweighting high-variance return targets, the proposed method
enables stable exploitation of long-horizon information.
Extensive experiments on challenging benchmarks demonstrate consistent
performance improvements, particularly under high-variance data regimes.

---

## 🧠 Method Overview

<p align="center">
  <img src="assets/overview.png" width="90%">
</p>

Our framework consists of three key components:

1. **$n$-step return learning** to mitigate long-horizon bootstrapping bias.
2. **Categorical distributional critic** to model return uncertainty and variance.
3. **Variance-averse policy optimization** that suppresses unreliable,
   high-variance targets via variance-aware value aggregation and action selection.

Together, these components enable robust offline RL even when naive multi-step
learning fails due to variance amplification.

---

## 📊 Experimental Results

<p align="center">
  <img src="assets/results.png" width="90%">
</p>

We evaluate the proposed method on **D4RL AntMaze** and **OGBench**
tasks covering sparse rewards, long horizons, and noisy behavior datasets.
Across all settings, our approach consistently outperforms strong baselines,
including flow-based policies with naive $n$-step returns.
Notably, the proposed method remains stable as dataset-induced return variance
increases, where existing methods often collapse.

---

## 🎯 Qualitative Results

<p align="center">
  <img src="assets/qualitative.gif" width="90%">
</p>

Qualitative rollouts show that the learned policies exhibit more stable and
goal-directed behaviors, avoiding erratic exploration caused by high-variance
value targets.
This highlights the practical benefits of variance-aware decision making in
offline RL.

---

## 📚 BibTeX
```bibtex
@inproceedings{anonymous2026vanflow,
  title     = {Variance-Averse n-Step Offline Reinforcement Learning for Sparse Long-Horizon Environments},
  author    = {Anonymous Authors},
  booktitle = {Conference Name},
  year      = {2026}
}
