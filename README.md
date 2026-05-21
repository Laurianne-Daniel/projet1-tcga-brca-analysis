# Project 1 — Exploratory Analysis of Breast Cancer Molecular Subtypes (TCGA-BRCA)

> **Research question:** Which clinical characteristics distinguish the PAM50 molecular subtypes of breast cancer, and are these differences statistically robust after correction for multiple testing?

## Why this project?

Breast cancer is molecularly heterogeneous: the intrinsic PAM50 subtypes (Luminal A, Luminal B, HER2-enriched, Basal-like, Normal-like) carry **distinct prognoses** and call for **different therapeutic strategies**. This project characterizes those differences on the reference TCGA-BRCA cohort (~1,100 patients), using a rigorous statistical workflow that documents every methodological choice — the kind of work expected from a biomedical data scientist supporting clinical or biotech teams.

## Approach

1. **Data retrieval** — clinical files downloaded from the [GDC Data Portal](https://portal.gdc.cancer.gov/)
2. **Cleaning** — deduplication, harmonization of missing-value encodings, stage regrouping, each decision documented in the notebook
3. **Descriptive exploration** — distributions and visualizations by subtype
4. **Statistical testing** — justified test selection (Kruskal-Wallis, Chi²) with FDR correction (Benjamini-Hochberg)
5. **Clinical-facing synthesis** — visualizations designed for decision-makers, not statisticians

## Key findings

> _To be completed after analysis is finalized._

## Repository structure

```
.
├── README.md
├── requirements.txt
├── projet1_tcga_brca_eda.ipynb
├── data/
│   ├── raw/             # raw files from GDC (not versioned)
│   └── processed/       # cleaned datasets (regenerable)
└── figures/             # exported figures (high-resolution PNG)
```

## How to reproduce

```bash
# 1. Clone the repository
git clone https://github.com/Laurianne-Daniel/projet1-tcga-brca-analysis.git
cd projet1-tcga-brca-analysis

# 2. Create a virtual environment
python -m venv .venv
source .venv/bin/activate          # macOS/Linux
# .venv\Scripts\Activate.ps1       # Windows PowerShell

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download the data from the GDC Data Portal
#    (detailed instructions in section 2.1 of the notebook)
#    Place TSV files in data/raw/

# 5. Launch the notebook
jupyter notebook projet1_tcga_brca_eda.ipynb
```

## Assumed limitations

- The TCGA cohort is not representative of the general population (selection bias from US academic centers)
- Mortality is analyzed without accounting for follow-up time — proper survival analysis is the subject of Project 4
- No external validation on an independent cohort (METABRIC validation planned)

## Part of a broader portfolio

This project is the first in a series of four demonstrating a complete biomedical data science workflow:

- **Project 1 (this project)** — exploratory analysis of a clinico-genomic cohort
- **Project 2** — differential gene expression analysis (RNA-seq)
- **Project 3** — interactive dashboard for exploration by non-coders
- **Project 4** — survival analysis (Kaplan-Meier, Cox proportional hazards)

## About me

I help biomedical and biotech teams turn their clinical, biological, and genomic data into reliable analyses and actionable visualizations — accelerating decision-making and reducing uncertainty. A biomedical scientist augmented by data.

**Contact:** [your email] · [LinkedIn] · [portfolio website]
