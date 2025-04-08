# README
# Acute Myeloid Leukemia Heatmap Analysis

Analysis of RNA-seq data from 19 acute myeloid leukemia (AML) model mice samples, adapted from refine.bio examples.

## Original Source
This analysis was adapted from the [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html).

## Dataset Information
- **Source:** [Shih et al., 2017](https://pubmed.ncbi.nlm.nih.gov/28193779/)
- **Platform:** RNA-seq
- **Samples:** 19 AML model mice samples
- **Processing:** Pre-processed and quantile normalized by [refine.bio](https://www.refine.bio/)
- **Accession:** SRP070849

## Analysis Overview
This project performs clustering analysis on RNA-seq data from AML model mice, focusing on treatment responses in IDH2 and TET2 mutant samples. The analysis includes:
- Data preprocessing and normalization
- Variance-based gene selection
- Hierarchical clustering
- Heatmap visualization with annotations

## Required Libraries
```r
library(pheatmap)
library(magrittr)
library(readr)
library(dplyr)
library(tibble)
```

## Directory Structure
```markdown
project/
├── data/
│   └── SRP070849/
│       ├── SRP070849.tsv
│       └── metadata_SRP070849.tsv
├── plots/
└── results/
    └── top_90_var_genes.tsv
```

## Key Features
- **Sample Annotation:** Includes mutation status (IDH2/TET2/WT) and treatment information
- **Gene Selection:** Top quartile genes based on variance
- **Visualization:** Custom color scheme (deepskyblue → black → yellow)
- **Reproducibility:** Fixed random seed for consistent results

## Usage Instructions
1. Clone this repository
2. Create required directories using the setup script
3. Download dataset files from refine.bio
4. Run the analysis pipeline
5. Generated outputs include:
   - Clustering heatmap
   - Selected high-variance genes
   - Session information

## Output Files
- `aml_heatmap.png`: Final annotated heatmap
- `top_90_var_genes.tsv`: High-variance genes selected for analysis
- Session information for reproducibility tracking

## Citation
This analysis uses data from Shih et al., 2017 [PMID: 28193779](https://pubmed.ncbi.nlm.nih.gov/28193779/)