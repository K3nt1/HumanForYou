# Ethics in Artificial Intelligence: The HumanForYou Attrition Project

## Addressing Employee Turnover with Responsible AI

| Project Group Members | Role |
| :--- | :--- |
| **El Meskine Anas** | ** |
| **Haider Maisam** | *Project Manager* |
| **Ferchichi Haifa** | ** |
| **Gautier Quentin** | ** |

---

## Table of Contents

1.  [Project Context and Problem Statement](#1-project-context-and-problem-statement)
2.  [Ethical Methodology and Approach](#2-ethical-methodology-and-approach)
3.  [The Seven Key Ethical Requirements](#3-the-seven-key-ethical-requirements)
    * [3.1. Respect for Human Autonomy](#31-respect-for-human-autonomy)
    * [3.2. Technical Robustness and Security](#32-technical-robustness-and-security)
    * [3.3. Data Privacy and Governance](#33-data-privacy-and-governance)
    * [3.4. Transparency](#34-transparency)
    * [3.5. Diversity, Non-discrimination, and Fairness](#35-diversity-non-discrimination-and-fairness)
    * [3.6. Environmental and Societal Well-being](#36-environmental-and-societal-well-being)
    * [3.7. Accountability](#37-accountability)
4.  [Key Ethical Decisions and Vigilance Points](#4-key-ethical-decisions-and-vigilance-points)
5.  [Conclusion](#5-conclusion)
6. [Resources and Bibliography](#6--resources-and-bibliography)
    * [6.1. Ethical and Regulatory Sources (Compliance and Framework)](#61-ethical-and-regulatory-sources-compliance-and-framework)
    * [6.2. Technical and Methodological Sources (Fairness & Transparency)](#62-technical-and-methodological-sources-fairness--transparency)
    * [6.3. Project-Specific Sourcess (AI in HR Context)](#63-project-specific-sources-ai-in-hr-context)

---

## 1. Project Context and Problem Statement

The HumanForYou pharmaceutical company faces an annual employee **attrition rate of approximately 15%**. This project aims to utilize data analysis and AI models to **identify the key factors influencing employee turnover** and to **propose data-driven recommendations** to improve employee retention.

While the goal is beneficial to the company, the use of sensitive HR data and predictive modeling necessitates a rigorous ethical framework to ensure that the solution is fair, non-discriminatory, and respects employee rights.

---

## 2. Ethical Methodology and Approach

Our ethical methodology is integrated throughout the project lifecycle, from data collection/preparation to final model deployment and recommendation generation.

* **Approach:** We adopt a **"Privacy by Design"** and **"Fairness by Design"** approach, ensuring ethical considerations guide technical decisions. Team discussions involve dedicated checkpoints to review ethical implications before moving to the next phase (e.g., before feature selection and before final model selection).
* **Guiding Framework:** Our analysis is structured around the **seven key requirements for trustworthy AI** as defined by the European Commission.

---

## 3. The Seven Key Ethical Requirements

### 3.1. Respect for Human Autonomy

**Focus:** Ensuring employees retain control and are not coerced or manipulated by the AI's recommendations.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Recommendation Scope** | The AI model must only generate **macro-level recommendations** (e.g., increase salary in department X, improve work-life balance in role Y), **not individual employee risk scores** used for punitive actions. |
| **Human Oversight** | **Final decisions** on policy changes and interventions **must remain with HR/Management**. The AI serves as an advisory tool, not a decision-maker. |

### 3.2. Technical Robustness and Security

**Focus:** Ensuring the AI system is reliable, secure, and accurate in its predictions.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Model Validation** | Rigorous use of **cross-validation** and deployment metrics like **precision, recall, and F1-score** (focusing on the minority class: Attrition) to ensure reliability. |
| **Data Security** | All sensitive data processing is conducted in a **secure, authorized environment**. Data is treated as **anonymized** (using `EmployeeID` as a unique identifier only within the project scope). |

### 3.3. Data Privacy and Governance

**Focus:** Protecting the sensitive employee information used to train the model.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Data Minimization** | Exclusion of any personally identifiable information (PII) beyond what was strictly provided and necessary (`EmployeeID` is not PII but serves as a linkage key). Variables like `EmployeeCount` and `Over18` (redundant) were **dropped to reduce data footprint**. |
| **Data Retention** | A clear policy must be established with HumanForYou management regarding the **destruction of the derived dataset** and the original files upon project completion. |

### 3.4. Transparency

**Focus:** Ensuring the model's workings and recommendations are understandable and explainable.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Model Choice** | Prioritizing **interpretable models** (e.g., Logistic Regression, Decision Trees) or using **Explainable AI (XAI)** techniques (e.g., SHAP, LIME) alongside complex models (e.g., Gradient Boosting) to articulate *why* a factor drives attrition. |
| **Documentation** | Clear and comprehensive documentation of the **data processing steps** and the **model's limitations** for the client. |

### 3.5. Diversity, Non-discrimination, and Fairness

**Focus:** Preventing the model from learning or amplifying existing biases based on protected characteristics (Gender, Age, etc.).

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Bias Mitigation** | Careful monitoring of **disparate impact** across sensitive groups (e.g., Gender, Marital Status) regarding the predicted attrition risk. If gender or age are strong predictors, recommendations must focus on underlying *actionable* factors (e.g., low salary for a specific role/level, not gender itself). |
| **Fairness Metrics** | Analysis of **parity metrics** (e.g., Equal Opportunity Difference) to ensure the model performs equally well for different employee subgroups. |

### 3.6. Environmental and Societal Well-being

**Focus:** Ensuring the solution contributes positively and avoids negative environmental or societal consequences.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Societal Benefit** | The primary goal (reducing turnover) contributes to **societal well-being** by improving job stability, reducing operational stress, and fostering a better workplace. |
| **Computational Efficiency** | Choice of models and training methods that are **computationally efficient** to minimize the environmental footprint (energy consumption) associated with AI training and inference. |

### 3.7. Accountability

**Focus:** Clearly defining who is responsible for the outcome and the compliance of the AI system.

| Ethical Decision/Vigilance Point | Justification/Implementation |
| :--- | :--- |
| **Team Accountability** | The **project team** is accountable for the model's validity and the ethical review process documented herein. |
| **Client Accountability** | **HumanForYou Management/HR** is accountable for the *use* and *impact* of the recommendations generated by the model on employees and company policies. |

---

## 4. Key Ethical Decisions and Vigilance Points

* **Decision 1: Focus on Actionable Insights.** We decided not to build a high-risk prediction system identifying individuals, but rather an **explanatory system** identifying systemic weaknesses (e.g., "Employees with < 2 years at the company and low Job Satisfaction are at high risk"). This maintains autonomy.
* **Vigilance Point 1: Work-Life Balance and Overtime.** The analysis of the `in_out_time` data must ensure that excessive working hours are identified as a **risk factor for attrition** and not used to punish employees with low commitment scores.
* **Vigilance Point 2: Salary/Performance Bias.** Care must be taken to ensure that the model does not penalize historically underpaid roles or demographic groups simply because their low salary is a strong predictor of leaving. Recommendations must address the underlying **equity issue**.

---

## 5. Conclusion

By integrating the seven ethical requirements of the European Commission into our methodology, we ensure that the AI solution developed for HumanForYou is not only effective in reducing employee turnover but is also **fair, transparent, and respectful** of human autonomy and data privacy. The model's primary function is to **empower the HR department** with systemic insights, allowing them to make **ethically sound, human-centered policy decisions**.

## 6. Resources and Bibliography

This section lists the key academic, technical, and regulatory sources that guided the ethical framework and methodological choices for the HumanForYou AI project.

### 6.1. Ethical and Regulatory Sources (Compliance and Framework)

These sources define the foundational ethical principles and regulatory requirements that the project adheres to.

| Source/Reference | Compliance & License | Annotation/Contribution |
| :--- | :--- | :--- |
| **European Commission (EC):** *Ethics Guidelines for Trustworthy AI (High-Level Expert Group on AI - HLEG)* | Public Domain/EC Publication | **Foundation of the Ethical Approach.** Details the seven key requirements (Human Autonomy, Robustness, Fairness, etc.) used to structure this document and guide ethical checkpoints throughout the project lifecycle. |
| **European Commission (EC):** *Proposal for a Regulation on a European Approach for Artificial Intelligence (AI Act)* | Public Domain/EC Publication | Provides the context for classifying the AI system (HR/attrition modeling is often considered high-risk) and informs the need for rigorous accountability and transparency measures. |

### 6.2. Technical and Methodological Sources (Fairness & Transparency)

These references justify the technical tools and methods chosen to ensure the fairness and explicability of the AI model.

| Source/Reference | Compliance & License | Annotation/Contribution |
| :--- | :--- | :--- |
| **Ribeiro, M. T., Singh, S., & Guestrin, C. (2016).** *"Why Should I Trust You? Explaining the Predictions of Any Classifier."* (KDD '16) | Academic/Standard Copyright | **Technical Justification for Transparency.** Introduces **LIME** (Local Interpretable Model-agnostic Explanations), a key method for locally justifying model predictions to stakeholders and ensuring transparency (Section 3.4). |
| **Lundberg, S. M., & Lee, S. I. (2017).** *"A Unified Approach to Interpreting Model Predictions."* (NeurIPS '17) | Academic/Standard Copyright | **Technical Justification for Transparency.** Introduces **SHAP** (SHapley Additive Explanations), utilized to calculate feature importance and articulate *why* specific factors (e.g., Job Satisfaction, distance) drive attrition, aiding in ethical root cause analysis. |
| **IBM.** *AI Fairness 360 (AIF360) Toolkit Documentation.* | Open Source License (Apache 2.0) | **Technical Justification for Fairness.** A practical toolkit providing metrics (Disparate Impact, Equal Opportunity Difference) and mitigation algorithms to test and ensure the model does not propagate historical biases across sensitive groups (Section 3.5). |

### 6.3. Project-Specific Sources (AI in HR Context)

These sources inform the ethical challenges and best practices specific to implementing predictive AI systems in the Human Resources domain.

| Source/Reference | Compliance & License | Annotation/Contribution |
| :--- | :--- | :--- |
| **Deloitte.** *Mobilising AI: Unlocking new experiences and insights to manage your global workforce.* (July 2025). | Commercial Report / Consulting Publication | **Specific HR Ethical and Risk Framework.** This guide provides a set of essential risks and considerations for applying AI/GenAI in HR and Payroll. It is used to justify: <ul><li>The necessity of **Human Oversight** to validate errors and biases, as AI is not infallible.</li><li>The importance of **Transparency and Explainability** in cases of decision-making assistance (risk management or calculations).</li><li>The risk of **Data Bias**: the document insists that training data must be representative and free from inherent biases to prevent discrimination.</li><li>The relevance of analyzing attendance data (`in_out_time`) to **predict wellbeing concerns** and salary equity.</li></ul> |
| **4Spot Consulting.** *Strategic HR Data Governance: 7 Essential Principles.* | Consulting/Industry Publication | **Data Governance and Privacy Foundation.** This resource establishes fundamental principles for managing sensitive employee data, crucial for meeting the "Data Privacy and Governance" requirement. It justifies the project's adherence to policies concerning **data quality, data access control, security, and compliance** before and during the modeling phase (Section 3.3). |