#  Healthcare BI Platform

Plateforme de Business Intelligence de bout en bout pour l'analyse de données hospitalières, le suivi de la performance des hôpitaux et l'aide à la décision.

---

##  Sommaire

- [Fonctionnalités](#-fonctionnalités)
- [Technologies](#-technologies)
- [Modèle de données](#-modèle-de-données)
- [Architecture](#-architecture)
- [Dashboards](#-dashboards)
- [KPIs](#-kpis)
- [Pipeline ETL](#-pipeline-etl)
- [Structure du projet](#-structure-du-projet)
- [Objectifs métier](#-objectifs-métier)
- [Confidentialité & sécurité](#-confidentialité--sécurité)
- [Améliorations futures](#-améliorations-futures)

---

##  Fonctionnalités

- Pipelines ETL pour l'intégration des données hospitalières
- Modélisation dimensionnelle du data warehouse
- Dashboards Power BI interactifs et suivi des KPI
- Analyse des admissions hospitalières et de l'activité en soins intensifs (ICU)
- Analyse de la durée de séjour des patients
- Analyse des diagnostics et pathologies
- Suivi des réadmissions et de la mortalité
- Analyse des ressources et des assurances santé
- Suivi de la performance et de l'activité opérationnelle des hôpitaux
- Reporting automatisé et aide à la décision
- Anonymisation et confidentialité des données

---

##  Technologies

### BI & Data
`Power BI` · `SQL Server` · `SQL / Data Warehouse` · `ETL` · `CSV / Excel` · `Modélisation dimensionnelle` · `Data Analysis` · `DAX` · `Power Query` · `KPI Analysis` · `Healthcare Analytics` · `Statistical Analysis`

### Développement & Déploiement
`Git / GitHub` · `Power BI Desktop` · `SQL Server Management Studio (SSMS)`

---

##  Modèle de données

Le projet suit une approche de modélisation dimensionnelle basée sur une architecture **Fact / Dimension**.

### Table de faits

**`Fact_Admission`**
- Informations d'admission
- Dates d'admission et de sortie
- Assurance
- Indicateur ICU
- Indicateur de décès à l'hôpital
- Type d'admission
- Lieu d'admission
- Lieu de sortie

### Tables de dimensions

| Table | Attributs |
|---|---|
| `Dim_Patient` | Démographie, date de naissance, genre, ethnicité, statut marital |
| `Dim_Date` | Année, mois, trimestre, semestre, semaine, jour |
| `Dim_Location` | Lieu d'admission, lieu de sortie, catégorie de service |
| `Dim_TypeAdmission` | Type, niveau, classe d'admission, indicateur d'urgence, description |
| `Dim_Assurance` | Assurance, catégorie et nom de l'assurance |

---

##  Architecture

Pipeline d'analyse healthcare de bout en bout intégrant sources CSV/Excel, ETL, Data Warehouse dimensionnel et dashboards Power BI.

```
CSV / Excel
     │
     ▼
Ingestion & ETL
     │
     ▼
Nettoyage & Transformation
     │
     ▼
SQL Server / Data Warehouse
     │
     ├── Dim_Patient
     ├── Dim_Date
     ├── Dim_Location
     ├── Dim_TypeAdmission
     └── Dim_Assurance
     │
     ▼
Fact_Admission
     │
     ▼
Modèle de données Power BI
     │
     ▼
Dashboards interactifs
     │
     ▼
Aide à la décision hospitalière
```

---

##  Dashboards

### 1. Admissions
- Total des admissions
- Admissions par période
- Admissions par type et par lieu
- Admissions par assurance
- Admissions ICU / urgences
- Tendances des admissions

### 2. Analyse Patient & Séjour
- Nombre de patients
- Durée de séjour moyenne / maximale
- Analyse des séjours en ICU
- Analyse des sorties d'hôpital
- Durée de séjour par type d'admission et caractéristiques patient

### 3. Performance médicale
- Taux de mortalité
- Analyse des décès à l'hôpital
- Suivi de la mortalité en ICU
- Tendances des admissions par catégorie médicale

### 4. Ressources & Analyse opérationnelle
- Indicateurs d'utilisation des ICU
- Volumes d'admissions/sorties
- Activité hospitalière par service
- Identification des séjours prolongés
- Suivi des KPI opérationnels

---

##  KPIs

- Total Admissions
- Total Patients
- ICU Admissions
- Emergency Admissions
- Average Length of Stay
- Maximum Length of Stay
- Mortality Rate
- Hospital Expiration Rate
- Admissions by Period / Location / Type / Insurance

---

##  Pipeline ETL

**Extract**
- Fichiers CSV / Excel
- Datasets cliniques hospitaliers
- Datasets administratifs

**Transform**
- Nettoyage des données
- Détection des doublons
- Gestion des valeurs manquantes
- Standardisation des types de données
- Transformation des dates
- Anonymisation des données
- Contrôles d'intégrité référentielle

**Load**
- Chargement des données nettoyées dans le Data Warehouse, connecté à Power BI

---

##  Objectifs métier

- Améliorer l'efficacité opérationnelle des hôpitaux
- Suivre les admissions et l'activité ICU
- Analyser les séjours des patients
- Suivre les indicateurs de performance santé
- Faciliter l'allocation des ressources
- Faciliter la prise de décision stratégique
- Automatiser le reporting santé

---

##  Confidentialité & sécurité

- Anonymisation des patients
- Accès restreint aux informations sensibles
- Stockage sécurisé
- Contrôle d'accès basé sur les rôles
- Protection des informations cliniques et administratives

---

##  Améliorations futures

- Modélisation prédictive de la réadmission hospitalière
- Prédiction de la durée de séjour
- Prévision de la demande en ICU
- Stratification du risque patient
- Prévision de la demande en ressources
- Détection automatisée d'anomalies
- Intégration de datasets cliniques supplémentaires