# AI-Driven-Hybrid-Cybersecurity-Audit-Framework-for-Non-Governance-IT-Systems

---

## One-line summary
An AI driven hybrid framework that integrates classical machine-learning anomaly detection with LLM-based audit reasoning to automatically identify, assess, and explain security risks in non-governance IT systems then get human to validate.

---

## Project status
**Phase:** Functional prototype and evaluation

**Deliverables:** Prototypes(ML model results, LLM integration demo), compliance mapping, bibliography, evaluation results, final report, and presentation.

---

## Motivation
Small and medium private organizations rarely have the resources for deep cybersecurity audits. A hybrid system can help with low-risk handling and make auditing more scalable. This allows human auditors focus on more high-impact issues.

---

## Research objectives
* **RO1 - Feasibility:** Implement and evaluate multiple ML models on the UNSW-NB15 dataset for intrusion and anomaly detection.
*  **RO2 — Hybrid Intelligence:** Combine ML outputs with a Large Language Model(OpenAI) to generate structured audit findings, control mappings, and remediation steps.
*  **RO3 — Evaluation:** Compare model performance and test LLM interpretability, reliability, and token limits.
*  **RO4 — Recommendations:** Identify limitations, ethical issues, and next steps. Assess whether LLM-based reasoning is credible for auditing tasks or if results depend more on dataset quality and prompt design.

---

## Prototype overview
**High-level flow**
Data ingestion + preprocessing: Clean UNSW-NB15 network traffic dataset.

ML classification:

Models: Isolation Forest, Logistic Regression, Gradient Boosting, XGBoost.

Logistic Regression for explainable, auditable baselines.

XGBoost for higher recall and aggressive threat catching.

Evidence generation: Top-risk predictions exported as JSON evidence.

LLM reasoning: OpenAI GPT-4o-mini converts evidence into audit incidents, risk scores, control mappings, and remediation recommendations.

Human-in-the-loop review: Analysts verify or adjust the LLM’s suggested incidents.

Results visualization: Confusion matrices, ROC/PR curves, and JSON-formatted incident reports in the audit_ml_models/results folder.

---

## Key Findings
Logistic Regression achieved ≈ 85% accuracy / 0.86 F1, best overall balance.

XGBoost achieved ≈ 0.76 F1, with stronger recall for attacks.

Isolation Forest over-flagged anomalies but served as a good pre-filter.

LLM successfully produced a structured incident report after prompt optimization, output quality heavily depends on prompt clarity + evidence size rather than raw model accuracy.


---

## Loom Recordings
**Begin watching in order**
1. https://www.loom.com/share/deba290d5bbe484d9c08340cd78b7496?sid=0ee2ebff-36b8-42d9-8f8d-70b3bb16697d
2. https://www.loom.com/share/cb82c9d5b63a43bd9d5422260bbf7f71?sid=880a6ab2-be7f-4363-8f7f-6a9aa701efe3
3. https://www.loom.com/share/7dd9e5a915474e3a8d27727481d38014?sid=ec876fa5-e417-4a2c-b5a8-aa8145d8f56c
