# CJIS Security Addendum & Contractor Compliance Agreement

**Document Reference:** AUC-SEC-CJIS-001  
**Version:** 3.0  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Legal / Law Enforcement Sector Compliance  
**Regulatory Baselines:** FBI Criminal Justice Information Services (CJIS) Security Policy Version 6.1 (June 25, 2026) | Title 28 CFR Part 20 | FBI CJIS Security Addendum (Standard Form CJIS-001c)

---

> [!IMPORTANT]
> **Workload Activation Notice:** Processing or storing Criminal Justice Information (CJI) on the Auctoric platform is strictly subject to prior agency execution of this Addendum, completion of State CJIS Systems Agency (CSA) fingerprint-based background vetting, and formal activation of an approved sovereign cloud boundary (e.g., Google Cloud Assured Workloads for CJIS). Workloads involving CJI are not permitted on commercial multi-tenant endpoints.

---

## 1. Scope, Purpose, and Governing Standards

This CJIS Security Addendum & Contractor Compliance Agreement ("**Agreement**") is entered into by and between the Contracting Law Enforcement Agency or Criminal Justice Agency ("**CJA**") and **Auctoric, LLC** ("**Contractor**" or "**Auctoric**").

This Agreement incorporates the mandatory provisions of the **FBI CJIS Security Addendum (Standard Form CJIS-001c)** and establishes the technical and administrative safeguards required under **FBI CJIS Security Policy Version 6.1** for private contractors administering, processing, or supporting systems conveying Criminal Justice Information ("**CJI**").

---

## 2. Incorporating the Uniform FBI CJIS Security Addendum (Form CJIS-001c)

### 2.1 Contractor Personnel Background Screening & Training
* **Fingerprint-Based Record Check:** Prior to being granted unescorted logical or physical access to infrastructure handling unencrypted CJI, all Auctoric personnel must undergo a state and national fingerprint-based background check through the appropriate State CSA.
* **Felony Disqualification:** Any individual with a felony conviction is strictly barred from access to systems conveying CJI.
* **Security Awareness Training:** Auctoric personnel with administrative access to CJIS-designated infrastructure must complete biennial CJIS Security Awareness Training within thirty (30) days of assignment.

### 2.2 Sovereign Data Boundary & Physical/Logical Protection
* **Dedicated Cloud Enclaves:** All CJI processed or stored within Auctoric systems resides exclusively within dedicated government sovereign cloud boundaries (e.g., Google Cloud Assured Workloads for CJIS).
* **Logical Segregation:** Virtual machines, container namespaces, and vector databases containing CJI are logically and cryptographically partitioned from commercial multi-tenant infrastructure.
* **Personnel Geographic Restrictions:** Access to unencrypted CJI is restricted to screened personnel in accordance with CJIS Security Policy v6.1 Area 5.10 (Advisory Policy Board country standards, including the United States and Canada).

### 2.3 Cryptographic Standards (CJIS Area 5.10)
* **Data in Transit:** All network traffic conveying CJI across public or shared networks is encrypted using cryptographic modules conforming to FIPS standards with a minimum of TLS 1.3 or IPsec (AES-256).
* **Data at Rest:** All disk volumes, database records, and vector embeddings containing CJI are encrypted at rest using AES-256 with customer-controlled or dedicated KMS keys.

### 2.4 Handling CJI in Artificial Intelligence & Large Language Models
* **Absolute Prohibition on Public Model Training:** CJI shall **NEVER** be ingested into public, shared, or multi-tenant foundational AI models for training, calibration, or evaluation.
* **Ephemeral Processing:** Prompt inputs and model completions containing CJI are processed in volatile memory enclaves and purged immediately post-inference, unless the CJA explicitly configures encrypted retention in an authorized CJIS-compliant repository.
* **Immutable Audit Trail (CJIS Area 5.4):** Every transaction, inference call, automated agent tool execution, and administrative access event touching CJI is recorded with tamper-resistant audit logs retained for a minimum of one (1) year.

### 2.5 Security Incident Discovery and Reporting
* **Escalation Protocol:** Auctoric will notify the CJA Information Security Officer (ISO) and the designated State CSA contact within **four (4) hours** of discovering an unauthorized access event, data breach, or security incident involving CJI.
* **Audit Co-operation:** Auctoric agrees to permit triennial CJIS compliance audits conducted by the State CSA and the FBI CJIS Audit Unit (CAU).

---

## 3. Execution & Agency Signatures

IN WITNESS WHEREOF, the parties hereto have executed this CJIS Security Addendum.

| **For Criminal Justice Agency (CJA)** | **For Auctoric, LLC (Contractor)** |
| :--- | :--- |
| **Agency Name:** `[Name of Law Enforcement Agency]` | **Company Name:** `Auctoric, LLC` |
| **Signature:** ___________________________ | **Signature:** ___________________________ |
| **Name:** `[Authorized Agency Official]` | **Name:** `[Authorized Officer Name]` |
| **Title:** `[Chief of Police / Sheriff / Director]` | **Title:** `[CISO / General Counsel]` |
| **Date:** `[Insert Date]` | **Date:** `[Insert Date]` |

---

## 4. Contractor Employee Acknowledgment (Standard Form CJIS-001c Attachment)

*I hereby certify that I have reviewed the FBI CJIS Security Policy and understand my legal obligation to preserve the confidentiality, integrity, and security of all Criminal Justice Information.*

* **Employee Name:** `[Employee Legal Name]`
* **Title / Role:** `[DevOps / Infrastructure Engineer]`
* **Signature:** ___________________________
* **Date:** `[Insert Date]`
