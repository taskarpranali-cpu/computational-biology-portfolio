# Drug Discovery ML Pipeline

## Overview

Predicting drug potency (pIC50 values) from molecular structure using machine learning. This project covers the full cheminformatics pipeline: retrieving bioactivity data from ChEMBL, computing molecular fingerprints, training predictive models, and visualizing chemical space.

## Dataset

**ChEMBL Bioactivity Data** — compounds tested against a target protein  
Molecular descriptors: PubChem fingerprints / Morgan fingerprints via RDKit

Source: [ChEMBL Database](https://www.ebi.ac.uk/chembl/) via API  
Reference repo: [weixin10/Machine-Learning-for-Drug-Discovery](https://github.com/weixin10/Machine-Learning-for-Drug-Discovery)

## Key Results

*Update this section as you complete the project:*

- Model R² score: ___
- Best performing model: ___
- Key molecular features driving potency: ___

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_data_retrieval.ipynb` | Query ChEMBL API, download bioactivity data |
| `02_molecular_descriptors.ipynb` | SMILES to fingerprints with RDKit, descriptor computation |
| `03_model_training.ipynb` | Random Forest, SVR, model comparison and evaluation |
| `04_chemical_space.ipynb` | t-SNE visualization of molecular fingerprints, SAR analysis |

## How to Run

```bash
pip install numpy pandas matplotlib seaborn scikit-learn rdkit-pypi chembl_webresource_client

jupyter notebook
```

## What I Learned

*Update this section after completing the project:*

- How to work with molecular representations (SMILES, fingerprints)
- Connecting chemical structure to biological activity
- Evaluating regression models for drug potency prediction
