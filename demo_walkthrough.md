# 5-Minute Demo Walkthrough

This walkthrough explains how to quickly understand the purpose of this repository and review example adversarial test cases.

The goal of this project is to demonstrate **structured AI red-teaming workflows** used to identify vulnerabilities in large language models (LLMs) and AI agent systems.

---

# Step 1 — Understand the Threat Model

Start with the threat model:

taxonomy/threat-model.md

This document explains:

- Who the adversaries are
- What systems are being tested
- What assets are at risk
- How attackers may attempt to manipulate AI systems

Understanding the threat model provides context for the adversarial tests.

---

# Step 2 — Review the Failure Taxonomy

Open:

taxonomy/failure-classes.md

This file defines the **types of failures** that can occur when models are manipulated.

Examples include:

- Instruction hierarchy violations
- Policy evasion
- Context leakage
- Over-compliance

This taxonomy ensures findings are labeled consistently.

---

# Step 3 — Examine Attack Techniques

Next open:

taxonomy/attack-techniques.md

This document explains the techniques used in adversarial testing.

Examples:

- Direct prompt injection
- Indirect prompt injection
- Persona hijacking
- Multi-turn escalation

These techniques form the basis of the attack scenarios in the repository.

---

# Step 4 — Review Example Attack Scenarios

Attack scenarios are located in:

attacks/

Examples include:

attacks/prompt-injection/role-confusion.md  
attacks/indirect-injection/rag-poisoned-document.md  
attacks/agent-exploitation/tool-exfiltration.md  

Each scenario documents:

- The adversarial prompt or setup
- Expected safe behavior
- Observed failure signals
- Security implications

These scenarios simulate real red-team testing techniques.

---

# Step 5 — Understand the Evaluation Framework

Open:

evaluations/evaluation-methodology.md

This document describes how adversarial tests are evaluated.

It includes:

- Testing procedures
- Failure classification rules
- Severity assignment
- Reproducibility requirements

This ensures findings are consistent and actionable.

---

# Step 6 — Review Signal Definitions

Open:

evaluations/signal-definitions.md

This document defines evaluation signals such as:

- PASS (Safe Behavior)
- FAIL — Partial Compliance
- FAIL — Full Compliance
- FAIL — Misleading Safety

These signals help standardize human evaluation of model responses.

---

# Project Goal

This repository demonstrates how **human-driven AI red-teaming** can identify vulnerabilities that automated benchmarks may miss.

The framework is designed to produce:

- reproducible adversarial test cases
- structured failure classifications
- high-quality human evaluation artifacts

These outputs can help improve the safety, robustness, and reliability of AI systems.

---

# Defensive Research Notice

All prompts and examples in this repository are designed for **defensive AI safety research**.

They use benign payloads and simulated data to illustrate adversarial techniques without enabling harmful real-world misuse.