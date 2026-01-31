<div align="center">

  <h1><strong>ATN vs. Machine‑Learned Plasma Biomarker Phenotypes</strong></h1>
  <h3><strong>Reproducible Analysis Pipeline for Comparing ATN Classification and Data‑Driven Clustering in a Population‑Based Cohort</strong></h3>

  <p>
    <img src="https://img.shields.io/badge/Made%20with-R-276DC3.svg">
    <img src="https://img.shields.io/badge/TensorFlow-2.x-orange.svg">
    <img src="https://img.shields.io/badge/Data-HRS%202016-blue.svg">
    <img src="https://img.shields.io/badge/Open%20Science-Reproducible-orange.svg">
  </p>

</div>

---

# 🛠️ Repository Structure

| **Folder & File** | **Description** |
|---------------|-------------|
| **Code** | Full R Markdown pipeline (`ATN_Machine_Learned_Plasma_Biomarker_Phenotypes.Rmd`) documenting the entire workflow |
| **Figures** | All exported plots and graphs |
| **Results** | Saved models, latent spaces, training histories, serialized analysis objects, etc. |
| **Tables** | CSV outputs for all tables |
| **Data** | *(Empty)* - users must obtain HRS data through the official portal; raw HRS data are not included |
| **License** | MIT License |

---

# 📘 Overview

This repository contains the complete reproducible analysis pipeline for the manuscript:

***ATN Classification and Machine‑Learned Plasma Biomarker Phenotypes Reveal Distinct Alzheimer’s Pathology in a Population‑Based Cohort***  
**Author:** Emmanuel Fle Chea, MPH

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

- concordance between ATN and machine learning frameworks    

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

# 🚀 Getting Started

### **1. Clone the Repository**
```bash
git clone https://github.com/efchea1/ATN-vs-Machine-Learned-Plasma-Biomarker-Phenotypes.git
cd ATN-vs-Machine-Learned-Plasma-Biomarker-Phenotypes
```

### **2. Install R and RStudio**
- R ≥ 4.3.0
- RStudio (recommended)

### **3. Install Required R Packages**
```
install.packages(c(install.packages(c("aricode", "cluster", "corrplot", "cowplot", "DESeq2", "DiagrammeR",
                   "DiagrammeRsvg", "dplyr", "factoextra", "fpc", "ggdendro", "ggplot2",
                   "ggplotify", "GGally", "glue", "gridExtra", "haven", "keras", "lme4",
                   "lmerTest", "logistf", "mclust", "naniar", "NbClust", "nnet", "patchwork",
                   "pheatmap", "ppclust", "PredictABEL", "readr", "reshape2",
                   "ResourceSelection", "reticulate", "rmda", "rsvg", "Rtsne", "survey",
                   "tensorflow", "tidyr", "tidyverse", "umap", "viridis"))
))
```
---

# 📁 Data Requirements
HRS data **cannot be redistributed**.

To reproduce the analysis:
1. Register at: https://hrs.isr.umich.edu
2. Request access to the **2016 Venous Blood Study** biomarker files
3. Download the required datasets (SAS format)
4. Place them in your local working directory
5. The analysis pipeline (`.Rmd`) includes all necessary code for loading and preprocessing the HRS datasets once they are downloaded.

# 📜 Citation
If you use this code, please cite:

Chea, E.F.  
ATN Classification and Machine-Learned Plasma Biomarker Phenotypes Reveal Distinct Alzheimer's Pathology in a Population-Based Cohort.  

Preprint **DOI:** https://doi.org/10.64898/2026.01.02.26343331

**Peer-review journal publication:** *In-progress*

# 👤 Author
**Emmanuel Fle Chea, MPH**  
Independent Researcher • Data Scientist • Biomedical Researcher  
📧 **Email:** emmanuelf.chea@gmail.com

# 📄 License
This project is released under the **MIT License**.  
See the **LICENSE** file for full terms.  
You are free to reuse, modify, and build upon this work with attribution.
