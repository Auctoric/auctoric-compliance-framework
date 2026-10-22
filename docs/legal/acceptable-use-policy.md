# Acceptable Use Policy (AUP)

**Document Reference:** AUC-LEG-AUP-001  
**Version:** 3.1  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal & Safety  
**Harmonized Upstream Policies:** Google Cloud Generative AI Prohibited Use Policy | Microsoft Azure OpenAI Code of Conduct | Anthropic Usage Policy | EU AI Act (Reg (EU) 2024/1689, Art. 5)

---

## 1. Overview and Purpose

This Acceptable Use Policy ("**AUP**") defines the mandatory boundaries, safety restrictions, and prohibited practices governing the use of the **Auctoric Governed AI Platform**, APIs, developer SDKs, autonomous agent frameworks, and inference endpoints (collectively, the "**Services**").

Because Auctoric orchestrates workloads on top of leading hyperscalers (including **Google Cloud Platform / Vertex AI**, **Microsoft Azure**, and **Anthropic**), **this AUP directly incorporates and harmonizes with the most restrictive policies in our technology stack**. Any activity prohibited by our upstream providers is strictly prohibited on Auctoric. Every customer, developer, and user accessing the Services must comply with this AUP.

---

## 2. Harmonized Prohibited AI Practices

You agree not to use the Services, or allow any third party to use the Services, for any of the following prohibited activities:

### 2.1 Healthcare & Clinical Decision-Making (Google Cloud Alignment)
1. **Automated Medical Diagnosis:** Providing automated, unsupervised clinical diagnostic assessments, medical triage, or patient care instructions;
2. **Prescription & Treatment Planning:** Generating, modifying, or authorizing pharmaceutical prescriptions or medical treatment plans. Neither the presence of licensed professional supervision, nor a customer’s regulated healthcare status, nor the execution of a HIPAA Business Associate Agreement authorizes a clinical use prohibited by an underlying foundation model provider;
3. **Medical Device Functionality:** Operating the platform as an uncertified Software-as-a-Medical-Device (SaMD) subject to FDA, EMA, or EU MDR 2017/745 regulatory approval. Non-clinical administrative healthcare workflows (such as scheduling or billing drafting) are permitted where verified by administrative staff before finalization.

### 2.2 Critical Infrastructure & Kinetic Systems (Google & Anthropic Alignment)
1. **Critical Infrastructure Control:** Deploying autonomous agentic workflows to directly monitor, operate, or control nuclear energy facilities, electric power grids, water treatment plants, or public utility distribution networks;
2. **Transportation & Life-Safety:** Operating real-time air traffic control systems, autonomous vehicular navigation, emergency 911 dispatch routing, or life-support medical equipment;
3. **Autonomous Physical Action:** Interfacing agentic tool-execution endpoints with physical actuators, robotics, or industrial machinery without air-gapped deterministic emergency stop overrides.

### 2.3 Weapons, CBRN, and Physical Violence
1. **CBRN Materials:** Designing, synthesizing, weaponizing, or optimizing Chemical, Biological, Radiological, or Nuclear (CBRN) agents, pathogens, or delivery mechanisms;
2. **Kinetic Weaponry:** Generating actionable manufacturing schematics or operational instructions for firearms, 3D-printed ghost guns, explosives, or improvised military devices;
3. **Violence & Self-Harm:** Facilitating, inciting, or encouraging acts of suicide, self-harm, terrorism, or physical violence against individuals or groups.

### 2.4 EU AI Act Prohibited Practices (Regulation (EU) 2024/1689, Article 5)
1. **Subliminal Cognitive Manipulation:** Deploying subliminal or purposefully manipulative techniques to materially distort an individual’s behavior, impairing informed decision-making in a manner causing physical or psychological harm;
2. **Exploitation of Vulnerabilities:** Exploiting vulnerabilities related to age, physical or mental disability, or socioeconomic circumstance to distort behavior;
3. **Social Scoring:** Evaluating or classifying natural persons based on social behavior or personality traits leading to discriminatory or unjustified detrimental treatment;
4. **Biometric Categorization of Sensitive Traits:** Deducing race, political opinions, trade union membership, religious beliefs, or sexual orientation via biometric categorization;
5. **Workplace Emotion Inference:** Using emotion recognition algorithms in workplace or educational environments (unless deployed strictly for validated medical or physical safety reasons).

