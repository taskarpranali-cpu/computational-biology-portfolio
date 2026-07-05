# LLM Biology Benchmark

## Overview

A custom benchmark evaluating how well large language models perform on biology reasoning tasks. This project designs evaluation questions across multiple biology domains, tests LLMs programmatically, and analyzes where models succeed and fail — mirroring the kind of evaluation work done by Anthropic's Life Sciences team.

## Why This Matters

Anthropic's Research Scientist (Life Sciences) role involves "translating deep biological domain knowledge into model training objectives, benchmarks, and agentic workflows." This project demonstrates exactly that skill: using biology expertise to rigorously evaluate AI.

## Benchmark Categories

| Category | Example Task | Questions |
|----------|-------------|-----------|
| **Gene Function** | Given a gene name, predict its function and associated pathways | 50 |
| **Experimental Design** | Design a CRISPR experiment to knock out gene X in cell line Y | 30 |
| **Data Interpretation** | Interpret a volcano plot or gene expression heatmap described in text | 30 |
| **Pathway Reasoning** | Predict downstream effects of inhibiting a kinase in a signaling cascade | 30 |
| **Literature Synthesis** | Summarize the role of gene X in disease Y based on provided abstracts | 20 |

## Key Results

*Update this section as you complete the project:*

- Overall accuracy by model: ___
- Strongest category: ___
- Weakest category (where biology expertise catches model errors): ___
- Common failure patterns: ___

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_benchmark_design.ipynb` | Define questions, expected answers, and scoring rubrics |
| `02_question_bank.ipynb` | Generate and curate the question dataset |
| `03_model_evaluation.ipynb` | Query LLMs via API, collect responses |
| `04_scoring_analysis.ipynb` | Score responses, compute metrics, error analysis |
| `05_results_report.ipynb` | Visualize results, identify failure patterns, write-up |

## How to Run

```bash
pip install numpy pandas matplotlib seaborn anthropic openai

# Set your API key
export ANTHROPIC_API_KEY="your-key-here"

jupyter notebook
```

## Scoring Framework

Each response is scored on:
1. **Factual accuracy** (0-3): Are the biological facts correct?
2. **Completeness** (0-2): Does it cover the key points an expert would mention?
3. **Reasoning quality** (0-2): Does it show understanding of biological mechanisms?
4. **Hallucination check** (0-1): Does it fabricate citations, genes, or pathways?

## What I Learned

*Update this section after completing the project:*

- How to design rigorous evaluations for LLMs on domain-specific tasks
- Where current LLMs struggle with biology reasoning
- The gap between "sounds right" and "is right" in scientific AI
