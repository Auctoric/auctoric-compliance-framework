# Data Processing Addendum (DPA) with Standard Contractual Clauses (SCCs)

**Document Reference:** AUC-LEG-DPA-001  
**Version:** 3.2  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal

---

This Data Processing Addendum ("**DPA**") supplements and amends the [Master Services Agreement](master-services-agreement.md) ("**Principal Agreement**") entered into by and between **[Auctoric, Inc.]** ("**Auctoric**", "Processor") and the customer entity identified in the applicable Order Form ("**Customer**", "Controller").

---

## 1. Scope, Order of Precedence, and Definitions

### 1.1 Scope
This DPA applies whenever Auctoric processes Personal Data on behalf of Customer in the provision of the Auctoric platform and AI governance services.

### 1.2 Order of Precedence
In the event of any conflict between the Principal Agreement and this DPA, the terms of this DPA shall govern. In the event of any conflict between this DPA and the Standard Contractual Clauses (SCCs), the SCCs shall prevail.

### 1.3 Definitions
* **"Applicable Privacy Laws"** means all worldwide data protection and privacy laws and regulations applicable to the personal data in question, including: (i) Regulation (EU) 2016/679 (GDPR); (ii) UK GDPR and Data Protection Act 2018; (iii) California Consumer Privacy Act as amended by the CPRA; (iv) Swiss Federal Act on Data Protection (FADP); and (v) Canadian PIPEDA.
* **"Customer Personal Data"** means any Personal Data processed by Auctoric on behalf of Customer in connection with Customer’s use of the Services.
* **"Standard Contractual Clauses"** or **"SCCs"** means the standard contractual clauses approved by European Commission Implementing Decision (EU) 2021/914 of 4 June 2021.

---

## 2. Processing Mandate and Instructions

### 2.1 Customer as Controller
Customer instructs Auctoric to process Customer Personal Data solely:
1. To provide, maintain, and support the Services in accordance with the Principal Agreement;
2. As documented in this DPA and applicable Order Forms;
3. As strictly necessary to comply with applicable legal obligations.

### 2.2 Model Training Exclusion
Auctoric shall **not** process, train, fine-tune, or calibrate any general foundational machine learning models using Customer Personal Data. All model inference operations occur in ephemeral execution enclaves without persistence, unless persistent storage or retrieval-augmented generation (RAG) vector embeddings are expressly configured by Customer.

---

## 3. Confidentiality and Personnel

Auctoric ensures that any personnel authorized to process Customer Personal Data have committed themselves to confidentiality obligations or are under an appropriate statutory obligation of confidentiality, and have undergone role-based privacy and security training.

---

## 4. Security of Processing (Article 32 GDPR)

Auctoric implements and maintains appropriate technical and organizational measures (TOMs) designed to ensure a level of security appropriate to the risk, as detailed in **Schedule B (Technical and Organizational Measures)**. These measures include:
* Pseudonymization, hashing, and AES-256 encryption of Personal Data at rest;
* TLS 1.3 encryption for all data in transit across public and internal network boundaries;
* Multi-tenant data segregation with cryptographically separated namespaces;
* Formal Business Continuity and Disaster Recovery plans with annual testing;
* Continuous automated vulnerability scanning and independent SOC 2 Type II and ISO 27001 audits.

---

## 5. Subprocessors

### 5.1 Authorization
Customer provides general written authorization for Auctoric to engage third-party Subprocessors to perform specific processing activities. An up-to-date list of Subprocessors is available at `[https://auctoric.ai/legal/subprocessors]`.

### 5.2 Notification and Objection Right
Auctoric will notify Customer at least thirty (30) calendar days prior to adding or replacing a Subprocessor via email or dashboard notification. Customer may object to a new Subprocessor on reasonable data protection grounds within fifteen (15) days of receipt of such notice. If Customer objects and the parties cannot resolve the objection, Customer may terminate the affected Services without penalty.

### 5.3 Flow-Down Obligations
Auctoric imposes data protection terms on each Subprocessor that offer at least the same level of protection for Customer Personal Data as those set out in this DPA.

---

## 6. Data Subject Rights Assistance

Auctoric will, taking into account the nature of the processing, assist Customer by appropriate technical and organizational measures to fulfill Customer's obligations to respond to requests from Data Subjects exercising their statutory rights under Applicable Privacy Laws (e.g., access, rectification, erasure, data portability).

If Auctoric receives a request directly from a Data Subject, Auctoric will notify Customer promptly and advise the Data Subject to submit their request directly to Customer.

---

## 7. Personal Data Breach Notification

### 7.1 Notification Timeline
Auctoric will notify Customer in writing without undue delay, and in any event within **forty-eight (48) hours**, after becoming aware of a confirmed Personal Data Breach impacting Customer Personal Data.

