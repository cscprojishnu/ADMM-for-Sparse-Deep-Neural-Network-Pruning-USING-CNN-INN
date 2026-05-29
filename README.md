# Prune Smart, Train Sharp: ADMM-Powered CNN and INN Models for Image Classification

Official implementation of the IEEE conference paper:

**“Prune Smart, Train Sharp: ADMM-Powered CNN and INN Models for Image Classification”**
**Published in IEEE Xplore (ICITIIT 2026)**
DOI: https://doi.org/10.1109/ICITIIT68860.2026.11499527

---

## Overview

This repository contains the implementation and experimental setup for our IEEE-published work on **ADMM-based structured pruning for image classification** using:

* **Convolutional Neural Networks (CNN)**
* **Involution / Invertible Neural Networks (INN)**
* **ADMM-integrated training optimization**
* **Post-training ADMM pruning**

The project evaluates six model configurations on the **CIFAR-10 benchmark dataset** and demonstrates how **Alternating Direction Method of Multipliers (ADMM)** can improve both:

* **Classification accuracy**
* **Model compactness / sparsity**

while preserving efficient training and deployment.

---

## Published Paper

📄 IEEE Xplore Publication:
https://doi.org/10.1109/ICITIIT68860.2026.11499527

### Citation

If you use this work in your research, please cite:

```bibtex
@INPROCEEDINGS{11499527,
  author={Dandamudi, Jishnu Teja and Chhetri, Yogendra},
  title={Prune Smart, Train Sharp: ADMM-Powered CNN and INN Models for Image Classification},
  booktitle={2026 International Conference on Intelligent Technologies, Information and Communication (ICITIIT)},
  year={2026},
  publisher={IEEE},
  doi={10.1109/ICITIIT68860.2026.11499527}
}
```

---

## Key Contributions

* Implementation of baseline **CNN** and **INN** models on CIFAR-10
* Integration of **ADMM optimization directly during training**
* Structured pruning for:

  * CNN filters
  * INN invertible blocks
* Comparative benchmarking across:

  * Baseline models
  * ADMM-enhanced models
  * Standalone post-training pruning variants
* Evaluation using:

  * Accuracy
  * Precision / Recall / F1-score
  * Confusion matrices

---

## Dataset

### CIFAR-10

* **60,000 RGB images**
* Image size: **32×32**
* **10 classes**
* Split:

  * **50,000 training**
  * **10,000 testing**

Classes:

* airplane
* automobile
* bird
* cat
* deer
* dog
* frog
* horse
* ship
* truck

---

## Models Evaluated

### 1. CNN

Baseline convolutional network.

### 2. INN

Baseline involution / invertible architecture.

### 3. CNN + ADMM

ADMM integrated during training for structured filter pruning.

### 4. INN + ADMM

ADMM-based structured pruning with invertibility constraints.

### 5. ADMM-Pruned CNN

Post-training pruning.

### 6. ADMM-Pruned INN

Post-training pruning.

---

## Experimental Results

### Performance Summary

| Model              | Epochs | Accuracy (%) |
| ------------------ | -----: | -----------: |
| CNN                |     50 |        91.09 |
| CNN                |    100 |        89.08 |
| CNN + ADMM         |     50 |        91.90 |
| CNN + ADMM         |    100 |    **92.40** |
| ADMM (CNN Variant) |     30 |        89.75 |
| ADMM (CNN Variant) |     50 |        91.51 |
| ADMM (CNN Variant) |    100 |        91.80 |
| INN                |     40 |        72.75 |
| INN                |     50 |        72.83 |
| INN                |    100 |        88.22 |
| INN + ADMM         |     50 |        86.28 |
| INN + ADMM         |    100 |        89.97 |
| ADMM (INN Variant) |     50 |        76.41 |
| ADMM (INN Variant) |    100 |    **94.21** |

### Main Findings

* **CNN + ADMM achieved 92.4%**
* **ADMM-pruned INN achieved 94.21%**
* ADMM improves:

  * generalization
  * sparsity
  * model efficiency
* Structured pruning reduces complexity without sacrificing performance

---

Metrics include:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

---

## Future Work

Potential extensions:

* ResNet + ADMM
* Vision Transformers + pruning
* CIFAR-100 / ImageNet
* Hardware-aware pruning
* Explainability for compressed models

---

## Authors

**Jishnu Teja Dandamudi**
Amrita School of Artificial Intelligence
Amrita Vishwa Vidyapeetham, Coimbatore, India

**Yogendra Chhetri**
Centre for Continuing Education
Indian Institute of Science, Bengaluru, India

---

## License

Add your preferred license:

* MIT
* Apache 2.0
* GPL

---

## Acknowledgement

This work was presented at **ICITIIT 2026** and published through **IEEE Xplore**.
