Exploratory Analysis of Molecular Subtypes of Breast Cancer (TCGA-BRCA)
Question: What clinical characteristics distinguish the PAM50 molecular subtypes of breast cancer, and are these differences statistically robust after correction for multiple testing?

Why this project?
Breast cancer is molecularly heterogeneous: the intrinsic PAM50 subtypes (Luminal A, Luminal B, HER2-enriched, Basal-like, Normal-like) have different prognoses and require distinct therapeutic strategies. This project aims to characterize these differences in the TCGA-BRCA reference cohort (~1,100 patients).

Approach
Retrieval of raw clinical data via the GDC Data Portal
Data cleaning: deduplication, harmonization of NaN codes, stage grouping
Descriptive exploration: distributions, visualizations by subtype
Justified statistical tests: Kruskal-Wallis, Chi², with FDR correction (Benjamini-Hochberg)
Visual summary oriented toward clinical decision-making
Key results
To be completed after execution.

Repo structure

.
├── README.md
├── requirements.txt
├── projet1_tcga_brca_eda.ipynb
├── data/
│   ├── raw/             # données téléchargées du GDC (non versionnées)
│   └── processed/       # données nettoyées
└── figures/             # figures exportées en PNG haute résolution
```

## Comment reproduire

```bash
# 1. Cloner le repo
git clone <url-du-repo>
cd projet1-tcga-brca

# 2. Créer un environnement virtuel
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
pip install -r requirements.txt

# 3. Télécharger les données depuis le GDC Data Portal
#    Instructions détaillées dans la section 2.1 du notebook
#    Déposer les fichiers TSV dans data/raw/

# 4. Lancer le notebook
jupyter notebook projet1_tcga_brca_eda.ipynb
```

## Limites assumées

- Cohorte TCGA non représentative de la population générale
- Comparaison de mortalité sans tenir compte du temps de suivi (analyse de survie complète prévue en Projet 4)
- Pas de validation externe sur cohorte indépendante (METABRIC envisagée)

## Pour aller plus loin

Ce projet est le premier d'une série de 4 démontrant un workflow complet de data science biomédicale :

- **Projet 1 (ce projet)** : analyse exploratoire d'une cohorte clinico-génomique
- **Projet 2** : analyse différentielle d'expression génique (RNA-seq)
- **Projet 3** : dashboard interactif pour exploration par des non-codeurs
- **Projet 4** : analyse de survie (Kaplan-Meier, Cox)

## Contact

[Ton nom] — [email] — [LinkedIn] — [site portfolio]

*Scientifique biomédicale augmentée par la data — analyse de données cliniques, biologiques et génomiques pour la biotech.*
