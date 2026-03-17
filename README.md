# 📊 Superstore Sales — Analyse & Dashboard Power BI

> Analyse approfondie des performances commerciales d'un Superstore mondial sur 4 ans (2011–2014).  
> Transformation de données transactionnelles brutes en indicateurs stratégiques via **Python** et **Power BI**.

---

## 🗂️ Présentation du projet

Ce projet repose sur un dataset Kaggle représentant les ventes d'une grande distribution mondiale couvrant **7 marchés**, **13 régions** et **3 catégories de produits**. L'objectif est d'identifier les segments les plus porteurs, d'optimiser les marges et d'appuyer la prise de décision à travers un tableau de bord interactif en 3 pages.

**Pipeline :** Données brutes → Nettoyage Python → Export CSV → Modélisation & Visualisation Power BI

---

## 🎯 Objectifs

- Réaliser une analyse exploratoire complète (EDA) et du feature engineering
- Nettoyer et normaliser les données de vente
- Calculer la rentabilité par produit, segment et région
- Construire un tableau de bord décisionnel interactif (3 pages)

---

## 🛠️ Stack Technique

| Outil | Usage |
|---|---|
| **Python (Pandas)** | Nettoyage, feature engineering, export CSV |
| **Power BI Desktop** | Modélisation des données & visualisation |
| **CSV** | Format source du dataset nettoyé |

---

## 📁 Structure du projet

```
📦 superstore-sales-powerbi
├── 📄 Superstore_Sales_Cleaned.csv   # Dataset nettoyé (51 290 lignes)
├── 📓 notebook_eda.ipynb             # Analyse exploratoire Python
├── 📊 dashboard_powerbi.pbix         # Tableau de bord Power BI (3 pages)
└── 📖 README.md
```

---

## 🔍 Analyse Exploratoire (EDA)

### Nettoyage & Préparation

| Étape | Description |
|---|---|
| **Conversion des types** | `Order Date` et `Ship Date` convertis pour les analyses temporelles |
| **Feature Engineering** | Création d'une colonne `Marge` = `Profit / Sales × 100` |
| **Extraction temporelle** | Colonnes `Year` et `Month` pour le filtrage chronologique |
| **Normalisation** | Arrondi des marges à deux décimales pour la lisibilité |

---

## 📊 Dashboard Power BI — 3 Pages

