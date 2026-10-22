# ISO 42001 & EU AI Act Governance Policy

**Document Reference:** AUC-AIG-POL-001  
**Version:** 2.1  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Corporate Governance / Public Trust  
**Regulatory Baselines:** ISO/IEC 42001:2023 (AIMS) Control Criteria | Regulation (EU) 2024/1689 (EU AI Act) | NIST AI RMF 1.0

---

## 1. Purpose and Executive Summary

**Auctoric, LLC** ("**Auctoric**") is committed to engineering, deploying, and governing trustworthy, robust, and ethical Artificial Intelligence systems. This Policy establishes Auctoric’s **Artificial Intelligence Management System (AIMS)** framework aligned with **ISO/IEC 42001:2023** control criteria and operationalizes compliance obligations under the **European Union Artificial Intelligence Act (EU AI Act, Regulation (EU) 2024/1689)**.

As a provider of enterprise Governed AI infrastructure, Auctoric establishes verifiable controls spanning model risk classification, human oversight, transparency, data provenance, robustness, and post-market monitoring across the AI system lifecycle.

---

## 2. Governance Structure & Roles

```mermaid
flowchart TD
    Board["Auctoric Board of Directors & Executive Leadership"] --> AIC["AI Ethics & Safety Steering Committee"]
    AIC --> CAIGO["Chief AI Governance Officer (CAIGO)"]
    AIC --> CISO["Chief Information Security Officer (CISO)"]
    CAIGO --> AIRM["AI Risk & Validation Working Group"]
    CAIGO --> LegPriv["Legal & Privacy Operations"]
    CISO --> RedTeam["AI Red Team & Safety Engineering"]
    AIRM --> MLOps["ML Engineering & Deployment Teams"]
```

### 2.1 AI Ethics & Safety Steering Committee
The Steering Committee meets regularly to review high-risk use cases, systemic risk evaluations, algorithmic fairness benchmarks, and regulatory alignment across jurisdictions.

### 2.2 Key Roles & Responsibilities
* **Chief AI Governance Officer (CAIGO):** Accountable for overall AIMS compliance, AI conformity reviews, and regulatory liaison.
* **Chief Information Security Officer (CISO):** Directs adversarial red-teaming, prompt injection mitigations, and technical security controls (ISO/IEC 27001 / OWASP LLM Top 10).
* **AI Safety Engineers:** Validate guardrail performance, toxicity benchmarks, data lineage, and model card completeness.
* **Customer Deployers:** Accountable for deployer obligations under Article 26 of the EU AI Act when integrating Auctoric APIs into downstream applications.

---

## 3. EU AI Act Classification and Risk Tiering

Auctoric enforces a formal risk triage process prior to offering any AI model, tool, or autonomous agent capability:

| Tier | EU AI Act Classification | Auctoric Platform Implementation | Permitted Deployment Status |
| :--- | :--- | :--- | :--- |
| **Tier 1: Prohibited** (Art. 5) | Subliminal manipulation, social scoring, biometric categorization for sensitive attributes, untargeted facial scraping, workplace emotion inference. | Hardcoded runtime architectural guardrails; strictly forbidden via Acceptable Use Policy. | **STRICTLY PROHIBITED** |
| **Tier 2: High-Risk** (Art. 6 & Annex III / Annex I) | Critical infrastructure, education admissions, employment screening, essential public services, law enforcement assistance, credit scoring. | Subject to Continuous Risk Management (Art. 9), Data Governance (Art. 10), Technical Documentation (Art. 11), Automatic Logging (Art. 12), and Human Oversight (Art. 14). *(Note: Operative compliance deadlines under EU AI Act: December 2, 2027 for Annex III; August 2, 2028 for Annex I).* | **PERMITTED WITH AUDITED CONTROLS & DUAL AUTHORIZATION** |
| **Tier 3: Specific Transparency / GPAI** (Art. 50 & 51) | General-Purpose AI (GPAI) models with systemic risk, conversational AI, deepfakes, synthetic text/media. | Synthetic content disclosure banners, transparency model cards, copyright compliance summaries, C2PA metadata provenance. | **PERMITTED WITH MANDATORY DISCLOSURES** |
| **Tier 4: Minimal Risk** (Art. 95 / Chapter IX) | AI-enabled search indexing, automated code completion, spam filters, administrative optimization. | Adherence to Auctoric Responsible AI Principles and voluntary codes of conduct. | **PERMITTED UNDER STANDARD POLICY** |

---

## 4. ISO/IEC 42001 AI Management System (AIMS) Control Criteria

Auctoric designs its processes to align with the core control domains established by ISO/IEC 42001:2023:

