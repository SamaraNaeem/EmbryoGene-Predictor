# EmbryoGene-Predictor
This repository contains code for predicting developmental stages of early human embryos using machine learning models trained on single-cell RNA sequencing (scRNA-seq) data (GSE155121).

Implemented models:
Graph Attention Network (GAT) – using PyTorch Geometric
Random Forest (RF) – using Scikit-learn
XGBoost – using XGBoost library

The objective is to classify cells by developmental stage and extract biologically meaningful marker genes.

Future Improvements
Add spatial transcriptomics integration.

Hyperparameter tuning with Optuna.

Expand model comparison with GraphSAGE and GATv2.

📄 License
This project is licensed under the MIT License
