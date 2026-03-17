# 📊 Superstore Sales — Analyse & Dashboard Power BI

> Analyse approfondie des performances commerciales d'un Superstore mondial : ventes, rentabilité et efficacité logistique. Transformation de données transactionnelles brutes en indicateurs stratégiques via Python et Power BI.

---

## 🗂️ Présentation du projet

Ce projet repose sur un dataset Kaggle représentant les ventes d'une grande distribution mondiale. L'objectif est d'identifier les segments de marché les plus porteurs, d'optimiser les marges et d'appuyer la prise de décision à travers un tableau de bord interactif.

**Pipeline :** Données brutes → Nettoyage Python → Export CSV → Modélisation & Visualisation Power BI

---

## 🎯 Objectifs

- Réaliser une analyse exploratoire complète (EDA) et du feature engineering
- Nettoyer et normaliser les données de vente
- Calculer la rentabilité par produit et par région
- Construire un tableau de bord décisionnel dans Power BI

---

## 🔍 Analyse Exploratoire (EDA)

### Nettoyage & Préparation

| Étape | Description |
|-------|-------------|
| **Conversion des types** | `Order Date` et `Ship Date` convertis pour les analyses temporelles |
| **Feature Engineering** | Création d'une colonne `Margin %` = Profit / Sales |
| **Extraction temporelle** | Colonnes `Year` et `Month` pour le filtrage chronologique |
| **Normalisation** | Arrondi des marges à deux décimales |

### Insights principaux

- **Marchés couverts :** APAC, EU, LATAM, US, Africa
- **Rentabilité variable :** La catégorie *Technology* affiche des profits unitaires élevés ; d'autres catégories subissent l'impact de remises importantes
- **Facteurs logistiques :** Le `Shipping Cost` et l'`Order Priority` influencent directement la marge nette par commande

---

## 📊 Dashboard Power BI — Vue d'ensemble

### KPIs Consolidés

| Indicateur | Valeur |
|------------|--------|
| 💰 Ventes Totales | **$12.64M** |
| 📈 Profit Total | **$1.47M** |
| 🎯 Marge Moyenne | **11.87%** |
| 📦 Quantité Totale | **178K unités** |

### Analyse Géographique

- **Treemap par marché :** APAC et EU sont les deux marchés dominants ; l'Afrique et le Canada restent des marchés de niche
- **Donut Chart par segment :**
  - 🟦 Consumer : 52%
  - 🟩 Corporate : 30%
  - 🟨 Home Office : 18%

### Tendances Temporelles

- **Saisonnalité marquée :** Pics récurrents en Q4 (fêtes + clôtures budgétaires)
- **Croissance organique :** Progression constante d'année en année

---

## 💡 Recommandations Stratégiques

1. **Améliorer la marge** — Analyser les coûts logistiques sur le marché APAC (le plus volumineux) pour identifier les leviers de réduction
2. **Focus Corporate** — Segment à plus forte fidélité et coût d'acquisition réduit ; une campagne ciblée stabiliserait les revenus hors périodes de pics
3. **Gestion prédictive des stocks** — Les pics de fin d'année sont prononcés ; anticiper les ruptures via une gestion prévisionnelle de l'inventaire

---

## 🛠️ Stack Technique

| Outil | Usage |
|-------|-------|
| **Python (Pandas)** | Nettoyage, feature engineering, export CSV |
| **Power BI Desktop** | Modélisation des données & visualisation |
| **CSV** | Format source du dataset nettoyé |

---

## 📁 Structure du projet
```
📦 superstore-sales-powerbi
├── 📄 Superstore_Sales_Cleaned.csv   # Dataset nettoyé
├── 📓 notebook_eda.ipynb             # Analyse exploratoire Python
├── 📊 dashboard_powerbi.pbix         # Tableau de bord Power BI
└── 📖 README.md
```

---

## 👤 Auteur

**Amine BERRA**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin)](https://linkedin.com/in/ton-profil)
[![GitHub](https://img.shields.io/badge/GitHub-black?logo=github)](https://github.com/ton-profil)