### Page 1 — Vue d'ensemble
![Overview](https://github.com/user-attachments/assets/c1641152-976b-418c-8bfa-47d175771dcf)

#### KPIs Consolidés (2011–2014)

| Indicateur | Valeur |
|---|---|
| 💰 Chiffre d'affaires | **$12.64M** |
| 📈 Bénéfice net | **$1.47M** |
| 🛒 Commandes | **25 035** |
| 👥 Clients uniques | **1 590** |
| 🎯 Marge moyenne | **11.61%** |

#### Évolution du CA et Bénéfice (2011–2014)

Croissance organique constante et soutenue sur toute la période, avec un **CA quasi doublé en 4 ans (+90%)**.

| Année | Ventes | Profit | Croissance CA |
|---|---|---|---|
| 2011 | $2.26M | $249K | — |
| 2012 | $2.68M | $307K | +18.5% |
| 2013 | $3.41M | $407K | +27.2% |
| 2014 | $4.30M | $504K | +26.3% |

> Le profit suit la même trajectoire ascendante, confirmant que la croissance ne sacrifie pas les marges.

#### Répartition par Segment

| Segment | Part des ventes |
|---|---|
| 🟦 Consumer | **51.5%** |
| 🟩 Corporate | **30.3%** |
| 🟨 Home Office | **18.3%** |

Le segment **Consumer** domine mais reste le plus volatile (sensible aux pics saisonniers de Q4). Le segment **Corporate** représente 30% du CA avec une fidélité et une régularité supérieures.

#### Ventes & Bénéfice par Catégorie

| Catégorie | Ventes | Profit | Marge moyenne |
|---|---|---|---|
| Technology | $4.74M | $664K | 4.97% |
| Furniture | $4.11M | $285K | **0.86%** ⚠️ |
| Office Supplies | $3.79M | $518K | **5.90%** ✅ |

> **Insight clé :** La Furniture est 2ème en volume mais dernière en rentabilité (0.86% de marge). Office Supplies est la catégorie la plus rentable en proportion malgré un volume inférieur.

#### Top 5 Sous-catégories par Bénéfice

| Rang | Sous-catégorie | Profit |
|---|---|---|
| 🥇 | Copiers | $258K |
| 🥈 | Phones | $217K |
| 🥉 | Bookcases | $162K |
| 4 | Appliances | $142K |
| 5 | Chairs | $140K |

---

### Page 2 — Régions
![Region](https://github.com/user-attachments/assets/88ebe6ed-0841-433d-b926-4a6f566c7710)

#### KPIs Régionaux

| KPI | Valeur |
|---|---|
| 🏆 Meilleure région | **Central** ($2.82M) |
| 🌍 Marchés actifs | **13 régions** sur 7 zones géographiques |

#### Part de marché par zone géographique

| Marché | Part | Coût expédition moyen |
|---|---|---|
| APAC | **28.4%** 🥇 | $35.19 ⚠️ |
| EU | **23.2%** 🥈 | $30.94 |
| US | 18.2% | $23.83 |
| LATAM | 17.1% | $22.75 |
| EMEA | 6.4% | $17.57 |
| Africa | 6.2% | $19.22 |
| Canada | 0.5% | $19.29 |

> **APAC et EU représentent 51.6% du CA total** — ce sont les deux piliers de l'entreprise. À noter que l'APAC affiche les coûts d'expédition les plus élevés ($35.19/commande), ce qui pèse directement sur les marges dans ce marché pourtant dominant.

#### Classement des régions par CA

| Rang | Région | Ventes |
|---|---|---|
| 🥇 | Central | $2.82M |
| 🥈 | South | $1.60M |
| 🥉 | North | $1.25M |
| 4 | Oceania | $1.10M |
| 5 | Southeast Asia | $0.88M |

> La région **Central** génère presque le double de la 2ème région (South). Elle regroupe des marchés US et LATAM à fort volume.

---

### Page 3 — Produits
![Products](https://github.com/user-attachments/assets/7238ad82-be81-41e0-9f48-e25deb4e2aed)

#### KPIs Produits

| KPI | Valeur | Signification |
|---|---|---|
| ✅ Meilleure catégorie | **Technology** | $664K de profit absolu |
| ✅ Top sous-catégorie | **Phones** | Plus haut volume de ventes |
| 🚨 Alerte perte | **Tables** | Seule sous-catégorie en perte nette |
| 🚨 Marge Tables | **-24.2%** | Perte sèche sur chaque vente |

#### Analyse complète des sous-catégories

**Profit par sous-catégorie (toutes) :**

| Sous-catégorie | Profit | Statut |
|---|---|---|
| Copiers | +$258K | ✅ |
| Phones | +$217K | ✅ |
| Bookcases | +$162K | ✅ |
| Appliances | +$142K | ✅ |
| Chairs | +$140K | ✅ |
| Accessories | +$130K | ✅ |
| ... | ... | ✅ |
| Machines | +$59K | ⚠️ Marge négative (-4.35%) |
| **Tables** | **-$64K** | 🚨 **Perte structurelle** |

#### 🚨 Focus — La sous-catégorie Tables

C'est **le signal d'alarme majeur du dataset** :

- **Profit : -$64 083** (seule sous-catégorie en rouge)
- **Marge moyenne : -24.2%** → l'entreprise perd 24 centimes sur chaque dollar vendu
- Causes probables : remises excessives (`Discount` élevé) et/ou coûts logistiques disproportionnés pour des articles volumineux

---

## 💡 Recommandations Stratégiques

### Forces identifiées ✅

- Croissance robuste sur 4 ans (+90% CA, profit x2)
- Présence mondiale établie sur 7 marchés et 13 régions
- Technology (Copiers, Phones) = moteurs de profit fiables

### Points critiques à adresser 🚨

| Priorité | Action | Impact attendu |
|---|---|---|
| 🔴 Urgent | **Audit Tables** — analyser les remises accordées et les coûts logistiques. Stopper les ventes déficitaires ou repositionner le prix | Stopper -$64K de pertes annuelles |
| 🔴 Urgent | **Furniture** — marge de 0.86% sur $4.1M est un risque majeur. Réduire les remises ou renégocier les coûts fournisseurs | +plusieurs centaines de K$ de marge |
| 🟠 Important | **Logistique APAC** — coûts d'expédition les plus élevés ($35.19) sur le plus grand marché (28.4%). Même -10% libère plusieurs dizaines de K$ | Amélioration directe des marges |
| 🟡 Moyen terme | **Développer Corporate** — 30% du CA mais plus stable et fidèle que Consumer. Campagne ciblée B2B | Stabilisation des revenus hors Q4 |
| 🟡 Moyen terme | **Gestion prédictive des stocks** — pics Q4 très marqués. Anticiper les ruptures par prévision de la demande | Optimisation logistique saisonnière |
| 🟢 À étudier | **Rationaliser Canada** — 0.5% du CA pour un marché entier à gérer. ROI du marché à analyser | Réduction des coûts de structure |

---

## 👤 Auteur

**Amine BERRA**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ton-profil)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ton-profil)

---

*Dataset source : [Kaggle — Superstore Sales Dataset](https://www.kaggle.com/)*
