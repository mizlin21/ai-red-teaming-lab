# Adversarial Test Index

This document provides a quick overview of all adversarial test scenarios included in this repository.

The goal is to make it easy to review attack coverage and understand what types of vulnerabilities are being tested.

---

# Prompt Injection Tests

| Test Case | Technique | Failure Class | Description |
|-----------|-----------|--------------|-------------|
| role-confusion.md | Role Confusion | Instruction Hierarchy Violation | Attempts to override system behavior by redefining the model’s role |

Location:

attacks/prompt-injection/role-confusion.md

---

# Indirect Prompt Injection Tests

| Test Case | Technique | Failure Class | Description |
|-----------|-----------|--------------|-------------|
| rag-poisoned-document.md | Retrieval Poisoning | Indirect Prompt Injection | Malicious instructions embedded in retrieved documents |

Location:

attacks/indirect-injection/rag-poisoned-document.md

---

# Agent Exploitation Tests

| Test Case | Technique | Failure Class | Description |
|-----------|-----------|--------------|-------------|
| tool-exfiltration.md | Tool Misuse | Sensitive Data Exposure | Attempts to extract internal configuration or API keys |

Location:

attacks/agent-exploitation/tool-exfiltration.md

---

# Coverage Summary

Current adversarial coverage includes:

- Prompt Injection
- Indirect Prompt Injection (RAG attacks)
- Agent Tool Misuse
- Instruction Hierarchy Violations
- Sensitive Data Exposure

Additional adversarial techniques can be added as new attack scenarios are developed.

---

# Purpose

This index provides a centralized view of adversarial testing coverage, making it easier to review experiments and track expansion of the red-team dataset.

This structure mirrors documentation practices commonly used in security research and AI safety evaluations.