### 4.1 AI Policy and Context (Clause 4 & 5)
Auctoric reviews internal AI governance objectives, societal impact assessments, and stakeholder expectations on a semi-annual cadence.

### 4.2 AI Risk Assessment & Treatment (Clause 6 & Annex A.5)
* **Risk Identification:** Evaluation of algorithmic bias, model drift, data poisoning, prompt injection (OWASP LLM01), sensitive data disclosure (LLM06), and hallucinations.
* **Treatment Protocols:** Implementation of real-time input/output guardrails, retrieval-augmented grounding (RAG), and deterministic confidence thresholds.

### 4.3 Data Governance for AI (Annex A.6)
* **Data Lineage:** Complete tracking of fine-tuning corpuses and synthetic benchmark sources using structured manifests.
* **Bias & Fairness Mitigation:** Pre-deployment statistical parity, disparate impact analysis, and demographic representation reviews across datasets.
* **Data Minimization:** Exclusion of unnecessary PII from training pipelines using automated masking and differential privacy.

### 4.4 Model Development, Verification & Validation (Annex A.7)
* Models undergo structured offline benchmarking across standardized evaluations (MMLU, HELM, TrustLLM) prior to promotion to staging.
* Adversarial red-teaming evaluating jailbreaks, prompt extraction, and multi-turn manipulation.

### 4.5 Post-Market Monitoring & Continuous Learning (Annex A.8)
* Telemetry monitoring model drift, latency, token throughput, and safety filter triggering rates.
* Regular calibration checks to ensure consistency and reliability over extended production cycles.

---

## 5. Technical Documentation & Logging (EU AI Act Articles 11 & 12)

For High-Risk AI configurations, Auctoric maintains technical documentation including:
1. System description, intended purpose, and authorized deployer profiles;
2. Algorithmic architecture specifications, model parameters, and training methodologies;
3. Dataset descriptions (provenance, curation methodology, and bias mitigation measures);
4. Risk management file detailing identified hazards, residual risks, and mitigation verifications;
5. Audit logs automatically capturing inference timestamps, user session tokens, model versions, prompt hashes, and guardrail trigger flags, retained for a minimum of twelve (12) months.

---

## 6. Transparency and User Disclosure (EU AI Act Article 50)

Auctoric provides automated transparency mechanisms ensuring that end-users are clearly informed when interacting with an AI system:
* **Interactive Agents:** System prompts explicitly announce the artificial nature of conversational interfaces (e.g., *"I am an AI assistant hosted on the Auctoric platform"*).
* **Synthetic Media & Text Provenance:** Machine-generated assets carry cryptographic C2PA provenance metadata verifying Auctoric origin.
* **Public Model Cards:** Published datasheets covering model architecture, limitations, evaluation metrics, and intended operational domains.

---

## 7. Serious Incident Reporting (EU AI Act Article 73)

### 7.1 Definition of Serious Incident
Any incident involving an Auctoric AI system that directly or indirectly leads to:
1. Death or serious harm to a person’s health;
2. Serious and irreversible disruption of critical infrastructure;
3. Breach of obligations under European Union law intended to protect fundamental rights;
4. Serious property or environmental damage.

### 7.2 Reporting Timelines Under Article 73
Auctoric will notify relevant market surveillance authorities and affected deployers without undue delay:
* **Immediate Notification:** Following establishment of a causal link or reasonable likelihood between the AI system and the serious incident.
* **Widespread / Critical Infrastructure Harm:** No later than **two (2) days** after becoming aware of the incident.
* **Death or Severe Health Impairment:** No later than **ten (10) days** after becoming aware of the incident.
* **General Outer Limit:** In any event, no later than **fifteen (15) calendar days** after becoming aware of the incident. Initial preliminary reports may be submitted where forensic investigations are ongoing.

---

## 8. Compliance Reviews & Internal Assurance

* **Internal Audits:** Conducted periodically by the compliance team in coordination with the CAIGO to evaluate operational adherence to AIMS controls.
* **Standards Alignment:** Controls and operational practices are designed to comply with ISO/IEC 42001:2023 criteria and applicable EU AI Act requirements.
* **Enforcement:** Non-compliance with this policy by Auctoric personnel is grounds for disciplinary action up to and including termination of employment.

---

## 9. Inquiries & Regulatory Contact

* **Chief AI Governance Officer:** `[caigo@auctoric.ai]`
* **AI Ethics & Safety Office:** `[ai-ethics@auctoric.ai]`
* **Official Postal Address:** `[Auctoric, LLC, 100 Enterprise Way, Suite 400, San Francisco, CA 94105]`
