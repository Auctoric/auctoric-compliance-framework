# Accessibility Conformance Statement (VPAT® / WCAG 2.2 AA / Section 508)

**Document Reference:** AUC-ACC-VPAT-001  
**Version:** 2.6 (Based on VPAT® Version 2.5 Rev)  
**Effective Date:** `[Insert Effective Date]`  
**Last Updated:** October 22, 2026  
**Classification:** Public / Procurement Guidance  
**Applicable Standards:** Web Content Accessibility Guidelines (WCAG) 2.2 Level AA Criteria | Revised Section 508 (US Rehabilitation Act) | EN 301 549 (EU)

---

## 1. Executive Summary & Evaluation Scope

**[Auctoric, Inc.]** ("**Auctoric**") is committed to digital accessibility for all users, including individuals with disabilities. This document provides an **Internal Interim Conformance Assessment** evaluating the Auctoric web console and documentation interfaces against WCAG 2.2 Level AA and Revised Section 508 standards.

* **Product Name:** Auctoric Governed AI Console & Documentation Portal
* **Product Version:** v2.4+
* **Product Description:** Web-based developer console, administrative dashboard, agent workflow builder, and API governance interface.
* **Evaluation Methods:** Evaluated internally using automated accessibility testing (Axe-core, Lighthouse), manual screen reader testing (NVDA, VoiceOver), and keyboard-only navigation simulations.
* **Assessment Status:** Self-Assessed Conformance Report; third-party audit planned for next major release cycle.

---

## 2. Terms and Conformance Levels

The terms used in the Conformance Level column are defined as follows:
* **Supports:** The functionality of the product has at least one method that meets the criterion without known defects.
* **Partially Supports:** Some functionality of the product does not meet the criterion, and remediation is underway.
* **Does Not Support:** The majority of product functionality does not meet the criterion.
* **Not Applicable:** The criterion is not relevant to the product.

---

## 3. WCAG 2.2 Conformance Matrix (Level A & Level AA)

### Principle 1: Perceivable

| Success Criterion | Conformance Level | Remarks and Explanations |
| :--- | :---: | :--- |
| **1.1.1 Non-text Content (Level A)** | **Supports** | Non-decorative UI icons, workflow diagrams, and visual badges provide descriptive `alt` text or `aria-label` attributes. |
| **1.2.1 Audio-only / Video-only (Level A)** | **Supports** | Video tutorials and platform walk-throughs provide closed captioning and text transcripts. |
| **1.3.1 Info and Relationships (Level A)** | **Supports** | Semantic HTML5 elements (`<nav>`, `<main>`, `<header>`, `<table>`) are utilized throughout. |
| **1.4.1 Use of Color (Level A)** | **Supports** | Color is never used as the sole indicator of status (error states feature icons and text labels). |
| **1.4.3 Contrast (Minimum) (Level AA)** | **Supports** | Text and interactive elements maintain a contrast ratio of at least 4.5:1 against backgrounds (3:1 for large text). |
| **1.4.10 Reflow (Level AA)** | **Supports** | Responsive layout reflows up to 400% zoom without horizontal scrolling. |
| **1.4.11 Non-text Contrast (Level AA)** | **Supports** | UI components (form fields, buttons, toggles) maintain >= 3:1 contrast against adjacent colors. |

### Principle 2: Operable

| Success Criterion | Conformance Level | Remarks and Explanations |
| :--- | :---: | :--- |
| **2.1.1 Keyboard (Level A)** | **Supports** | Interactive controls, code editors, prompt inputs, and dropdown menus are operable via keyboard navigation. |
| **2.1.2 No Keyboard Trap (Level A)** | **Supports** | Focus can be moved away from any component using standard tab or escape keys. |
| **2.4.3 Focus Order (Level A)** | **Supports** | Navigation sequence follows logical reading order and workflow hierarchy. |
| **2.4.7 Focus Visible (Level AA)** | **Supports** | High-visibility focus indicators (2px outline) appear around active elements during keyboard navigation. |
| **2.4.11 Focus Not Obscured (Minimum) (Level AA - WCAG 2.2)** | **Partially Supports** | Sticky navigation banners occasionally overlap active focus in deeply nested agent graph views; remediation scheduled. |
| **2.5.7 Dragging Movements (Level AA - WCAG 2.2)** | **Supports** | Canvas drag-and-drop operations provide alternative single-pointer button controls for node connection. |
| **2.5.8 Target Size (Minimum) (Level AA - WCAG 2.2)** | **Supports** | Interactive click/tap targets meet the minimum 24x24 CSS pixel boundary requirement. |

### Principle 3: Understandable

| Success Criterion | Conformance Level | Remarks and Explanations |
| :--- | :---: | :--- |
| **3.1.1 Language of Page (Level A)** | **Supports** | Natural language of each page is programmatically declared via HTML `lang="en"`. |
| **3.2.1 On Focus (Level A)** | **Supports** | Receiving focus does not initiate an unexpected context change or submit forms automatically. |
| **3.3.1 Error Identification (Level A)** | **Supports** | Input errors are identified and described to the user in text with `aria-live` announcements. |
| **3.3.2 Labels or Instructions (Level A)** | **Supports** | Form fields provide persistent labels and contextual helper tooltips. |
| **3.3.7 Redundant Entry (Level A - WCAG 2.2)** | **Supports** | Previously entered authentication tokens and organization IDs are auto-populated across steps. |
| **3.3.8 Accessible Authentication (Minimum) (Level AA - WCAG 2.2)** | **Supports** | Login flows support password managers, WebAuthn passkeys, and do not rely on cognitive function tests. |

### Principle 4: Robust

| Success Criterion | Conformance Level | Remarks and Explanations |
| :--- | :---: | :--- |
| **4.1.2 Name, Role, Value (Level A)** | **Supports** | Standard WAI-ARIA roles, states, and properties are correctly assigned to custom widgets. |
| **4.1.3 Status Messages (Level AA)** | **Supports** | Real-time streaming generation updates utilize `aria-live="polite"` to update screen readers unobtrusively. |

---

## 4. Revised Section 508 Chapter 5 (Software) Conformance

* **502.2.1 User Control of Accessibility Features:** Auctoric web software does not disrupt platform accessibility settings (such as high-contrast modes or screen magnification).
* **502.3.1 Object Information:** The user interface exposes name, role, value, and states to assistive technology via standard DOM interfaces.
* **503.2 User Preferences:** Respects system preferences for dark mode, reduced motion (`prefers-reduced-motion: reduce`), and contrast settings.

---

## 5. Assistive Technology Compatibility

The Auctoric platform has been tested internally and confirmed compatible with:
* **Screen Readers:** NVDA (Windows / Chrome & Firefox), VoiceOver (macOS / Safari & Chrome)
* **Screen Magnification:** ZoomText, macOS Zoom
* **Speech Input:** Dragon NaturallySpeaking, Apple Voice Control

---

## 6. Feedback, Inquiries, and Remediation Requests

Auctoric welcomes inquiries regarding accessibility and is committed to swift remediation of identified barriers:
* **Accessibility Coordinator:** `[accessibility@auctoric.ai]`
* **Compliance Inquiries:** `[compliance@auctoric.ai]`
* **Mailing Address:** `[Auctoric, Inc., Attn: Accessibility Team, 100 Enterprise Way, Suite 400, San Francisco, CA 94105]`
