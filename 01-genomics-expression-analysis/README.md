# Genomics Expression Analysis

## Overview

Machine learning classification and differential expression analysis on cancer genomics data. This project demonstrates a complete computational biology workflow: loading real patient data, performing statistical analysis, building ML classifiers, and interpreting results through a biological lens.

## Dataset

**Breast Cancer Wisconsin (Diagnostic)** — 569 samples, 30 features  
Features are computed from digitized images of fine needle aspirates of breast masses. They describe characteristics of cell nuclei present in the image.

Source: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)) / `sklearn.datasets`

## Key Results

*Update this section as you complete the project:*

- Classification accuracy: ___%
- Top 5 predictive features: ___
- Biological interpretation: ___

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_data_exploration.ipynb` | Load data, summary statistics, missing value analysis |
| `02_visualization.ipynb` | Distribution plots, correlation heatmap, PCA visualization |
| `03_statistical_analysis.ipynb` | t-tests, ANOVA, multiple testing correction |
| `04_ml_classification.ipynb` | Random Forest, Logistic Regression, feature importance |
| `05_biological_interpretation.ipynb` | Map top features to biology, literature context |

## How to Run

```bash
# Clone this repository
git clone https://github.com/yourusername/computational-biology-portfolio.git
cd computational-biology-portfolio/01-genomics-expression-analysis

# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn scipy

# Launch Jupyter
jupyter notebook
```

## What I Learned

*Update this section after completing the project:*

- How to handle high-dimensional biological data
- Feature selection methods for genomics
- Connecting ML results back to biological mechanisms