### 2.5 Cyberattacks, Exploitation, and Model Distillation
1. **Malicious Payloads:** Generating polymorphic malware, ransomware, exploit scripts, or automated vulnerability scanning tools for unauthorized target exploitation;
2. **Adversarial Jailbreaking & Attacks:** Conducting prompt injection attacks, model inversion, or safety classifier bypasses against Auctoric or upstream hyperscaler infrastructure (except for authorized, good-faith security research conducted in strict accordance with the [Vulnerability Disclosure Policy](../technical-standards/vulnerability-disclosure-policy.md));
3. **Anti-Model Distillation:** Using inference outputs to train, fine-tune, bootstrap, or calibrate any machine learning or foundation model that competes with Auctoric, Google Cloud, Microsoft Azure, or Anthropic;
4. **Credential Harvesting & Phishing:** Orchestrating automated spear-phishing, credential stuffing, or social engineering campaigns.

### 2.6 Fraud, Deception, and High-Risk Profiling
1. **Electoral & Civic Deception:** Operating automated bots or generating synthetic deepfake media intended to suppress voter turnout, deceive voters, or undermine democratic electoral processes;
2. **Synthetic Media Impersonation:** Creating synthetic depictions of real human beings without prominent, clear watermarking and disclosure of its artificial origin;
3. **Child Exploitation (CSAM):** Generating, distributing, or facilitating Child Sexual Abuse Material (CSAM) or Child Sexual Exploitation and Abuse (CSAE)—violations will be reported immediately to NCMEC and federal law enforcement;
4. **Unsupervised Statutory ADM:** Making fully automated decisions producing legal effects (e.g., credit denial, mortgage qualification, tenancy screening, employment termination) without meaningful human oversight and explainability.

---

## 3. High-Risk Deployer Obligations

If Customer utilizes Auctoric to power High-Risk AI Systems as classified under Annex III of the EU AI Act or critical systems under NIST AI RMF:
* **Human-in-the-Loop (HITL):** Customer must maintain meaningful human review mechanisms capable of rejecting, overriding, or modifying platform-generated recommendations.
* **Incident Escalation:** Customer must notify Auctoric at `[compliance@auctoric.ai]` within forty-eight (48) hours of becoming aware of any systemic algorithmic failure, discrimination incident, or regulatory inquiry.
* **Auditability:** Customer must maintain complete prompt context logs and human sign-off records as required by [Schedule 1: AI Service-Specific Terms](ai-service-specific-terms.md).

---

## 4. Platform Safety Guardrails & Runtime Classifiers

To maintain compliance with Google Cloud and our multi-cloud hyperscaler stack:
* Auctoric deploys multi-stage, privacy-preserving runtime classifiers analyzing prompts and completions in volatile memory.
* Filters automatically tokenize PII/PCI strings, intercept prompt injection vectors, and block prohibited CBRN, cyberweapon, and toxic content.
* Circumventing, tampering with, or attempting to evade these runtime filters is a material violation of this Policy.

---

## 5. Violations, Enforcement, and Upstream Reporting

### 5.1 Enforcement Hierarchy
Upon discovering or receiving a credible report of an AUP violation, Auctoric may:
1. Issue formal compliance remediation warnings;
2. Impose real-time rate throttles or restrict specific model routes;
3. Immediately suspend API keys or terminate the customer account where reasonably necessary to protect platform stability or comply with law, providing notice and identifying restoration conditions as soon as practicable;
4. Report severe violations (including CSAM, terrorist content, or critical infrastructure threats) to law enforcement and national market surveillance authorities.

### 5.2 Upstream Hyperscaler Escalation
If a violation involves an upstream provider’s model endpoint (e.g., Google Vertex AI or Azure OpenAI), Auctoric will cooperate with upstream Trust & Safety investigators and comply with mandatory reporting obligations under our enterprise hyperscaler agreements.

### 5.3 Appeals Process
If you believe a request was blocked or an account suspended due to an erroneous classification or false positive:
* Submit an appeal to `[appeals@auctoric.ai]` within fourteen (14) days;
* Include account ID, transaction hash/timestamp, and technical justification;
* The Auctoric AI Safety & Compliance Committee will review and respond within five (5) business days.

---

## 6. Reporting Violations

* **Email:** `[safety@auctoric.ai]` or `[trust@auctoric.ai]`
* **Online Incident Form:** `[https://auctoric.ai/safety/report-violation]`
* **Coordinated Vulnerability Disclosures:** Refer to [Vulnerability Disclosure Policy](../technical-standards/vulnerability-disclosure-policy.md) and [.well-known/security.txt](../../.well-known/security.txt)
