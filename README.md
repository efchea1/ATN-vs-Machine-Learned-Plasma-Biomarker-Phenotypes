<div align="center">

  <h1><strong>ATN vs. Machine‑Learned Plasma Biomarker Phenotypes</strong></h1>
  <h3><strong>Reproducible Analysis Pipeline for Comparing ATN Classification and Data‑Driven Clustering in a Population‑Based Cohort</strong></h3>

  <p>
    <img src="https://img.shields.io/badge/Made%20with-R-276DC3.svg">
    <img src="https://img.shields.io/badge/TensorFlow-2.x-orange.svg">
    <img src="https://img.shields.io/badge/Data-HRS%202016-blue.svg">
  </p>

</div>

---

# 📘 Overview

This repository contains the complete reproducible analysis pipeline for the manuscript:

**ATN Classification and Machine‑Learned Plasma Biomarker Phenotypes Reveal Distinct Alzheimer’s Pathology in a Population‑Based Cohort**  
*Author: Emmanuel Fle Chea, MPH*

The project compares:

### **Theory‑driven ATN classification**
- Aβ42/40 ratio  
- p‑tau181  
- NfL
- GFAP

### **Data‑driven biomarker phenotypes derived from**
- k‑means clustering  
- Gaussian mixture models (GMMs)  
- Variational Autoencoder (VAE) latent structure  
- PCA for linear comparison  

Using **4,465 participants** from the **Health and Retirement Study (HRS) 2016 Venous Blood Study**, this pipeline evaluates:

- concordance between ATN and clustering  
- biological interpretability  
- cluster stability  
- cognitive associations over 4 years  

This repository is designed for **transparency**, **reproducibility**, and **open scientific practice**.

---

# 🧠 Scientific Background

## **ATN Framework**

| Component | Biomarker      | Interpretation        |
|----------|----------------|------------------------|
| **A**    | Aβ42/40 ratio  | Amyloid pathology      |
| **T**    | p‑tau181       | Tau pathology          |
| **N**    | NfL            | Neurodegeneration      |

ATN uses **binary cutoffs**, which may obscure continuous biological variation.

---

## **Data‑Driven Phenotyping**

Unsupervised learning methods identify **continuous biomarker gradients** and **latent phenotypes**:

- **k‑means** → partitions biomarker space into clusters  
- **GMM** → probabilistic clustering  
- **VAE** → nonlinear latent structure  
- **PCA** → linear dimensionality reduction  

This project evaluates how these approaches align or diverge.

---

# 📊 Key Findings (from the manuscript)

- ATN and clustering show **modest concordance** (ARI = 0.119, NMI = 0.113).  
- Removing GFAP increases concordance by **57%**, showing its orthogonal biology.  
- **k = 4** clusters provide the best biological resolution.  
- A rare **non‑AD neurodegeneration cluster** (0.3%) is small but highly stable.  
- PCA captures **global structure**; VAE captures **localized nonlinear trajectories**.  
- Both ATN and clusters predict **4‑year cognitive decline** (R² ≈ 0.02).  

---

# 🚀 Getting Started

### **1. Clone the Repository**
```bash
git clone https://github.com/efchea1/ATN-vs-Machine-Learned-Plasma-Biomarker-Phenotypes.git
cd ATN-vs-Machine-Learned-Plasma-Biomarker-Phenotypes
```

# Install R and RStudio
- R ≥ 4.3.0
- RStudio (recommended)

# Install Required R Packages
```install.packages(c(install.packages(c("aricode", "cluster", "corrplot", "cowplot", "DESeq2", "DiagrammeR",
                   "DiagrammeRsvg", "dplyr", "factoextra", "fpc", "ggdendro", "ggplot2",
                   "ggplotify", "GGally", "glue", "gridExtra", "haven", "keras", "lme4",
                   "lmerTest", "logistf", "mclust", "naniar", "NbClust", "nnet", "patchwork",
                   "pheatmap", "ppclust", "PredictABEL", "readr", "reshape2",
                   "ResourceSelection", "reticulate", "rmda", "rsvg", "Rtsne", "survey",
                   "tensorflow", "tidyr", "tidyverse", "umap", "viridis"))
))
```

