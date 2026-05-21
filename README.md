# Projet 1 — Analyse exploratoire des sous-types moléculaires du cancer du sein (TCGA-BRCA)

> **Question** : Quelles caractéristiques cliniques distinguent les sous-types moléculaires PAM50 du cancer du sein, et ces différences sont-elles statistiquement robustes après correction pour tests multiples ?

## Pourquoi ce projet ?

Le cancer du sein est moléculairement hétérogène : les sous-types intrinsèques PAM50 (Luminal A, Luminal B, HER2-enriched, Basal-like, Normal-like) ont des **pronostics différents** et appellent des **stratégies thérapeutiques distinctes**. Ce projet vise à caractériser ces différences sur la cohorte de référence TCGA-BRCA (~1100 patientes).

## Approche

1. **Récupération** des données cliniques brutes via le GDC Data Portal
2. **Nettoyage** : déduplication, harmonisation des codages de NaN, regroupement des stades
3. **Exploration descriptive** : distributions, visualisations par sous-type
4. **Tests statistiques** justifiés : Kruskal-Wallis, Chi², avec correction FDR (Benjamini-Hochberg)
5. **Synthèse visuelle** orientée décision clinique

## Résultats clés

> _À compléter après exécution._

## Structure du repo

```
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
