# breast-cancer-rnaseq-tcga
Integrative Transcriptomic and Machine Learning Analysis of Breast Cancer Using TCGA RNA-seq Data
# Integrative Transcriptomic and Machine Learning Analysis of Breast Cancer Using TCGA RNA-seq Data

![R](https://img.shields.io/badge/R-4.x-276DC3?style=flat&logo=r)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Data](https://img.shields.io/badge/Data-TCGA--BRCA-blue)

## 📌 Project Overview

This project presents a comprehensive bioinformatics pipeline for analyzing RNA-seq gene expression data from The Cancer Genome Atlas Breast Cancer (TCGA-BRCA) dataset. The workflow integrates differential gene expression analysis, functional enrichment, and machine learning classification to identify molecular mechanisms and potential biomarkers associated with breast cancer.

---

## 🎯 Objectives

- Retrieve and preprocess RNA-seq data from the TCGA-BRCA dataset
- Identify differentially expressed genes (DEGs) between tumor and normal samples
- Visualize transcriptomic patterns using PCA, volcano plots, and heatmaps
- Perform Gene Ontology (GO) enrichment analysis
- Build a Random Forest classifier to distinguish tumor vs normal samples
- Identify candidate biomarker genes

---

## 📊 Dataset

| Parameter | Value |
|---|---|
| Source | TCGA-BRCA (via TCGAbiolinks) |
| Total Samples | 1,224 |
| Tumor Samples | 1,111 |
| Normal Samples | 113 |
| Total Genes | 60,660 |
| Filtered Genes | 37,589 |

---

## 🛠️ Tools & Packages

| Category | Tools |
|---|---|
| Data Retrieval | TCGAbiolinks |
| Differential Expression | DESeq2 |
| Functional Enrichment | clusterProfiler, org.Hs.eg.db |
| Visualisation | ggplot2, pheatmap, EnhancedVolcano |
| Machine Learning | randomForest, caret |
| Environment | R, RStudio |

---

## 🔬 Methodology

1. **Data Retrieval** — Downloaded TCGA-BRCA RNA-seq counts via TCGAbiolinks
2. **Preprocessing** — Filtered low-expression genes (count ≥ 10 in at least 10 samples)
3. **Differential Expression** — DESeq2 analysis with padj < 0.05 and |Log2FC| > 1
4. **Visualisation** — PCA, volcano plots, and heatmaps using ggplot2 and pheatmap
5. **Enrichment Analysis** — Gene Ontology analysis using clusterProfiler
6. **Machine Learning** — Random Forest classifier (500 trees) on top 100 DEGs
7. **Biomarker Identification** — Feature importance from Random Forest model

---

## 📈 Key Results

- **11,406** statistically significant differentially expressed genes identified
- **Adjusted p-value** < 0.05 and **|Log2 Fold Change|** > 1
- PCA and heatmaps confirmed clear transcriptomic separation between tumor and normal samples
- GO enrichment revealed key biological processes:
  - Extracellular matrix organization
  - Humoral immune response
  - G-protein coupled receptor signaling
  - Hormone transport
- Random Forest classifier (500 trees) trained on top 100 DEGs achieved high classification accuracy

---

## 📁 Repository Structure

- **scripts/** — R Markdown analysis script
- **results/** — Output figures (volcano plot, PCA, heatmap, GO enrichment)
- **report/** — Full rendered HTML report
- **README.md** — Project documentation

---

## 🚀 How to Run

1. Clone this repository:
```bash
git clone https://github.com/PranshuJivnani/breast-cancer-rnaseq-tcga.git
```

2. Open `scripts/breast_cancer_analysis.Rmd` in RStudio

3. Install required packages:
```r
install.packages(c("BiocManager", "ggplot2", "pheatmap", "randomForest", "caret"))
BiocManager::install(c("TCGAbiolinks", "DESeq2", "clusterProfiler", "org.Hs.eg.db"))
```

4. Knit the R Markdown file to reproduce the full analysis

---

## 👤 Author

**Pranshu Jivnani**
MSc Bioinformatics — Teesside University, Middlesbrough, UK
📧 connect.pranshu19@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/pranshu-jivnani)

---

## 📄 License

This project is licensed under the MIT License.
