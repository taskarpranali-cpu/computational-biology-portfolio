# Neuroimaging Classification

## Overview

Classifying cognitive states from brain imaging data using machine learning. This project extracts features from neuroimaging datasets (fMRI or EEG), trains classifiers to distinguish brain states, and evaluates model performance with proper cross-validation.

## Dataset

*Choose one of these publicly available datasets:*

- **Haxby (2001)** — fMRI object recognition dataset (via Nilearn)
- **MNE sample dataset** — MEG/EEG auditory & visual stimuli
- **OpenNeuro datasets** — various fMRI experiments

Source: [Nilearn datasets](https://nilearn.github.io/stable/modules/datasets.html) / [MNE datasets](https://mne.tools/stable/overview/datasets_index.html)

## Key Results

*Update this section as you complete the project:*

- Classification accuracy: ___
- Brain regions most informative for classification: ___
- Comparison of feature extraction methods: ___

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_data_loading.ipynb` | Load neuroimaging data, visualize brain maps |
| `02_preprocessing.ipynb` | Signal cleaning, filtering, epoching (EEG) or masking (fMRI) |
| `03_feature_extraction.ipynb` | ROI-based features, time-frequency features, connectivity |
| `04_classification.ipynb` | SVM, Random Forest, cross-validated evaluation |

## How to Run

```bash
pip install numpy pandas matplotlib seaborn scikit-learn nilearn mne

jupyter notebook
```

## What I Learned

*Update this section after completing the project:*

- How neuroimaging data is structured and preprocessed
- Feature extraction strategies for brain data
- Challenges of high-dimensional, noisy biological signals
