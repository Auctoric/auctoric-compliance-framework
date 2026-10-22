# Data Processing Addendum (DPA) with Standard Contractual Clauses (SCCs)

**Document Reference:** AUC-LEG-DPA-001  
**Version:** 3.3  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal  
**Regulatory Baselines:** Regulation (EU) 2016/679 (GDPR) | UK GDPR | California Consumer Privacy Act as amended (CPRA) | Swiss FADP

---

This Data Processing Addendum ("**DPA**") supplements and amends the [Master Services Agreement](master-services-agreement.md) ("**Principal Agreement**") entered into by and between **Auctoric, LLC** ("**Auctoric**", "Processor") and the customer entity identified in the applicable Order Form ("**Customer**", "Controller" or "Processor" on behalf of third parties).

---

## 1. Scope, Order of Precedence, and Definitions

### 1.1 Scope
This DPA applies whenever Auctoric processes Personal Data on behalf of Customer in the provision of the Auctoric platform and AI governance services.

### 1.2 Order of Precedence
In the event of any conflict or inconsistency between the Principal Agreement and this DPA, the terms of this DPA shall govern with respect to the processing of Personal Data. In the event of any conflict between this DPA and the Standard Contractual Clauses (SCCs), the SCCs shall prevail.

### 1.3 Definitions
* **"Applicable Privacy Laws"** means all worldwide data protection and privacy laws and regulations applicable to the personal data in question, including: (i) Regulation (EU) 2016/679 (GDPR); (ii) UK GDPR and Data Protection Act 2018; (iii) California Consumer Privacy Act as amended by the CPRA; (iv) Swiss Federal Act on Data Protection (FADP); and (v) Canadian PIPEDA.
* **"Customer Personal Data"** means any Personal Data processed by Auctoric on behalf of Customer in connection with Customer’s use of the Services.
* **"Standard Contractual Clauses"** or **"SCCs"** means the standard contractual clauses approved by European Commission Implementing Decision (EU) 2021/914 of 4 June 2021.

---

## 2. Processing Mandate and Instructions

### 2.1 Customer Instructions
Customer instructs Auctoric to process Customer Personal Data solely:
1. To provide, maintain, and support the Services in accordance with the Principal Agreement;
2. As documented in this DPA and applicable Order Forms;
3. As strictly necessary to comply with applicable legal obligations. Auctoric shall promptly inform Customer if, in its opinion, an instruction infringes Applicable Privacy Laws.

### 2.2 Model Training Exclusion
Auctoric shall **not** process, train, fine-tune, or calibrate any general foundational machine learning models using Customer Personal Data. All model inference operations occur in ephemeral execution enclaves without persistent storage of prompts or outputs, unless persistent storage or retrieval-augmented generation (RAG) vector embeddings are expressly configured by Customer.

---

## 3. Confidentiality and Personnel

Auctoric ensures that any personnel authorized to process Customer Personal Data have committed themselves to confidentiality obligations or are under an appropriate statutory obligation of confidentiality, and have undergone role-based privacy and security training.

---

## 4. Security of Processing (Article 32 GDPR)

Auctoric implements and maintains appropriate technical and organizational measures (TOMs) designed to ensure a level of security appropriate to the risk, as detailed in **Schedule B (Technical and Organizational Measures)**. These measures include:
* Pseudonymization, hashing, and AES-256 encryption of Personal Data at rest;
* TLS 1.3 encryption for all data in transit across public and internal network boundaries;
* Multi-tenant data segregation with cryptographically separated namespaces;
* Formal Business Continuity and Disaster Recovery plans with recurring testing;
* Continuous automated vulnerability scanning and control assessments aligned with ISO/IEC 27001 and SOC 2 criteria.

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
Auctoric will notify Customer in writing without undue delay, and in any event within **forty-eight (48) hours**, after becoming aware of a Personal Data Breach impacting Customer Personal Data. Initial notification may contain preliminary details then available and will not be delayed awaiting completion of the full forensic investigation.

### 7.2 Content of Notification
The notification will at a minimum describe:
1. The nature of the Personal Data Breach, including categories and approximate numbers of data subjects and records;
2. The identity and contact details of the Data Protection Officer or security lead;
3. The likely consequences of the incident;
4. The remediation measures taken or proposed to mitigate possible adverse effects. Supplementary information will be provided on a rolling basis as verified.

---

## 8. Audits and Compliance Verification

Auctoric shall make available to Customer all information necessary to demonstrate compliance with Article 28 GDPR. Auctoric satisfies this requirement by providing:
* Current security documentation, system summaries, and independent control assessment reports demonstrating compliance with ISO/IEC 27001, ISO/IEC 42001, and SOC 2 Type II criteria;
* Executive summaries of annual independent penetration tests.

