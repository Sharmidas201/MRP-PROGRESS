# MRP-PROGRESS
This repository contains the code, data, and results from my Major Research Project (MRP), which explores the effectiveness of entropy-based biomarkers and adaptive therapy modeling in improving survival prediction across heterogeneous cancer types.
---

## 🔍 Objective

To identify cancer-type-specific survival-associated genes and quantify pathway-level dysregulation using entropy metrics, with the goal of supporting adaptive therapy strategies.

---

## 📊 Data Sources

- **The Cancer Genome Atlas (TCGA)** mutation and clinical survival data
- Curated gene panel of ~126 genes involved in signaling/metabolic pathways

---

## 🧪 Methodology

- Data preprocessing, cleaning, and transformation
- Kaplan–Meier survival analysis
- Mutation-type risk ratio computation
- Univariate Cox Proportional Hazards modeling (by cancer type)
- Entropy score calculation for significant pathways
- Adaptive therapy modeling using entropy-guided risk

---

## 📁 Repository Contents

| |Description |
|---------------|
| Raw and cleaned datasets used in the study |
| Jupyter notebooks for EDA, modeling, entropy analysis |
| KM plots, heatmaps, survival diagrams |
| CSVs with top gene results, Cox outputs |
| Python modules for processing or modeling |

---

## 🧠 Key Findings

- TP53, EGFR, and SOX9 showed pan-cancer significance
- Specific mutation types (e.g., translation start site) are high-risk
(ONGOING)
