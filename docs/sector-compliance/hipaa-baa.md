# HIPAA Business Associate Agreement (BAA)

**Document Reference:** AUC-SEC-BAA-001  
**Version:** 3.0  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Legal / Healthcare Sector Compliance  
**Regulatory Standards:** Health Insurance Portability and Accountability Act of 1996 (HIPAA) | Health Information Technology for Economic and Clinical Health (HITECH) Act | Omnibus Rule (45 CFR Parts 160 & 164)

---

This Business Associate Agreement ("**BAA**") is entered into by and between **[Auctoric, Inc.]** ("**Business Associate**" or "**Auctoric**") and the customer entity identified in the underlying Master Services Agreement ("**Covered Entity**" or "**Customer**").

WHEREAS, Covered Entity is subject to the requirements of HIPAA and HITECH, and wishes to utilize the Auctoric Governed AI Platform to process, store, or transmit electronic Protected Health Information ("**ePHI**");

NOW, THEREFORE, the parties agree to the following terms and conditions:

---

## 1. Definitions

* **"Breach"** shall have the same meaning as given in 45 CFR § 164.402, generally denoting the acquisition, access, use, or disclosure of Protected Health Information in a manner not permitted under Subpart E of 45 CFR Part 164 that compromises the security or privacy of the PHI.
* **"Designated Record Set"** shall have the same meaning as given in 45 CFR § 164.501.
* **"Electronic Protected Health Information" ("ePHI")** means Protected Health Information transmitted or maintained in electronic media, as defined in 45 CFR § 160.103.
* **"Individual"** shall have the same meaning as given in 45 CFR § 160.103 and includes persons who qualify as a personal representative under 45 CFR § 164.502(g).
* **"Privacy Rule"** means the Standards for Privacy of Individually Identifiable Health Information at 45 CFR Part 160 and Part 164, Subparts A and E.
* **"Security Rule"** means the Health Insurance Reform: Security Standards at 45 CFR Part 160 and Part 164, Subparts A and C.

---

## 2. Permitted Uses and Disclosures by Business Associate

### 2.1 Authorized Provisioning of Services
Except as otherwise limited in this BAA, Business Associate may use or disclose ePHI solely to perform functions, activities, or services for, or on behalf of, Covered Entity as specified in the Master Services Agreement, provided that such use or disclosure would not violate the Privacy Rule if done by Covered Entity.

### 2.2 Strict Healthcare AI Non-Training Commitment
Business Associate explicitly warrants and covenants that **ePHI will NOT be used, retained, extracted, or aggregated to train, retrain, fine-tune, or align foundational, public, or multi-tenant machine learning models**, in accordance with Auctoric’s [AI DPA & Model Non-Retention Addendum](../ai-governance/ai-dpa-model-non-retention-addendum.md).

### 2.3 Management and Administration
Business Associate may use ePHI:
1. For the proper management and administration of Business Associate;
2. To carry out the legal responsibilities of Business Associate;
3. For data de-identification in strict conformity with 45 CFR § 164.514(b) (Safe Harbor or Expert Determination), only upon Covered Entity's prior written authorization.

---

## 3. Obligations and Activities of Business Associate

### 3.1 Security Rule Safeguards
Business Associate shall implement and maintain administrative, physical, and technical safeguards that reasonably and appropriately protect the confidentiality, integrity, and availability of ePHI that it creates, receives, maintains, or transmits on behalf of Covered Entity, complying with 45 CFR §§ 164.308, 164.310, 164.312, and 164.316:
* **Encryption Standards:** Business Associate enforces AES-256 encryption at rest and TLS 1.3 encryption in transit across all ePHI processing nodes.
* **Access Control:** Phishing-resistant Multi-Factor Authentication (MFA) and least-privilege role-based access control (RBAC).

### 3.2 Reporting of Breaches and Security Incidents
1. **Breach of Unsecured PHI:** Business Associate shall notify Covered Entity in writing without unreasonable delay, and in no event later than **ten (10) business days** after discovery of a confirmed Breach of Unsecured PHI.
2. **Security Incident Reporting:** Business Associate shall report to Covered Entity any successful unauthorized access, use, disclosure, modification, or destruction of ePHI. The parties acknowledge that unsuccessful attempts (e.g., automated port scans, unsuccessful pings, blocked firewall probes) occur continuously and that this Section constitutes notice without obligation to report such routine unsuccessful attempts.

### 3.3 Subcontractors & Subprocessors
In accordance with 45 CFR §§ 164.502(e)(1)(ii) and 164.308(b)(2), Business Associate shall ensure that any subcontractor or agent that creates, receives, maintains, or transmits ePHI on behalf of Business Associate agrees to the same restrictions, conditions, and requirements that apply to Business Associate with respect to such information.

### 3.4 Access to Books and Records
Business Associate shall make its internal practices, books, and records relating to the use and disclosure of ePHI available to the Secretary of Health and Human Services (HHS) for purposes of determining Covered Entity's or Business Associate's compliance with HIPAA.

---

## 4. Minimum Necessary Standard

Business Associate shall limit its requests, uses, and disclosures of ePHI to the minimum necessary to accomplish the intended purpose of the request, use, or disclosure, in accordance with 45 CFR § 164.502(b).

---

## 5. Term and Termination

### 5.1 Term
The term of this BAA shall be effective as of the Effective Date and shall terminate when all of the ePHI provided by Covered Entity to Business Associate is destroyed or returned to Covered Entity.

### 5.2 Termination for Cause
Upon Covered Entity’s knowledge of a material breach of this BAA by Business Associate, Covered Entity shall either:
1. Provide thirty (30) days' written notice and opportunity for Business Associate to cure the breach; or
2. Immediately terminate this BAA and the underlying Master Services Agreement if Business Associate fails to cure or if a cure is not feasible.

### 5.3 Effect of Termination & NIST Media Sanitization
Upon termination, Business Associate shall:
1. Return or destroy all ePHI received from Covered Entity that Business Associate still maintains in any form;
2. Securely overwrite storage media containing ePHI in accordance with NIST SP 800-88 Rev. 1;
3. If return or destruction is infeasible, extend the protections of this BAA to such ePHI and limit further uses and disclosures to those purposes that make the return or destruction infeasible.

---

## 6. Miscellaneous

### 6.1 Regulatory References
A reference in this BAA to a section in the HIPAA Rules means the section as in effect or as amended.

### 6.2 Precedence
In the event of a conflict between the terms of this BAA and the Master Services Agreement, the terms of this BAA shall govern with respect to HIPAA and ePHI compliance.

---

**IN WITNESS WHEREOF**, the parties have caused this Business Associate Agreement to be executed by their duly authorized representatives.

| **For [Auctoric, Inc.]** | **For [Covered Entity Legal Name]** |
| :--- | :--- |
| **Signature:** ___________________________ | **Signature:** ___________________________ |
| **Name:** `[Authorized Officer Name]` | **Name:** `[Authorized Officer Name]` |
| **Title:** `[CISO / Privacy Officer]` | **Title:** `[HIPAA Privacy Officer / Executive]` |
| **Date:** `[Insert Date]` | **Date:** `[Insert Date]` |
