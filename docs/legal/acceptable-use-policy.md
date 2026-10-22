# Acceptable Use Policy (AUP)

**Document Reference:** AUC-LEG-AUP-001  
**Version:** 2.5  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal

---

## 1. Overview and Purpose

This Acceptable Use Policy ("**AUP**") defines the mandatory rules and boundaries governing the use of the **Auctoric** platform, APIs, developer SDKs, autonomous agent frameworks, and hosted AI inference endpoints (collectively, the "**Services**").

Auctoric provides enterprise-grade Governed AI infrastructure designed to empower organizations while strictly mitigating technological risks, algorithmic harm, and regulatory violations. Every user, developer, and organization accessing the Services must comply with this AUP.

---

## 2. Prohibited AI and Platform Uses

You agree not to use the Services, or allow any third party to use the Services, for any of the following prohibited activities:

### 2.1 EU AI Act Prohibited AI Practices (Regulation (EU) 2024/1689, Article 5)
1. **Subliminal & Deceptive Techniques:** Deploying cognitive behavioral manipulation techniques beyond human consciousness to materially distort an individual’s behavior in a manner that causes physical or psychological harm.
2. **Exploitation of Vulnerabilities:** Exploiting vulnerabilities of individuals due to age, disability, or specific social or economic situation to distort their behavior.
3. **Biometric Categorization & Social Scoring:** Evaluating or classifying natural persons based on social behavior or personality traits leading to discriminatory treatment; or deducing race, political opinions, trade union membership, religious beliefs, or sexual orientation via biometric categorization.
4. **Real-Time Remote Biometric Identification:** Deploying real-time remote biometric identification in publicly accessible spaces for law enforcement purposes, except as strictly permitted under Article 5(1)(h) of the EU AI Act.
5. **Emotion Recognition in Workplaces and Educational Institutions:** Utilizing inference algorithms to infer emotional states in employment or academic environments, unless deployed strictly for medical or safety reasons.

### 2.2 Cyberattacks, Exploitation, and Malicious Software
1. Generating, optimizing, or deploying computer viruses, rootkits, polymorphic malware, spyware, or ransomware payloads;
2. Automating unauthorized reconnaissance, vulnerability exploitation, credential stuffing, or distributed denial-of-service (DDoS) operations;
3. Conducting adversarial jailbreak testing, prompt extraction, or safety boundary bypasses against Auctoric infrastructure without prior written authorization from `[security@auctoric.ai]`;
4. Attempting to reverse-engineer model weights, gradient histories, or foundational architectures.

### 2.3 Weapons, CBRN, and Physical Harm
1. Designing, manufacturing, enhancing, or weaponizing Chemical, Biological, Radiological, or Nuclear (CBRN) materials or delivery systems;
2. Generating actionable blueprints or instructions for kinetic weaponry, improvised explosive devices (IEDs), or critical infrastructure sabotage;
3. Facilitating, inciting, or coordinating acts of self-harm, suicide, or physical violence against individuals or groups.

### 2.4 Fraud, Deception, and Impersonation
1. Operating deceptive automated social bots or deepfake pipelines intended to disrupt democratic elections or civic processes;
2. Creating non-consensual deepfake pornography, synthetic non-consensual sexual content, or child sexual abuse material (CSAM);
3. Impersonating actual human individuals or legal entities without prominent disclosure, in violation of transparency obligations;
4. Orchestrating financial pyramid schemes, phishing campaigns, identity theft, or synthetic credit fraud.

### 2.5 Regulated Professional Advice & High-Stakes Decisions
1. Providing autonomous, unsupervised diagnostic medical decisions, prescription modifications, or emergency triage;
2. Generating formal legal opinions, court pleadings, or fiduciary financial determinations without qualified professional human oversight;
3. Using autonomous agentic executions for critical infrastructure control (e.g., nuclear grid, air traffic control) without fail-safe deterministic human overrides.

---

## 3. High-Risk Use System Requirements

If you utilize Auctoric to support High-Risk AI Systems as classified under the EU AI Act (Annex III) or critical systems under NIST AI RMF:

1. **Human-in-the-Loop (HITL):** You must maintain meaningful human oversight mechanisms capable of reviewing, rejecting, or overriding platform outputs.
2. **Post-Market Monitoring:** You must log system interactions and report any algorithmic anomalies or systemic bias incidents to `[compliance@auctoric.ai]`.
3. **Mandatory Documentation:** You must maintain technical documentation demonstrating compliance with risk management benchmarks as outlined in our [ISO 42001 & EU AI Act Policy](../ai-governance/iso-42001-eu-ai-act-policy.md).

---

## 4. Platform Safety Guardrails & Monitoring

To maintain compliance and platform safety:
* Auctoric operates automated, privacy-preserving safety classifiers designed to detect toxic payloads, prompt injection, and CBRN vectors in real-time.
* Classifiers operate at the network perimeter without persisting personal data into training pipelines.
* Any bypass of these runtime filters constitutes a material breach of this Policy.

---

## 5. Violations, Enforcement, and Appeals

### 5.1 Enforcement Actions
Auctoric reserves the right to investigate potential violations. Depending on the severity and frequency, Auctoric may:
* Issue formal warnings and compliance remediation notices;
* Impose temporary rate limit throttles or revoke specific API key permissions;
* Suspend or permanently terminate account access;
* Report severe violations (such as CSAM, terrorism, or critical infrastructure threats) to law enforcement or relevant competent authorities.

### 5.2 Appeals Process
If you believe your account suspension or prompt filtering resulted from an erroneous classification or false positive:
1. Submit an appeal to `[appeals@auctoric.ai]` within fourteen (14) days of notice;
2. Include account ID, transaction hash or timestamp, and technical justification;
3. The Auctoric AI Safety & Compliance Committee will review the appeal and deliver a written determination within five (5) business days.

---

## 6. Reporting Violations

If you discover or suspect a violation of this Policy, please report it immediately:
* **Email:** `[safety@auctoric.ai]` or `[trust@auctoric.ai]`
* **Online Incident Form:** `[https://auctoric.ai/safety/report-violation]`