If Customer reasonably requires an on-site audit, such audit will occur during regular business hours, once per calendar year, upon at least thirty (30) days’ prior written notice, without disrupting ongoing platform operations. This annual restriction and advance notice requirement shall not apply to audits mandated by a competent supervisory authority or initiated following a verified material Personal Data Breach.

---

## 9. Data Deletion and Return

Upon termination of the Services, Auctoric will, at Customer’s written election within thirty (30) days of termination, make Customer Personal Data available for export, and subsequently permanently deprovision and sanitize all Customer Personal Data within thirty (30) calendar days (total maximum 60 days from termination), in accordance with NIST SP 800-88 Revision 2 media sanitization standards, unless applicable European Union or Member State law requires continued retention.

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

### 10.2 UK International Data Transfer Mechanisms
For transfers subject to UK GDPR, the UK Information Commissioner's Office (ICO) International Data Transfer Addendum to the EU Commission Standard Contractual Clauses (Version B1.0) is incorporated herein.

---

## 11. California Consumer Privacy Act (CCPA/CPRA) Statutory Terms

To the extent Auctoric processes Personal Information subject to the CCPA/CPRA as a Service Provider or Contractor:
1. **No Sale or Sharing:** Auctoric shall not "sell" or "share" Customer Personal Information (as those terms are defined under Cal. Civ. Code § 1798.140).
2. **Business Purpose Limitations:** Auctoric shall not retain, use, or disclose Customer Personal Information for any purpose other than the business purposes specified in the Principal Agreement and this DPA, including retaining Personal Information for cross-context behavioral advertising.
3. **No Cross-Tenant Combination:** Auctoric shall not combine Customer Personal Information with personal information received from, or on behalf of, other persons or sources, except as expressly permitted under Cal. Code Regs. tit. 11, § 7050.
4. **Compliance Certification:** Auctoric certifies that it understands the restrictions set forth in this Section 11 and Cal. Civ. Code § 1798.140(ag) and agrees to comply with them.
5. **Monitoring & Notice of Non-Compliance:** Auctoric grants Customer the right to take reasonable and appropriate steps to ensure Auctoric uses Personal Information consistent with CCPA obligations. Auctoric will notify Customer promptly if it determines it can no longer meet its CCPA obligations.

---

## Schedule A: Details of Processing

* **Subject Matter:** The provision of AI governance, orchestrations, and inference services under the Principal Agreement.
* **Duration:** The term of the Principal Agreement plus agreed post-termination deletion windows.
* **Nature and Purpose:** Cloud-hosted AI inference, retrieval-augmented generation (RAG) routing, automated guardrail filtering, audit telemetry, and API integration.
* **Data Subject Categories:** Customer’s employees, end-users, system administrators, business partners, or consumers whose details are submitted in Customer prompts.
* **Categories of Personal Data:** Identifiers (names, emails, IDs), professional details, prompt contents, system logs, API credentials, and technical telemetry.
* **Special Categories of Data (Sensitive Data):** None intended unless Customer explicitly deploys the platform for HIPAA-compliant workflows under an executed Business Associate Agreement.

---

## Schedule B: Technical and Organizational Measures (TOMs)

1. **Access Control:** Centralized Single Sign-On (SSO) with Multi-Factor Authentication (MFA) via SAML 2.0 / OIDC. Least-privilege RBAC.
2. **Encryption:** AES-256 for data at rest. TLS 1.3 for data in transit with forward secrecy.
3. **Infrastructure Controls:** Cloud hosted exclusively in compliant Tier III/IV hyperscaler data centers (Google Cloud Platform).
4. **Vulnerability Management:** Continuous automated SAST/DAST/container scanning; annual independent penetration testing; managed vulnerability disclosure program.
5. **Incident Response:** 24/7 SIEM monitoring with automated alerting and documented escalation procedures.
6. **AI Safety Filters:** Real-time privacy-preserving PII redaction and prompt safety filters before inference dispatch.

---

**IN WITNESS WHEREOF**, the parties have executed this Data Processing Addendum.

| **For Auctoric, LLC** | **For [Customer Legal Name]** |
| :--- | :--- |
| **Signature:** ___________________________ | **Signature:** ___________________________ |
| **Name:** `[Authorized Officer Name]` | **Name:** `[Authorized Officer Name]` |
| **Title:** `[Data Protection Officer / VP]` | **Title:** `[Authorized Signatory Title]` |
| **Date:** `[Insert Date]` | **Date:** `[Insert Date]` |
