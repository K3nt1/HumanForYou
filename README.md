# 🤖 IA for HumanForYou

## 🇫🇷 Français

### Introduction

Ce projet d'**Analyse de Données et d'Intelligence Artificielle** est mené pour la société pharmaceutique indienne **HumanForYou**, qui emploie environ 4000 personnes. L'entreprise est confrontée à un taux de rotation annuel des employés (turnover) d'environ **15%**. Ce niveau de turnover est jugé préjudiciable en raison des retards de projet, des coûts de recrutement et de la perte de temps due à la formation des nouveaux employés.

L'objectif principal est de **déterminer les facteurs les plus influents** sur ce taux de rotation et de **proposer des modèles prédictifs** pour identifier les domaines d'amélioration afin de motiver les employés à rester au sein de l'entreprise.

### 🚀 Objectifs du Projet

1.  **Analyse Exploratoire des Données (EDA)**: Comprendre la structure des données et identifier les tendances initiales.
2.  **Ingénierie des Caractéristiques**: Préparer les données (nettoyage, gestion des valeurs manquantes 'NA' dans l'enquête, fusion des fichiers `in_out_time`, création de nouvelles variables pertinentes, gestion des variables catégorielles).
3.  **Analyse des Facteurs d'Attrition**: Déterminer les variables ayant la plus grande influence sur la décision d'un employé de quitter l'entreprise (`Attrition`).
4.  **Modélisation Prédictive**: Développer des modèles d'IA (classification) capables de prédire l'attrition future des employés.
5.  **Recommandations**: Proposer des zones d'amélioration concrètes pour la Direction, basées sur l'interprétation des meilleurs modèles, afin de réduire le taux de rotation.

### 📁 Données Fournies

Les données sont fournies sous forme de fichiers CSV anonymisés, tous liés par l'`EmployeeID`.

| Fichier | Description | Données Clés |
| :--- | :--- | :--- |
| `general_data.csv` | Informations RH générales (âge, salaire, ancienneté, rôle, etc.). **Contient la variable cible : `Attrition`**. | `Age`, `JobRole`, `MonthlyIncome`, `YearsAtCompany`, `Attrition`, etc. |
| `manager_survey_data.csv` | Évaluations des managers de Février 2015. | `JobInvolvement`, `PerformanceRating` |
| `employee_survey_data.csv` | Enquête QVT (Qualité de Vie au Travail) de Juin 2015. Contient des valeurs **"NA"**. | `EnvironmentSatisfaction`, `JobSatisfaction`, `WorkLifeBalance` |
| `in_out_time.zip` | Horaires d'arrivée et de départ des employés pour l'année 2015. | Timestamps à traiter pour calculer les heures travaillées, l'assiduité, etc. |

### 🛠 Livrables Attendus

1.  **AI Project - Deliverable: Ethics**: Document justifiant l'approche éthique du projet, conformément aux sept exigences de la Commission Européenne (respect de l'autonomie, robustesse technique, confidentialité des données, transparence, etc.).
2.  **AI Project - Deliverable: Bibliography**: Document listant et annotant les références académiques et techniques utilisées (méthodologiques, techniques, éthiques, spécifiques au projet).
3.  **AI Project - Presentation**: Présentation de 20 minutes couvrant l'approche globale : génération du *dataset* final, choix et justification des algorithmes d'IA, analyse des résultats et des métriques, amélioration du modèle, sélection finale et propositions concrètes pour le client. *(Le Jupyter Notebook sera également envoyé séparément)*.

---

## 🇬🇧 English

### Introduction

This **Data Analysis and Artificial Intelligence** project is being conducted for the Indian pharmaceutical company **HumanForYou**, which employs approximately 4,000 people. The company faces an annual employee turnover rate (attrition) of around **15%**. This level of turnover is considered detrimental due to project delays, recruitment costs, and the time loss associated with training new employees.

The primary objective is to **determine the most influential factors** on this turnover rate and to **propose predictive models** to identify areas for improvement that will motivate employees to stay with the company.

### 🚀 Project Objectives

1.  **Exploratory Data Analysis (EDA)**: Understand the data structure and identify initial trends.
2.  **Feature Engineering**: Prepare the data (cleaning, handling "NA" missing values in the survey, merging the `in_out_time` files, creating new relevant variables, managing categorical variables).
3.  **Attrition Factor Analysis**: Determine the variables that have the greatest influence on an employee's decision to leave the company (`Attrition`).
4.  **Predictive Modeling**: Develop AI models (classification) capable of predicting future employee attrition.
5.  **Recommendations**: Propose concrete areas for improvement to the Management, based on the interpretation of the best models, to reduce the turnover rate.

### 📁 Data Provided

The data is provided as anonymized CSV files, all linked by the `EmployeeID`.

| File | Description | Key Data |
| :--- | :--- | :--- |
| `general_data.csv` | General HR information (age, salary, seniority, role, etc.). **Contains the target variable: `Attrition`**. | `Age`, `JobRole`, `MonthlyIncome`, `YearsAtCompany`, `Attrition`, etc. |
| `manager_survey_data.csv` | Manager assessments from February 2015. | `JobInvolvement`, `PerformanceRating` |
| `employee_survey_data.csv` | QWL (Quality of Working Life) survey from June 2015. Contains **"NA"** values. | `EnvironmentSatisfaction`, `JobSatisfaction`, `WorkLifeBalance` |
| `in_out_time.zip` | Employee arrival and departure times for the year 2015. | Timestamps to be processed to calculate hours worked, attendance, etc. |

### 🛠 Expected Deliverables

1.  **AI Project - Deliverable: Ethics**: A document justifying the ethical approach of the project, in line with the seven requirements recommended by the European Commission (respect for human autonomy, technical robustness, data privacy, transparency, etc.).
2.  **AI Project - Deliverable: Bibliography**: A document listing and annotating the academic and technical references used (methodological, technical, ethical, project-specific).
3.  **AI Project - Presentation**: A 20-minute presentation covering the entire approach: generation of the final dataset, choice and justification of the AI algorithms, analysis of results and metrics, model improvement, final selection, and concrete proposals for the client. *(The Jupyter Notebook will also be sent separately)*.
