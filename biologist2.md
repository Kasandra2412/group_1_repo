Luecken, M.D. & Theis, F.J. (2019). *Current best practices in single-cell RNA-seq analysis: a tutorial.*  
*Molecular Systems Biology, 15*(6), e8746.  
[DOI Link](https://www.embopress.org/doi/10.15252/msb.20188746)  

## 🧬 GitHub Repository
[https://github.com/theislab/single-cell-tutorial](https://github.com/theislab/single-cell-tutorial)


# Biologist Report 1 – ColabFold (Protein Structure Prediction)

## Paper Information
**Title:** ColabFold: making protein folding accessible to all  
**Authors:** Mirdita, Schütze et al., *Nature Methods* (2022)  
**Article Link:** [https://www.nature.com/articles/s41592-022-01488-1](https://www.nature.com/articles/s41592-022-01488-1)  
**GitHub Repo:** [https://github.com/sokrypton/ColabFold](https://github.com/sokrypton/ColabFold)  
**Colab Notebook:** [AlphaFold2.ipynb](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/AlphaFold2.ipynb)  
**Website:** [https://colabfold.mmseqs.com](https://colabfold.mmseqs.com)

## Platform
Google Colab / Jupyter Notebook (runs fully in browser with GPU)

## Summary of the Paper
ColabFold simplifies AlphaFold2 protein structure prediction into an easy-to-run notebook.  
It combines MMseqs2 sequence search with AlphaFold2’s model for fast 3D folding of proteins or complexes.  
This method makes high-accuracy protein folding available to anyone without special hardware or installations.

## Why It Fits Our Theme
This paper provides an open, runnable notebook that aligns with our engineering team’s Jupyter setup and produces clear biological outputs (3D structures → function).  
It connects computational modeling with biological interpretation


# Biologist Report 2 — BioBB Workflows (Reproducible Biomolecular Simulation)

## Paper Information  
**Title:** Using interactive Jupyter Notebooks and BioConda for FAIR and reproducible biomolecular simulation workflows  
**Authors:** Bayarri, Andrio, Gelpí, Hospital, Orozco, *PLOS Computational Biology* (2024)  
**Article Link:** [https://doi.org/10.1371/journal.pcbi.1012173](https://doi.org/10.1371/journal.pcbi.1012173)  
**GitHub Repo:** [https://github.com/bioexcel/biobb_workflows](https://github.com/bioexcel/biobb_workflows)  
**Website:** [https://mmb.irbbarcelona.org/biobb/](https://mmb.irbbarcelona.org/biobb/)  

## Platform  
Jupyter Notebook (local or remote via BioConda environment)  

## Summary of the Paper  
This paper introduces BioBB Workflows, a collection of reproducible biomolecular simulation pipelines designed to run in Jupyter Notebooks using **BioConda** packages.  
It focuses on fair principles — Findable, Accessible, Interoperable, and Reusable — for biomolecular modeling, docking, and molecular dynamics.  
The authors provide complete runnable notebooks for tasks like protein–ligand docking and trajectory analysis, demonstrating open and shareable computational biology workflows.

## Why It Fits Our Theme  
This project provides directly runnable Jupyter notebooks with reproducible environments — ideal for our engineering team to execute and test.  
From a biological perspective, it connects simulation data (e.g., protein–ligand interactions) with interpretation of structural dynamics — aligning with our group’s protein modeling focus.  


# Biologist Report 3 – Protein Solubility Prediction (Regression & ANN Models)

## Paper Information
**Title:** Protein solubility prediction using regression, artificial neural networks, and XGBoost  
**Authors:** Xiaomi Zhou et al. (Independent Research, 2020)  
**Article Link:** (No formal journal publication; open research release via GitHub)  
**GitHub Repo:** [https://github.com/xiaomizhou616/Protein_solubility_regression_model](https://github.com/xiaomizhou616/Protein_solubility_regression_model)  
**Jupyter Notebooks:**  
- [ANNs-solubility-final.ipynb](https://github.com/xiaomizhou616/Protein_solubility_regression_model/blob/main/ANNs-solubility-final.ipynb)  
- [XGboost-final.ipynb](https://github.com/xiaomizhou616/Protein_solubility_regression_model/blob/main/XGboost-final.ipynb)

## Platform
Jupyter Notebook (Python 3; pandas, numpy, sklearn, xgboost)

## Summary of the Paper
This project builds machine learning models to predict protein solubility from sequence-derived features.  
It uses linear regression, artificial neural networks, and XGBoost to identify key physicochemical properties linked to protein solubility.  
The GitHub repository provides complete Jupyter notebooks, example datasets, and ready-to-run code for immediate experimentation.

## Why It Fits Our Theme
This repository offers a simple, executable notebook that reinforces our bioinformatics learning focus on protein modeling.  
It teaches the relationship between biological sequences and experimental outcomes (solubility) through accessible, interpretable ML models.  
It’s ideal for the engineering team since all code runs locally in Jupyter with minimal dependencies.


# Biologist Report 4 – SoDoPE (Protein Solubility and Domain Prediction)

## Paper Information
**Title:** SoDoPE: Fast and accurate prediction of protein solubility and domain boundaries  
**Authors:** Gardner BinfLab (University of Melbourne, 2020)  
**Article Link:** [https://academic.oup.com/bioinformatics/article-pdf/36/18/4691/50677813/btaa578.pdf](https://academic.oup.com/bioinformatics/article-pdf/36/18/4691/50677813/btaa578.pdf)  
**GitHub Repo:** [https://github.com/Gardner-BinfLab/SoDoPE_paper_2020](https://github.com/Gardner-BinfLab/SoDoPE_paper_2020)  
**Jupyter Notebook:** [SoDoPE_notebook.ipynb](https://github.com/Gardner-BinfLab/SoDoPE_paper_2020/blob/master/SoDoPE_notebook.ipynb)  

## Platform
Jupyter Notebook (Python 3; pandas, scikit-learn, matplotlib)

## Summary of the Paper
SoDoPE integrates machine learning with protein feature extraction to predict solubility and folding domains.  
It uses sequence-based features and pre-trained ML classifiers for solubility scoring, and the repository includes a runnable notebook for demonstration.  
This project aims to simplify bioinformatics predictions for experimental protein design.

## Why It Fits Our Theme
This paper continues our team’s focus on protein analysis using open, runnable Jupyter notebooks.  
It provides a reproducible workflow that’s easy for engineers to test and adapt, connecting biological data with predictive modeling.  
It balances scientific rigor with technical accessibility—making it a great addition to our group project.
