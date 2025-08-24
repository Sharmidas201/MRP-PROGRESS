# MRP – Entropy-Based Biomarkers and Adaptive Therapy Modeling for Cancer Survival Prediction

This repository contains the code, data, and results from my **Major Research Project (MRP)**, which investigates the effectiveness of **entropy-based pathway biomarkers** in predicting survival outcomes across heterogeneous cancer types**.

---

## 🔍 Objective

To:
1. Identify **cancer-type–specific survival-associated genes** using **univariate Cox Proportional Hazards (CoxPH)** modeling.
2. Compute **entropy scores** to quantify pathway-level dysregulation.
3. Compare gene-level and pathway-level models to evaluate prognostic power.


---

## 📊 Data Sources

- **The Cancer Genome Atlas (TCGA)**: Mutation and clinical survival data for LUSC and COADREAD.
- **OncoDB**: Median RNA expression data for curated pathway genes.
- Curated **126-gene panel** from oncogenic signaling and metabolic pathway literature (e.g., Sanchez-Vega et al., 2018).

---

## 🧪 Methodology Overview

### Phase 1 – Gene-Level Analysis
- Preprocessing and cleaning TCGA mutation & clinical data.
- Binary mutation matrix creation (altered vs. unaltered).
- **Univariate CoxPH models** per gene and cancer type.
- Identification of high-risk (HR > 1) and protective (HR < 1) genes.

### Phase 2 – Pathway Entropy Computation
- Selection of nine key signaling/metabolic pathways per cancer type.
- Entropy score calculation per patient based on pathway gene expression variability.

### Phase 3 – Pathway Survival Analysis
- CoxPH models for entropy scores per pathway and cancer type.
- Effect direction & magnitude reporting (logHR, HR, p-value).
- Visualization of risk vs. protective pathways using bar plots.

### Phase 4 – Interpretation & Adaptive Therapy Relevance
- Context-specific findings (e.g., MTOR→RB risk in LUSC vs. protective in COADREAD).
- Linking pathway effects to therapeutic modulation strategies.

---

## 📈 Key Findings

- **MTOR→RB** entropy significantly predicted survival in both cancers but with opposite effects (risk in LUSC, protective in COADREAD).
- **BRAF→NFE2L2** was protective in LUSC, consistent with oxidative stress regulation.
- **APC→RB** was strongly associated with poor prognosis in COADREAD, highlighting Wnt pathway dysregulation.
- Gene-level and pathway-level models provided complementary insights — gene-level captures single-gene effects, while entropy captures integrated dysregulation.

---

## 📂 Repository Structure

| File / Notebook | Description |
|-----------------|-------------|
| **Datapreprocessing.ipynb** | Prepares TCGA mutation & clinical data for analysis. |
| **COADREADEntropy.ipynb** | Computes pathway entropy scores for COADREAD. |
| **LUSCEntropy.ipynb** | Computes pathway entropy scores for LUSC. |
| **Cox_Analysis_with_Alterations.ipynb** | Gene-level CoxPH survival analysis. |
| **CoxHazard.ipynb** | Pathway-level CoxPH survival analysis. |
| **cox_results_top5_OS_altered.csv** | Top 5 significant genes by cancer type. |
| **top5_genes_per_cancer_type.csv** | Mutation frequency summaries. |
| **final_dataset_with_clinical.csv** | Merged dataset with clinical and entropy data. |
| **km_plots.zip** | Kaplan–Meier plots for significant genes & pathways. |

---

## 📜 Citation

If using this code or methodology, please cite:

> Das, S. (2025). *Entropy-based biomarkers and adaptive therapy modeling for survival prediction across cancer types* (Major Research Project, Toronto Metropolitan University).

---

## 🚀 Future Work

- Integrating clinical covariates into multivariate models.
- Testing deep learning survival models (e.g., DeepSurv, transformer-based).
- Simulating adaptive therapy protocols guided by entropy metrics.
- Expanding validation to additional TCGA cancer cohorts.

---
