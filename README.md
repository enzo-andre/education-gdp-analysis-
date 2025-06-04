# education-gdp-analysis-
Analyse exploratoire du lien entre le développement économique et l'éducation des filles

# Projet Data : PIB, dépenses publiques et scolarisation des filles au 21ème siècle

## 🧠 Objectif du projet

Ce projet vise à explorer les relations entre trois variables clés à l’échelle internationale :

- Le **PIB par habitant**
- Le **taux de scolarisation des filles en primaire (%)**
- Les **dépenses publiques en éducation (% du PIB)**

L’objectif est de déterminer dans quelle mesure la richesse d’un pays et ses investissements publics ont un impact sur le taux d’éducation des filles à l'école primaire.

---

## 🔎 Données utilisées

- Source : [Banque mondiale (World Bank Open Data)](https://data.worldbank.org/)
- Années analysées :
   - **2015** : analyse avec 2 variables (PIB + taux de scolarisation des filles)
   - **2018** : analyse enrichie avec 3 variables (PIB + Taux de scolarisation + dépenses publiques en éducation)
- Pays : tous les pays disposant des 3 indicateurs pour 2018
- Fichiers `.csv` utilisés :
  - `API_NY.GDP.PCAP.CD_DS2_en_csv_v2.csv` : PIB/habitant
  - `API_SE.PRM.NENR.FE_DS2_en_csv_v2.csv` : taux de scolarisation des filles (primaire)
  - `API_SE.XPD.TOTL.GD.ZS_DS2_en_csv_v2.csv` : dépenses publiques en éducation

---

## Étapes de l'analyse

1. **Préparation des données** :
   - Nettoyage
   - Transformation au format long
   - Fusion des datasets

2. **Analyse exploratoire (EDA)** :
   - Visualisation de la corrélation entre PIB et scolarisation
   - Filtrage des pays extrêmes pour lisibilité

3. **Régression linéaire simple** :
   - PIB par habitant (log) → scolarisation
   - R² : `0.202`

4. **Régression multiple** :
   - Variables explicatives :
     - log(PIB/hab)
     - Dépenses publiques en éducation
   - Variable cible : taux de scolarisation des filles
   - R² : `0.213`

---

## 💡 Résultats clés

- Une **corrélation positive modérée** entre la richesse d’un pays et la scolarisation des filles.
- L’ajout des dépenses publiques améliore **légèrement** la qualité explicative du modèle.
- Le **PIB reste la variable la plus influente** dans ce modèle.

---

## Extension du projet

Avant cette analyse principale, plusieurs tests ont été menés :

- ✅ Régressions simples sur l’année **2015** (2 variables)
- ✅ Comparaison des R² entre 2015 et 2018
- ✅ Nettoyage et visualisation progressive

---

## 📁 Contenu du dépôt

| Fichier | Description |
|--------|-------------|
| `education_gdp_analysis.ipynb` | Le notebook principal avec l’analyse complète |
| `*.csv` | Données sources issues de la Banque mondiale |
| `README.md` | Ce fichier de présentation |

---

## Pour aller plus loin

- Étendre à d'autres années
- Ajouter d’autres indicateurs (IDH, taux de fécondité, égalité de genre...)
- Construction d'un dashboard interactif

---

## 👤 Auteur

> Réalisé par **Enzo André**, dans le cadre d'une transition en data science.  
> [LinkedIn](https://www.linkedin.com/in/enzoandre/) | [Portfolio](https://github.com/enzo-andre)
