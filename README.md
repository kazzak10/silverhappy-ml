# Silver Happy — Data Analysis & ML Classification

> Projet annuel ESGI · Analyse de données et Machine Learning appliqués à la Silver Economy

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?logo=pandas&logoColor=white)
![Accuracy](https://img.shields.io/badge/Accuracy-82.2%25-brightgreen)
![CV](https://img.shields.io/badge/CV_5--folds-81.2%25_±_3.4%25-green)

---

## Contexte

Silver Happy est une plateforme de services à la personne dédiée aux seniors de 60 ans et plus (Silver Economy). Ce projet couvre deux axes :

1. **Reporting & Dashboards** — Analyse de l'activité et KPI pour la direction
2. **Classification ML** — Prédire la catégorie de service qu'un senior va souscrire

---

## Résultats clés

| Modèle | Accuracy Test | CV 5-folds |
|--------|--------------|------------|
| Random Forest (300 estimateurs) | **82.2%** | **81.2% ± 3.4%** |

**Feature la plus déterminante : `age_senior`** (importance Gini ~33%)

Insight métier : Les seniors de 60-65 ans plébiscitent Sport & Loisirs, les 80+ s'orientent vers Santé & Bien-être et Aide Administrative. Le nombre de connexions à la plateforme est le second signal (engagement numérique corrélé avec Loisirs & Culture).

---

## Structure du projet

```
silverhappy-ml/
├── notebooks/
│   ├── 01_reporting.ipynb         # EDA, dashboards, KPI
│   └── 02_ml_classification.ipynb # Pipeline ML complet
├── data/
│   ├── dataset_silverhappy.csv    # Dataset reporting (500 interventions)
│   └── dataset_silverhappy_v2.csv # Dataset ML (900 profils seniors)
├── outputs/
│   ├── A1_demographics.png
│   ├── A2_abonnements.png
│   ├── A3_engagement.png
│   ├── B1_kpi_services.png
│   ├── B2_evolution.png
│   ├── B3_conversion.png
│   ├── EDA_demographics.png
│   ├── ML_confusion_matrix.png
│   └── ML_feature_importance.png
├── requirements.txt
└── README.md
```

---

## Notebooks

### `01_reporting.ipynb` — Reporting & Dashboards

- **Partie A** · Profil démographique des adhérents (âge, genre, ville)
- **Partie A** · Analyse des abonnements et engagement (ancienneté, connexions)
- **Partie B** · KPI par service (CA, notes, durées moyennes)
- **Partie B** · Évolution mensuelle du CA et des interventions
- **Partie B** · Taux de conversion et statuts des demandes

### `02_ml_classification.ipynb` — Classification ML

- Chargement et exploration du dataset (900 profils)
- Feature engineering — encodage + `age_group` (tranche Silver Economy)
- Split stratifié 80/20 + validation croisée StratifiedKFold (5 folds)
- Entraînement Random Forest (`class_weight='balanced'`)
- Matrice de confusion + rapport de classification par classe
- Feature importance (Gini)
- Prédiction sur nouveaux profils

---

## Stack technique

| Domaine | Outils |
|---------|--------|
| Manipulation données | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn (RandomForest, StratifiedKFold, LabelEncoder) |
| Environnement | Python 3.10+, Jupyter Notebook |

---

## Installation

```bash
git clone https://github.com/<your-username>/silverhappy-ml.git
cd silverhappy-ml
pip install -r requirements.txt
jupyter notebook
```

---

## Auteur

**Zakaria Houari** · Étudiant Bachelor Informatique spécialité IA/Data · ESGI Paris

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Zakaria_Houari-0077B5?logo=linkedin)](https://linkedin.com/in/zakaria-houari)
[![GitHub](https://img.shields.io/badge/GitHub-@username-181717?logo=github)](https://github.com/username)
