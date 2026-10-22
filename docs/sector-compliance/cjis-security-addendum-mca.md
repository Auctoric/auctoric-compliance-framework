# CJIS Security Addendum & Management Control Agreement (MCA)

**Document Reference:** AUC-SEC-CJIS-001  
**Version:** 2.1  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Legal / Law Enforcement Sector Compliance  
**Regulatory Standards:** FBI Criminal Justice Information Services (CJIS) Security Policy (v5.9 / v5.10) | 28 CFR Part 20 | CJIS Security Addendum (Form CJIS-001c)

---

## Part I: CJIS Management Control Agreement (MCA)

This Management Control Agreement ("**MCA**") is entered into by and between the Contracting Law Enforcement / Criminal Justice Agency ("**CJA**") and **[Auctoric, Inc.]** ("**Contractor**" or "**Auctoric**").

### 1. Purpose and Authority
Pursuant to Title 28, Code of Federal Regulations (CFR), Part 20, and the FBI CJIS Security Policy, a Criminal Justice Agency may contract with a private contractor to administer, process, store, or support systems containing Criminal Justice Information ("**CJI**").

This Agreement establishes that the CJA maintains full management control over the criminal justice aspects of Auctoric platform operations housing or processing CJA data.

### 2. Grant of Management Control
Auctoric agrees that the CJA retains the ultimate authority to:
1. Set policies regarding the access, dissemination, and handling of CJI;
2. Approve or revoke access permissions for any Auctoric personnel or automated agent systems interacting with CJI;
3. Direct the immediate termination of services or severance of network interconnections in the event of an unmitigated security violation;
4. Initiate and conduct audits of Auctoric facilities, cloud configurations, and audit logs.

---

## Part II: CJIS Security Addendum (Uniform Contract Clause)

The following provisions incorporate the mandatory text and requirements of the **FBI CJIS Security Addendum (Standard Form CJIS-001c)**:

### 1. Contractor Personnel Background Screening & Training
* **Fingerprint-Based Background Check:** Prior to being granted unescorted logical or physical access to systems containing unencrypted CJI, all Auctoric personnel must undergo a state and national fingerprint-based background check through the appropriate State CJIS Systems Agency (CSA).
* **Felony Disqualification:** Any individual with a felony conviction is strictly barred from access to CJI.
* **Security Awareness Training:** Auctoric personnel with administrative access to CJIS-designated infrastructure must complete biennial Level 4 CJIS Security Awareness Training within thirty (30) days of assignment.

### 2. Physical & Logical Protection of CJI
* **U.S. Sovereign Data Boundary:** All CJI processed or stored within Auctoric systems resides exclusively within FedRAMP High / CJIS-attested hyperscaler data centers physically located within the contiguous United States (CONUS) (e.g., AWS GovCloud / Azure Government).
* **Logical Segregation:** Virtual machines, container namespaces, and vector databases containing CJI are logically and cryptographically partitioned from commercial multi-tenant infrastructure.
* **U.S. Persons Restriction:** Unencrypted CJI may only be accessed by vetted "U.S. Persons" (as defined under 8 U.S.C. § 1101(a)(20) and 8 U.S.C. § 1324b(a)(3)) who have satisfied the background screening requirements.

### 3. Encryption Standards (CJIS Area 5.10)
* **Data in Transit:** All network traffic conveying CJI across public or shared networks is encrypted using FIPS 140-3 validated cryptographic modules with a minimum of TLS 1.3 or IPsec (AES-256).
* **Data at Rest:** All disk volumes, database records, and vector embeddings containing CJI are encrypted at rest using FIPS 140-3 validated AES-256 encryption.

### 4. CJI Handling in Artificial Intelligence & Large Language Models
* **Prohibition on Model Training:** CJI shall **NEVER** be ingested into public or multi-tenant foundational AI models for training, calibration, or evaluation.
* **Ephemeral Inference:** Prompt inputs and model completions containing CJI are processed in volatile memory and purged immediately post-inference, unless the CJA specifies encrypted retention in an authorized CJIS-compliant evidence repository.
* **Audit Trail (CJIS Area 5.4):** Every prompt, inference transaction, automated agent tool call, and administrative access event touching CJI is recorded with immutable timestamps, user IDs, IP addresses, and event classifications, retained for a minimum of one (1) year.

### 5. Security Incident Reporting & Audit Rights
* **Incident Escalation:** Auctoric will notify the CJA Information Security Officer (ISO) and the FBI/State CSA within **four (4) hours** of confirming any unauthorized access, breach, or compromise involving CJI.
* **Audit Co-operation:** Auctoric agrees to permit triennial CJIS audits conducted by the State CSA and the FBI CJIS Audit Unit (CAU).

---

## Part III: Execution & Signatures

IN WITNESS WHEREOF, the parties hereto have executed this CJIS Management Control Agreement and Security Addendum.

| **For Criminal Justice Agency (CJA)** | **For [Auctoric, Inc.] (Contractor)** |
| :--- | :--- |
| **Agency Name:** `[Name of Law Enforcement Agency]` | **Company Name:** `[Auctoric, Inc.]` |
| **Signature:** ___________________________ | **Signature:** ___________________________ |
| **Name:** `[Authorized Agency Official]` | **Name:** `[Authorized Officer Name]` |
| **Title:** `[Chief of Police / Sheriff / Director]` | **Title:** `[CISO / General Counsel]` |
| **Date:** `[Insert Date]` | **Date:** `[Insert Date]` |

### Contractor Employee Acknowledgment (Individual Sign-Off Template)
*I hereby certify that I have reviewed the FBI CJIS Security Policy and understand my legal obligation to preserve the confidentiality and integrity of all Criminal Justice Information.*

* **Employee Name:** `[Employee Legal Name]`
* **Title / Role:** `[DevOps / Infrastructure Engineer]`
* **Signature:** ___________________________
* **Date:** `[Insert Date]`
