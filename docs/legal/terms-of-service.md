# Terms of Service (ToS)

**Document Reference:** AUC-LEG-TOS-001  
**Version:** 4.0  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Legal  
**Architectural Framework:** Microsoft Modular Self-Service Structure + Google Flow-Down Provisions  
**Incorporated Schedules:** [Schedule 1: AI Service-Specific Terms (SST)](ai-service-specific-terms.md) | [Customer Copyright & IP Protection Addendum](customer-copyright-ip-protection-addendum.md) | [Acceptable Use Policy (AUP)](acceptable-use-policy.md)

---

Welcome to **Auctoric**! These Terms of Service ("**Terms**") govern your access to and use of the website, APIs, software development kits (SDKs), documentation, developer console, and Governed AI-as-a-System platform services (collectively, the "**Services**") provided by **[Auctoric, Inc.]** ("**Auctoric**", "we", "us", or "our").

By creating an account, calling our APIs, embedding our SDKs, or otherwise accessing the Services, you ("**User**" or "**You**") agree to be bound by these Terms and the incorporated [Schedule 1: AI Service-Specific Terms](ai-service-specific-terms.md). If you are using the Services on behalf of an organization, you represent that you have authority to bind that entity, and "you" refers to that organization.

---

## 1. Modular Structure and Service-Specific Rules

These Terms govern your general account relationship, authentication, and platform use. Specialized technical features—such as multi-model LLM routing, agentic tool execution, and vector embeddings—are governed by our incorporated **[Schedule 1: AI Service-Specific Terms (SST)](ai-service-specific-terms.md)**. If there is a direct conflict between these core terms and Schedule 1, Schedule 1 shall control with respect to AI-specific operations.

---

## 2. Eligibility & Account Security

### 2.1 Eligibility
You must be at least 18 years of age (or the age of majority in your jurisdiction) to use the Services.

### 2.2 Credential Protection
You are strictly responsible for safeguarding your credentials, API keys, client secrets, and access tokens. Any actions, API consumption, or agent workflows executed through your credentials are your legal responsibility. If you suspect an unauthorized compromise, notify `[security@auctoric.ai]` immediately.

---

## 3. Developer License, Upstream Flow-Downs & Restrictions

### 3.1 License Grant
Subject to these Terms, Auctoric grants you a limited, non-exclusive, non-transferable, revocable license to access and use the Services in accordance with our technical documentation at `[https://docs.auctoric.ai]`.

### 3.2 Google Cloud & Multi-Model Flow-Down Covenants
Because Auctoric orchestrates workloads across foundation model providers (including Google Cloud Vertex AI, Microsoft Azure OpenAI, and Anthropic), you agree to the following flow-down covenants:
1. **Anti-Model Distillation:** You shall not use Outputs to train, fine-tune, bootstrap, or calibrate any machine learning, foundation, or generative AI model that competes with Auctoric, Google Cloud, Microsoft Azure, or Anthropic;
2. **Reverse Engineering:** You shall not decompile, disassemble, or extract model weights, neural architectures, or latent representations of the Services;
3. **Benchmarking:** You shall not publicly disclose or publish competitive benchmarking or stress test evaluations without prior written approval from Auctoric;
4. **Upstream Abuse Suspension:** If an upstream hyperscaler (e.g., Google Cloud Trust & Safety) flags your account’s traffic for safety or policy violations, Auctoric may immediately suspend your API access.

---

## 4. Acceptable Use and High-Risk Boundaries

You must strictly comply with our [Acceptable Use Policy](acceptable-use-policy.md). In particular, you shall not use the Services for:
* **Clinical Medical Decisions:** Autonomous medical diagnosis, treatment planning, or emergency triage without licensed medical professional oversight;
* **Critical Infrastructure:** Nuclear facilities, public utility power grids, air traffic control, or life support systems;
* **Prohibited AI Practices:** Social scoring, biometric categorization of sensitive traits, or subliminal manipulation banned under the EU AI Act;
* **Cyberweapons & Exploitation:** Generating malware, automated hacking tools, or executing prompt injection attacks against platform infrastructure.

---

## 5. Content Rights, Non-Retention & Copyright Defense

### 5.1 Your Content (Inputs and Outputs)
* **Inputs:** You retain all ownership rights in the text, data, code, prompts, and media you submit to the Services.
* **Outputs:** As between you and Auctoric, Auctoric assigns to you all right, title, and interest in and to the Outputs generated specifically for you from your Inputs.
* **Zero Model Training on Customer Data:** Auctoric does **not** use Customer Inputs or Outputs to train, fine-tune, or calibrate public foundational models or any third-party models. See our [AI DPA & Model Non-Retention Addendum](../ai-governance/ai-dpa-model-non-retention-addendum.md).

### 5.2 Customer Copyright Commitment (Output Defense)
Paid commercial users are protected by our enterprise **Customer Copyright Commitment**, defending against third-party copyright claims on AI Outputs provided Auctoric's built-in safety filters remained active. Full terms and covenants are set forth in the [Customer Copyright & IP Protection Addendum](customer-copyright-ip-protection-addendum.md).

---

## 6. Billing, Metered Quotas, and Cancellation

### 6.1 Usage Metering
Certain features operate on metered billing (e.g., token usage, GPU compute hours, agent runtimes). You agree to pay all applicable fees according to the billing terms presented at checkout.

### 6.2 Cancellation
You may cancel your self-service subscription at any time via the Auctoric Console settings. Access will continue until the end of the current billing cycle, with no refunds for partial periods.

---

## 7. Disclaimers and Limitations of Liability

### 7.1 Non-Deterministic AI Output Disclaimer
YOU EXPRESSLY UNDERSTAND AND AGREE THAT ARTIFICIAL INTELLIGENCE MODELS EMPLOY STATISTICAL PATTERN PREDICTION AND CAN PRODUCE INCORRECT, FACTUALLY INACCURATE, OR UNINTENDED RESULTS ("HALLUCINATIONS"). YOU MUST INDEPENDENTLY VERIFY ALL CRITICAL OUTPUTS BEFORE RELYING UPON THEM.

### 7.2 Disclaimer of Warranties
TO THE MAXIMUM EXTENT PERMITTED BY LAW, THE SERVICES ARE PROVIDED "AS IS" AND "AS AVAILABLE", WITHOUT WARRANTIES OF ANY KIND, EXPRESS, IMPLIED, OR STATUTORY.

### 7.3 Limitation of Liability
IN NO EVENT SHALL AUCTORIC BE LIABLE FOR INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES. AUCTORIC’S MAXIMUM AGGREGATE LIABILITY FOR ALL CLAIMS UNDER THESE TERMS SHALL NOT EXCEED THE GREATER OF ONE HUNDRED US DOLLARS ($100 USD) OR THE AMOUNT YOU PAID AUCTORIC IN THE THREE (3) MONTHS PRECEDING THE CLAIM.

---

## 8. Dispute Resolution & Binding Arbitration

Any dispute, controversy, or claim arising out of or relating to these Terms will be settled by binding individual arbitration administered by the American Arbitration Association (AAA) under its Commercial Arbitration Rules. You waive any right to participate in class actions or class-wide arbitration.

---

## 9. Contact Information

* **Legal Department:** `[legal@auctoric.ai]`
* **Privacy Office:** `[privacy@auctoric.ai]`
* **Mailing Address:** `[Auctoric, Inc., 100 Enterprise Way, Suite 400, San Francisco, CA 94105]`
