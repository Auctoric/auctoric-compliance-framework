# Global Privacy Policy

**Document Reference:** AUC-LEG-PRIV-001  
**Version:** 3.0  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal

---

## 1. Introduction & Scope

**[Auctoric, Inc.]** ("**Auctoric**", "we", "us", or "our") provides an enterprise-grade Governed AI-as-a-System platform. We are committed to upholding the highest standards of data protection, transparency, and individual privacy rights.

This Global Privacy Policy ("**Policy**") explains how we collect, use, disclose, and protect personal data across our websites, cloud platform, developer consoles, APIs, and client-facing AI governance solutions. It applies to:
* Visitors to our websites (`[https://auctoric.com]`);
* Registered users, administrators, and developers utilizing our platform;
* Individuals whose contact information is collected through sales and marketing initiatives.

> [!NOTE]
> When our enterprise customers process personal data within their own prompts, datasets, or inputs through the Auctoric platform, **Customer is the Data Controller** and **Auctoric is the Data Processor** (or Service Provider). In those scenarios, data processing is governed by our [Data Processing Addendum (DPA)](data-processing-addendum.md) and [AI DPA & Model Non-Retention Addendum](../ai-governance/ai-dpa-model-non-retention-addendum.md).

---

## 2. Categories of Personal Data We Collect

| Category | Description | Legal Basis (GDPR / UK GDPR) |
| :--- | :--- | :--- |
| **Account & Identity Data** | Full name, business email, corporate organization, username, hashed passwords, job title. | Contract Performance (Art. 6(1)(b)) |
| **Billing & Financial Data** | Billing address, tax ID, payment method details (processed via PCI-DSS Level 1 payment processor). | Legal Obligation & Contract (Art. 6(1)(b), (c)) |
| **Telemetry & System Logs** | IP address, browser user-agent, API request timestamps, latency, error codes, endpoint routes. | Legitimate Interest (Art. 6(1)(f)) |
| **Customer Content (Inputs/Outputs)** | Structured or unstructured text, prompts, queries, and generated responses submitted via platform APIs. | Contract Performance / Processor Mandate |
| **Support & Communications** | Support tickets, diagnostic traces, feedback submissions, and webinar registrations. | Legitimate Interest / Consent (Art. 6(1)(a), (f)) |

---

## 3. How We Use Personal Data

We use personal data strictly for legitimate operational purposes, including:
1. Providing, hosting, securing, and maintaining the Auctoric Platform;
2. Authenticating user identity, enforcing role-based access control (RBAC), and detecting unauthorized access;
3. Metering API usage, calculating billable tokens, and processing subscription invoices;
4. Enforcing our Acceptable Use Policy and mitigating cybersecurity threats (e.g., prompt injection, DDoS);
5. Complying with regulatory obligations under GDPR, CCPA, HIPAA, CJIS, and the EU AI Act.

> [!IMPORTANT]
> **Zero Customer Data Retention for Base Model Training:** Auctoric does NOT sell personal data, nor do we use Customer Content (prompts, inputs, vector embeddings, outputs) to train or improve public foundational models.

---

## 4. Subprocessors and Data Disclosures

Auctoric shares personal data only with trusted third-party service providers ("Subprocessors") who are contractually bound by rigorous confidentiality and data protection obligations:
* **Cloud Infrastructure Providers:** Hyperscalers hosting compute, container orchestration, and isolated VPC storage (e.g., AWS, GCP, Azure);
* **Payment Gateways:** PCI-DSS Level 1 certified processors (e.g., Stripe);
* **Security & Monitoring Providers:** Managed threat detection, telemetry aggregation, and WAF providers.

An updated list of authorized Subprocessors is published at `[https://auctoric.com/legal/subprocessors]`.

---

## 5. International Data Transfers

When transferring personal data from the European Economic Area (EEA), the United Kingdom, or Switzerland to countries without an adequacy decision, Auctoric executes:
* Standard Contractual Clauses (SCCs) approved by the European Commission (Implementing Decision (EU) 2021/914);
* The UK International Data Transfer Addendum (IDTA);
* Supplementary technical measures including AES-256 encryption in transit (TLS 1.3) and at rest, zero-knowledge architectural silos, and strict cryptographic access management.

---

## 6. Retention of Personal Data

We retain personal data only as long as necessary to fulfill the purposes for which it was collected:
* **Account Records:** Kept for the duration of the active subscription plus required financial retention periods (typically 7 years for tax/accounting).
* **System Logs & Audit Traces:** Retained for 365 days for SOC 2 and security forensics compliance, then automatically purged.
* **Customer Inference Ephemeral Cache:** Real-time inference data in RAM is discarded immediately post-response generation, unless Customer explicitly configures asynchronous logging or custom retention buckets.

---

## 7. Individual Data Subject Rights

Depending on your jurisdiction (e.g., GDPR, CCPA/CPRA, LGPD), you possess specific legal rights regarding your personal data:

1. **Right of Access & Portability:** Request a copy of your personal data in a structured, machine-readable format.
2. **Right to Rectification:** Correct inaccurate or incomplete information.
3. **Right to Erasure ("Right to be Forgotten"):** Request deletion of personal data where statutory retention grounds no longer apply.
4. **Right to Restrict or Object to Processing:** Object to processing based on legitimate interests or direct marketing.
5. **Rights Regarding Automated Decision-Making & Profiling:** Understand the logic involved in automated systems and request human intervention. See our [Automated Decision-Making Notice](../ai-governance/automated-decision-making-notice.md).
6. **Right to Opt-Out of Sale / Sharing (California CPRA):** Auctoric does not sell or share personal information for cross-context behavioral advertising.

To exercise these rights, email `[privacy@auctoric.com]` or submit a request via our Data Privacy Portal at `[https://auctoric.com/privacy/requests]`.

---

## 8. Security Measures

Auctoric implements technical and organizational safeguards certified against ISO 27001, ISO 42001, and SOC 2 Type II controls:
* Mutual TLS 1.3 encryption across all internal microservice communication and external endpoints;
* Hardware Security Module (HSM) key management with envelope encryption;
* Role-based access control (RBAC), multi-factor authentication (MFA), and least-privilege administrative access;
* Continuous automated vulnerability scanning and third-party red teaming.

---

## 9. Contact and Data Protection Officer (DPO)

For inquiries, concerns, or formal privacy complaints, please contact our Data Protection Officer:

* **Data Protection Officer:** `[Name of DPO / Privacy Officer]`
* **Email:** `[dpo@auctoric.com]` or `[privacy@auctoric.com]`
* **Physical Address:** `[Auctoric, Inc., Attn: Privacy Office, 100 Enterprise Way, Suite 400, San Francisco, CA 94105]`
* **EU Representative (GDPR Art. 27):** `[Auctoric EU Compliance Ltd, Dublin, Ireland - eu-rep@auctoric.com]`
* **UK Representative (UK GDPR):** `[Auctoric UK Ltd, London, United Kingdom - uk-rep@auctoric.com]`