### 7.2 Content of Notification
The notification will at a minimum describe:
1. The nature of the Personal Data Breach, including categories and approximate numbers of data subjects and records;
2. The identity and contact details of the Data Protection Officer or security lead;
3. The likely consequences of the incident;
4. The remediation measures taken or proposed to mitigate possible adverse effects.

---

## 8. Audits and Compliance Verification

Auctoric shall make available to Customer all information necessary to demonstrate compliance with Article 28 GDPR. Auctoric satisfies this requirement by providing:
* Current SOC 2 Type II reports, ISO 27001 certificates, and ISO 42001 certification summaries;
* Executive summaries of annual third-party penetration tests.

If Customer reasonably requires an on-site audit, such audit will occur during regular business hours, once per calendar year, upon at least thirty (30) days’ prior written notice, without disrupting ongoing platform operations.

---

## 9. Data Deletion and Return

Upon termination of the Services, Auctoric will, at Customer’s written election, delete or return all Customer Personal Data, and securely delete existing copies in accordance with NIST SP 800-88 Rev 1 sanitization standards within sixty (60) days, unless applicable European Union or Member State law requires continued retention.

---

## 10. International Transfers & Standard Contractual Clauses (SCCs)

### 10.1 Application of European SCCs
Where the processing involves an international transfer of Customer Personal Data subject to EU GDPR to a country not recognized as providing an adequate level of data protection, the Standard Contractual Clauses (Commission Implementing Decision (EU) 2021/914) are incorporated as follows:
* **Module Two (Controller-to-Processor)** applies where Customer is a Controller and Auctoric is a Processor.
* **Module Three (Processor-to-Processor)** applies where Customer is a Processor on behalf of third-party controllers and Auctoric acts as a Sub-processor.
* **Clause 7 (Docking Clause):** Optional docking clause is incorporated.
* **Clause 9 (Use of Sub-processors):** Option 2 (General written authorization) applies with a 30-day notice period.
* **Clause 11 (Redress):** The optional language is omitted.
* **Clause 17 & 18 (Governing Law & Forum):** The laws and courts of the Republic of Ireland shall govern.

### 10.2 UK International Data Transfer Addendum
For transfers subject to UK GDPR, the UK Information Commissioner's Office (ICO) International Data Transfer Addendum to the EU Commission Standard Contractual Clauses (Version B1.0) is incorporated herein.

---

## Schedule A: Details of Processing

* **Subject Matter:** The provision of AI governance, orchestrations, and inference services under the Principal Agreement.
* **Duration:** The term of the Principal Agreement plus retention periods mandated by law or agreed data deletion timelines.
* **Nature and Purpose:** Cloud-hosted AI inference, retrieval-augmented generation (RAG) routing, automated guardrail filtering, audit telemetry, and API integration.
* **Data Subject Categories:** Customer’s employees, end-users, system administrators, business partners, or consumers whose personal details are provided in Customer prompts.
* **Categories of Personal Data:** Identifiers (names, emails, IDs), professional details, prompt contents, system logs, API credentials, and technical telemetry.
* **Special Categories of Data (Sensitive Data):** None intended unless Customer explicitly deploys the platform for HIPAA-compliant or regulated workflows under a designated Business Associate Agreement.

---

## Schedule B: Technical and Organizational Measures (TOMs)

1. **Access Control:** Centralized Single Sign-On (SSO) with Multi-Factor Authentication (MFA) via SAML 2.0 / OIDC. Least-privilege RBAC.
2. **Encryption:** AES-256 for data at rest. TLS 1.3 for data in transit with forward secrecy.
3. **Physical Security:** Cloud hosted exclusively in SOC 2 Type II, ISO 27001, and Tier III/IV compliant hyperscaler data centers.
4. **Vulnerability Management:** Weekly automated SAST/DAST/container scanning; annual third-party penetration testing; managed vulnerability disclosure program.
5. **Incident Response:** 24/7/365 Security Operations Center (SOC) monitoring and automated SIEM alerting.
6. **AI Safety Filters:** Real-time privacy-preserving PII redaction and prompt safety filters before inference dispatch.

---

**IN WITNESS WHEREOF**, the parties have executed this Data Processing Addendum.

| **For [Auctoric, Inc.]** | **For [Customer Legal Name]** |
| :--- | :--- |
| **Signature:** ___________________________ | **Signature:** ___________________________ |
| **Name:** `[Authorized Officer Name]` | **Name:** `[Authorized Officer Name]` |
| **Title:** `[Data Protection Officer / VP]` | **Title:** `[Authorized Signatory Title]` |
| **Date:** `[Insert Date]` | **Date:** `[Insert Date]` |
