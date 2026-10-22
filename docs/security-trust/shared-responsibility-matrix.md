# Shared Responsibility Matrix

**Document Reference:** AUC-SEC-SRM-001  
**Version:** 3.0  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Customer Guidance  
**Standards Frameworks:** SOC 2 | ISO/IEC 27001 | ISO/IEC 42001 | NIST AI RMF | FedRAMP / CMMC  
**Companion Documents:** [Master Services Agreement](../legal/master-services-agreement.md) | [Schedule 1: AI Service-Specific Terms](../legal/ai-service-specific-terms.md) | [Customer Copyright & IP Protection Addendum](../legal/customer-copyright-ip-protection-addendum.md)

---

## 1. Overview and Architecture Principles

Security, intellectual property protection, and regulatory compliance within the **Auctoric Governed AI Platform** operate under a **Tripartite Shared Responsibility Model**. Ensuring end-to-end security, data protection, and statutory alignment is a collaborative obligation shared among:

1. **Cloud Service & Foundation Model Providers (CSP):** Underlying hyperscaler infrastructure (**Google Cloud / Vertex AI**, **Microsoft Azure**, **Anthropic**, **AWS**) providing physical facilities, specialized GPU hardware (TPUs/H100s), foundational pre-training datasets, and base model weights.
2. **Auctoric (AI Platform & Governance Provider):** Multi-model routing gateway, real-time safety guardrails, PII/PCI redaction, Customer Copyright Commitment defense, agentic orchestration, tenant vector isolation, and WORM audit logging.
3. **Customer (Deployer & Enterprise Tenant):** User identity provisioning, prompt crafting, application data classification, client secrets management, human oversight (HITL), and downstream regulatory compliance.

```mermaid
flowchart TD
    subgraph CSP["1. Upstream Providers (Google Cloud / Azure / Anthropic)"]
        Phys["Physical Data Center Facilities & Server Hardware"]
        Virt["Hypervisor, Virtualization & GPU Accelerators"]
        BaseModels["Base Foundational Model Weights & Pre-Training Lineage"]
    end

    subgraph Auctoric["2. Auctoric Platform (Governed AI-as-a-System)"]
        Kubernetes["Container Orchestration, EKS/GKE Hardening"]
        Router["Multi-Model Gateway & Intelligent Dispatch Engine"]
        Guardrails["Runtime Guardrails, PII Masking & Safety Classifiers"]
        CCC["Customer Copyright Commitment (CCC) Output Defense"]
        AuditLog["Immutable WORM Audit Logging & Evidence Pipelines"]
    end

    subgraph Customer["3. Customer (Deployer & Tenant)"]
        IAM["User Account Creation, IdP Integration (SAML/SSO) & MFA"]
        DataGov["Data Classification, Sensitive Data Identification & Input Sanitation"]
        SafetyGov["Guardrail Activation, System Prompt Design & HITL Workflows"]
        AntiDistill["Adherence to Anti-Distillation & Prohibited Use Covenants"]
        Downstream["Downstream Regulatory Compliance (EU AI Act, HIPAA, CJIS)"]
    end

    CSP --- Auctoric --- Customer
```

---

## 2. Comprehensive Shared Responsibility Matrix

