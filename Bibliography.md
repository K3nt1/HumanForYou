# AI Project - Deliverable: Bibliography

| Project Group Members | Role |
| :--- | :--- |
| **El Meskine Anas** | *Data Analyst* |
| **Haider Maisam** | *Project Manager* |
| **Ferchichi Haifa** | *Data Engineer* |
| **Gautier Quentin** | *Machine Learning Engineer* |

---

This document presents the academic, technical, and industry references that guided our work on the HumanForYou project. The sources are organized by theme to clearly indicate their relevance to the concepts covered, the chosen methodologies, and the ethical decision-making process.

---

## Table of Contents

1. [Methodological and Theoretical Sources](#1-methodological-and-theoretical-sources)
2. [Sources on Technical Aspects](#2-sources-on-technical-aspects)
3. [Ethical and Societal Sources](#3-ethical-and-societal-sources)
4. [Project-Specific Sources](#4-project-specific-sources)

## 1. Methodological and Theoretical Sources

**Methodological and Theoretical Sources**

*(References dealing with the theoretical bases of machine learning, classification models, handling class imbalance, and HR analytics)*

| Source/Reference | Type / License | Contribution and Justification |
| :--- | :--- | :--- |
| **Hastie, T., Tibshirani, R., & Friedman, J.** *The Elements of Statistical Learning.* | Academic Textbook | Provides the theoretical foundations for the selection and validation of supervised learning algorithms (e.g., Logistic Regression, Tree-based methods) used for attrition classification. |
| **Chawla, N. V. et al.** *SMOTE: Synthetic Minority Over-sampling Technique.* | Academic Paper | Justifies the methodological approach used to address the class imbalance issue (15% attrition) through techniques like over-sampling (SMOTE) or using cost-sensitive learning metrics. |
| **Bersin, J.** *The HR Technology Landscape.* | Industry Report / Professional Book | Provides a strategic and managerial context for the project, validating the use of data-driven methods to address workforce problems like turnover and talent retention. |

---

## 2. Sources on Technical Aspects

**Sources on Technical Aspects**

*(References describing the specific techniques used: Python libraries, Feature Engineering for time series.)*

| Source/Reference | Type / License | Contribution and Justification |
| :--- | :--- | :--- |
| **Scikit-learn documentation.** | Open Source / Technical Docs | Justifies the implementation choices regarding model training, hyperparameter tuning (e.g., GridSearchCV), and the use of standard metrics (ROC AUC, Precision, Recall) for model evaluation. |
| **Atique, M., et al.** *Enhancing Employee Turnover Prediction: An Advanced Feature Engineering Analysis.* (Computer Systems Science and Engineering, 2025). | Academic Article (Open Access) | **Validation of Feature Engineering Strategy.** This recent study confirms that raw HR data is insufficient for accurate predictions without advanced transformation. The authors demonstrate that introducing specific engineered features significantly improves model accuracy (Recall/F1-Score) for turnover prediction, directly validating our approach of creating calculated features like `AverageWorkingHours` to better capture employee behavior. |

---

## 3. Ethical and Societal Sources

**Ethical and Societal Sources**

*(References relating to ethical standards, bias, and governance frameworks. Includes the European Commission's framework.)*

| Source/Reference | Type / License | Contribution and Justification |
| :--- | :--- | :--- |
| **European Commission (EC):** *Ethics Guidelines for Trustworthy AI (High-Level Expert Group on AI - HLEG)* | Regulatory / EC Publication | **Core Ethical Framework.** Establishes the seven core requirements (Fairness, Transparency, Accountability, etc.) that structure the ethical deliverable and guide the team's decisions regarding bias mitigation and human oversight. |
| **IBM.** *AI Fairness 360 (AIF360) Toolkit Documentation.* | Open Source / Apache 2.0 License | Justifies the **technical approach to fairness and bias mitigation**. It supports the selection and calculation of fairness metrics (e.g., Disparate Impact, Equal Opportunity Difference) to ensure the model does not discriminate against protected groups (Section 3.5). |
| **Deloitte.** *Mobilising AI: Unlocking new experiences and insights to manage your global workforce.* (July 2025). | Commercial Report / Consulting Publication | Provides a **specific risk framework for AI in HR**, emphasizing the need for human validation, data privacy, and ethical compliance in predictive systems. It informs the definition of ethical vigilance points (Section 4). |

---

## 4. Project-Specific Sources

**Project-Specific Sources**

*(Sources that directly inspired the approach, the problem, or the management of similar cases.)*

| Source/Reference | Type / License | Contribution and Justification |
| :--- | :--- | :--- |
| **Kaggle:** *HR Analytics Case Study* (Original Data Source) | Data Repository / Community | Acknowledges the origin and the initial context of the dataset. Guides the team on common feature preparation steps and initial model benchmarks associated with this specific data. |
| **4Spot Consulting.** *Strategic HR Data Governance: 7 Essential Principles.* | Consulting/Industry Publication | Establishes fundamental **Data Governance principles** (Data Quality, Access Control) essential for handling sensitive employee data, thereby strengthening the compliance and privacy aspects of the project (Section 3.3). |
| **Singh, P., et al.** *A Case Study on HR Analytics Employee Attrition Using Predictive Analytics.* (European Economic Letters, 2023). | Academic Article (Open Access) | **Validation of Pre-processing and Modeling methodology.** This study, conducted on a similar HR dataset, provides the academic justification for: <ul><li>**Handling Missing Data**: It supports the strategy of cleaning survey data (imputing or removing nulls) before modeling.</li><li>**Feature Selection**: It confirms the importance of converting categorical variables (like Job Role or Department) into numerical values (Encoding).</li><li>**Model Benchmarking**: It validates the relevance of comparing multiple algorithms (Logistic Regression vs. Random Forest) to solve the specific problem of employee turnover.</li></ul> |