# Predicting Developmental Disorders Using scRNA-seq Data

This repository contains my MSc Data Science final project, which explores the use of machine learning to predict early developmental disorders using single-cell RNA sequencing (scRNA-seq) data from human embryos.

## Project Overview
Developmental disorders often originate during early embryogenesis, yet diagnosis typically occurs much later. This project investigates whether machine learning models can learn meaningful patterns from high-dimensional scRNA-seq data to identify disrupted developmental trajectories at an early stage.

The study uses the publicly available **GSE155121** dataset, consisting of over **476,000 single cells** sampled from **13 human embryos** across post-conception weeks **3–12**, a critical window for gastrulation, neurulation, and early organ formation.

## Objectives
- Preprocess and analyse large-scale scRNA-seq data
- Apply machine learning and graph-based models for developmental stage prediction
- Compare classical ML models with deep learning approaches
- Identify biologically meaningful gene markers associated with development
- Build an interpretable and reproducible analysis pipeline

## Dataset
- **Source:** NCBI Gene Expression Omnibus (GEO) – GSE155121
- **Data type:** Single-cell RNA sequencing (scRNA-seq)
- **Cells:** ~476,000
- **Genes:** ~32,000 per cell
- **Metadata:** developmental stage, spatial origin, cell type annotations

Due to size constraints, raw data is not included in this repository.

## Models Implemented
- **Graph Attention Network (GAT)**  
  Captures relational structure between cells using k-nearest neighbour graphs and attention mechanisms.
- **Random Forest (RF)**  
  Provides a strong, interpretable baseline for high-dimensional biological data.
- **XGBoost**  
  Achieved the best overall performance and strongest generalization.

## Methodology
- Data normalization and log transformation
- Selection of highly variable genes (HVGs)
- Feature scaling and dimensionality reduction
- Graph construction for GAT using kNN
- Model training, validation, and comparison
- Feature importance and biomarker analysis

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrices
- UMAP visualizations

## Key Results
- **XGBoost** achieved the highest performance with an **F1-score ≈ 0.989**
- **Random Forest** showed strong generalization and interpretability
- **GAT** effectively captured gene–gene and cell–cell relationships
- Several biologically relevant genes were consistently identified across models

## Key Findings
- Gene expression patterns contain strong predictive signals for developmental stages
- Ensemble and boosting methods perform exceptionally well on scRNA-seq data
- Graph-based learning offers valuable biological interpretability
- Shared biomarkers across models highlight robust developmental signals

## Project Structure
- `notebooks/` – Jupyter notebooks for preprocessing, modelling, and analysis
- `figures/` – Generated plots and visualizations
- `README.md` – Project overview

## Tools & Technologies
- Python
- Scanpy, AnnData
- Scikit-learn
- XGBoost
- PyTorch & PyTorch Geometric
- NumPy, Pandas
- Matplotlib, Seaborn
- Jupyter Notebook

## How to Run
1. Clone the repository
   ```bash
   git clone https://github.com/SamaraNaeem/EmbryoGene-Predictor.git