| Domain / Control Area | Cloud / Model Provider | Auctoric Platform | Customer (Tenant) | Responsibility Summary & Operational Guidance |
| :--- | :---: | :---: | :---: | :--- |
| **Physical & Environmental** | **Sole** | Inherited | Inherited | CSP provides biometric data center access, UPS power, HVAC, and physical camera monitoring. |
| **Hypervisor & GPU Isolation** | **Sole** | Inherited | Inherited | CSP guarantees multi-tenant hypervisor and GPU memory slice isolation. |
| **Network Perimeter (DDoS / Edge)** | Shared | **Primary** | Customer Config | CSP provides L3/L4 DDoS mitigation; Auctoric configures WAF, TLS 1.3 termination, and rate limits; Customer configures custom IP allowlists if required. |
| **Platform Microservices & OS** | Inherited | **Sole** | N/A | Auctoric hardens container images (distroless), applies weekly OS patches, and enforces zero-root execution. |
| **AI Foundation Model Weights** | **Sole** (Upstream) | Shared | N/A | Upstream provider secures foundational weights; Auctoric verifies model artifact checksums and protects custom fine-tuned LoRA matrices. |
| **AI Safety Guardrails & Filtering** | Inherited | **Primary** | **Shared** | Auctoric provides real-time PII redaction and prompt toxicity classifiers; Customer must keep filters active and configure domain-specific blocklists. |
| **Prompt Injection Defense** | Inherited | **Shared** | **Shared** | Auctoric deploys multi-stage heuristic & neural prompt injection filters; Customer must sanitize input parameters and prevent direct concatenated user prompts in system roles. |
| **Tenant Data Isolation & RAG** | Inherited | **Primary** | Shared | Auctoric provides cryptographically partitioned vector indexes; Customer manages index access permissions and document ingestion scope. |
| **Output Copyright Indemnity (CCC)** | Upstream Indemnity | **Primary Defense** | **Condition Precedent** | Upstream provider indemnifies base weights; Auctoric defends outputs under CCC; Customer must keep guardrails active and avoid intentional infringing prompts. |
| **Anti-Model Distillation Enforcement** | **Enforcing Entity** | **Enforcing Entity** | **Contractual Duty** | Upstream terms prohibit competing distillation; Auctoric forbids synthetic dataset training; Customer covenants not to train competing foundation models. |
| **Clinical / Healthcare Triage** | Disclaimed | Disclaimed | **Sole Responsibility** | Neither Google nor Auctoric provides medical devices; Customer must maintain a qualified licensed clinician as the ultimate human decision-maker. |
| **Critical Infrastructure Control** | Disclaimed | Disclaimed | **Sole Responsibility** | Systems are not fault-tolerant for hazardous environments; Customer must implement air-gapped deterministic emergency stop overrides. |
| **Data Encryption at Rest** | Shared | **Primary** | Shared | CSP provides KMS hardware; Auctoric enforces AES-256 by default; Customer may supply Customer-Managed Encryption Keys (CMEK). |
| **Data Encryption in Transit** | Shared | **Sole** | Customer Config | Auctoric enforces TLS 1.3 across all endpoints; Customer must ensure their client SDKs and API libraries do not disable TLS verification. |
| **Identity & Access Management (IAM)**| Inherited | Shared | **Primary** | Auctoric provides SSO/SAML integrations and RBAC tools; Customer must enforce corporate MFA, manage user provisioning, and deprovision departed staff. |
| **API Secret & Token Management** | Inherited | Shared | **Primary** | Auctoric securely hashes and stores credentials; Customer must never hardcode API keys in frontend code, git repositories, or client bundles. |
| **Human-in-the-Loop (HITL) Controls** | Inherited | Shared | **Primary** | Auctoric provides audit logs and HITL intervention APIs; Customer must staff and execute human review for High-Risk automated decisions. |
| **End-User Consent & Privacy Rights** | Inherited | Shared | **Sole** | Customer is the Data Controller responsible for collecting valid consent and responding to consumer data subject requests (DSARs). |
| **Backup & Business Continuity** | Shared | **Primary** | Shared | Auctoric maintains multi-region backup pipelines (RPO < 1h, RTO < 4h); Customer is responsible for maintaining local copies of raw source documents. |

---

## 3. Detailed AI & Large Language Model (LLM) Risk Responsibilities

The OWASP Top 10 for Large Language Applications requires specific shared actions:

### 3.1 LLM01: Prompt Injection & Adversarial Jailbreaking
* **Auctoric Responsibility:** Implement real-time multi-stage injection classifiers, inspect semantic embedding anomalies, and isolate system prompts from user prompt execution blocks.
* **Customer Responsibility:** Implement input length validation, escape untrusted variables, and architect workflows using least-privilege agent tools (e.g., read-only database connections).

### 3.2 LLM02: Sensitive Information Disclosure
* **Auctoric Responsibility:** Offer automated client-side and edge PII tokenization/masking filters before inference dispatch; guarantee zero model retention for public training.
* **Customer Responsibility:** Classify sensitive datasets prior to ingestion; avoid passing unencrypted credentials, proprietary trade secrets, or unmasked PHI into general prompts.

### 3.3 LLM06: Excessive Agency & Autonomous Tool Execution
* **Auctoric Responsibility:** Provide deterministic guardrails, function-call permission scopes, runaway loop ceilings, and rate limits on tool execution.
* **Customer Responsibility:** Enforce human approval gates before downstream agents execute irreversible actions (e.g., executing financial wires, deleting database records, issuing formal legal notices).

---

## 4. Compliance RACI Matrix

* **R (Responsible):** The party executing the activity.
* **A (Accountable):** The party with ultimate decision ownership.
* **C (Consulted):** The party providing input or technical resources.
* **I (Informed):** The party kept updated on status.

| Compliance Task | Cloud / Model Provider | Auctoric | Customer |
| :--- | :---: | :---: | :---: |
| SOC 2 Type II Infrastructure Attestation | R/A | I | I |
| SOC 2 Type II Platform Application Attestation | I | R/A | I |
| Customer Downstream Application SOC 2 / ISO Certification | I | C | R/A |
| EU AI Act Conformity Assessment (High-Risk Systems) | I | R (System) | A (Deployment) |
| Customer Copyright Commitment (CCC) Defense | R (Upstream) | R/A (Output) | C (Compliance with Covenants) |
| HIPAA BAA Execution | I | R/A | R/A |
| User Credential Revocation upon Employee Departure | I | I | R/A |
| Incident Response for Cloud Infrastructure Outage | R/A | C | I |
| Incident Response for Model Inference Vulnerability | I | R/A | C/I |
| Customer Data Subject Access Request (DSAR) Fulfillment | I | C | R/A |

---

## 5. Contact & Support

For assistance regarding shared controls, architecture reviews, or compliance scoping:
* **Compliance Engineering:** `[compliance-eng@auctoric.ai]`
* **Trust & Security Portal:** `[https://trust.auctoric.ai]`
