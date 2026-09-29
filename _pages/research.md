---
permalink: /research/
title: "Research"
author_profile: true
---

Label-Efficient Defect Detection with Active Learning
======
**Undergraduate Research Student**, Smart Manufacturing and Data Analytics (SMDA) Lab, Hanyang University  
Advisor: [Prof. Jihoon Chung](https://cjh7.github.io/) &nbsp;·&nbsp; Mar 2026 – Aug 2026

In manufacturing, labeling every product is too slow and costly, so only a small subset can be labeled. This project asked which samples should be labeled first.

- Studied semi-supervised label spreading and active learning on MNIST, then reproduced a mixed-supervision surface-defect segmentation model (Božič et al., 2021) on KSDD2 using the authors' public code.
- Replaced the paper's random choice of which 16 defect images receive pixel-level labels with active-learning strategies. Core-set (k-center) selection reached AP 0.881, compared with 0.865 for random selection.
- Extended the study to semiconductor wafer maps (WM-811K), which have no die-level ground truth. I generated 20,000+ defect masks by running 10 Claude Opus agents in parallel on an expert-style labeling procedure, and validated them on 846 defect-free wafers (median false-marking rate 0–2.1%).
- Over 10 runs with 256 labels, k-center improved IoU 1.48× over random selection (0.321 vs. 0.217, p < 0.001) and captured rare defect types (< 1%) that random selection missed. Uncertainty sampling lost to random selection in all 10 runs.
- Worked through the proofs of the core-set bound (Sener & Savarese, 2018) and confirmed that the measured coverage radius δ<sub>S</sub> ranked the strategies in the same order as their performance (k-center 3.8 vs. random 16.0).

Anomaly Detection for a Thermal Power Plant
======
**Undergraduate Thesis**, Industrial Engineering Capstone Design I, Hanyang University (team of 3)  
Mar 2025 – Jun 2025

- Handled preprocessing and LSTM-autoencoder modeling on 1,108 sensor variables recorded every minute (4,320 time points).
- Removed 202 constant sensors and a distribution-shifted day (Kolmogorov–Smirnov test), clustered sensors with DBSCAN, and kept the five highest-variability sensors per cluster as 50 model inputs.
- Reconstruction-error detection reached precision 0.99, recall 0.97, and F1 0.98, compared with F1 0.80 for a Hurst–Mahalanobis control chart.
