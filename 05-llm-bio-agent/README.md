# LLM-Powered Biology Research Agent

## Overview

An agentic workflow where an LLM autonomously queries biological databases to answer research questions. Given a natural language question like "What genes are involved in DNA repair in breast cancer?", the agent retrieves data from NCBI, UniProt, and PDB, synthesizes the information, and produces a structured research summary.

## Why This Matters

Anthropic's Life Sciences team builds "agentic workflows" that make Claude a "superhuman life sciences research assistant." This project is a prototype of exactly that — demonstrating how an LLM can orchestrate multiple biological data sources to accelerate research.

## Architecture

```
User Question
     │
     ▼
┌─────────────┐
│  LLM Agent  │ ← Decides which databases to query
└──────┬──────┘
       │
  ┌────┼────┬─────────┐
  ▼    ▼    ▼         ▼
NCBI  UniProt  PDB  PubMed
  │    │    │         │
  └────┼────┴─────────┘
       │
       ▼
┌─────────────┐
│  LLM Agent  │ ← Synthesizes results
└──────┬──────┘
       │
       ▼
  Structured Research Summary
```

## Supported Queries

| Query Type | Example | Databases Used |
|------------|---------|---------------|
| Gene info | "What does BRCA1 do?" | NCBI Gene, UniProt |
| Protein structure | "Show me the structure of p53" | PDB, UniProt |
| Literature search | "Recent papers on CRISPR in oncology" | PubMed |
| Pathway analysis | "What pathway is KRAS involved in?" | NCBI, UniProt |
| Cross-reference | "Find druggable targets in the MAPK pathway" | Multiple |

## Key Results

*Update this section as you complete the project:*

- Queries successfully answered: ___/___
- Average retrieval accuracy: ___
- Failure modes identified: ___

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_database_apis.ipynb` | Connect to NCBI Entrez, UniProt REST, PDB APIs |
| `02_tool_functions.ipynb` | Build Python functions the LLM can call as tools |
| `03_agent_loop.ipynb` | Implement the agent: plan → query → synthesize loop |
| `04_evaluation.ipynb` | Test on curated questions, measure accuracy |

## How to Run

```bash
pip install numpy pandas biopython anthropic requests

# Set your API key
export ANTHROPIC_API_KEY="your-key-here"

jupyter notebook
```

## What I Learned

*Update this section after completing the project:*

- How to design tool-use workflows for LLMs
- Working with biological database APIs programmatically
- Challenges of grounding LLM outputs in real data
- Error handling when APIs return unexpected results
